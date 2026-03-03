---
name: journal-guideline-checker
description: Checks molecular biology manuscript drafts against journal submission guidelines by exploring the provided journal guideline URL. Extracts rules such as section structure, reference formatting, and figure requirements using a browser subagent, then validates the manuscript files to ensure compliance. Note that word counts and English spelling (UK/US) regulations are handled by the manuscript-translation skill. Use when the user asks to check manuscript formatting or submission compliance. If the user does not provide a journal guideline URL, you MUST ask the user to provide one.
---

# ジャーナル投稿規程（Guideline）コンプライアンスチェッカー

投稿先のジャーナル（論文誌）の投稿規程（Author Guidelines / Formatting Requirements等）URLを巡回してルールを抽出し、原稿ファイルが構造やフォーマットの規定を満たしているかを自動検証するスキル。

---

## 1. 役割分担の原則

本スキル（`journal-guideline-checker`）は、**構造や体裁・フォーマット**に焦点を当てます。英文の単語数（AbstractやMain textの語数制限）や、イギリス英語/アメリカ英語の指定など、言語（英語）そのものに依存するルールについては `manuscript-translation`（英文校正フェーズ）に委ね、本スキルではメインの検証対象から外すか簡易な警告に留めます。

### 本スキルが検証する主な項目：

- **セクション構成**: 必須セクションの有無、順序（例: Introduction → Results → Discussion → Methods か、それとも Methods が最後か）
- **参考文献（References）**: ジャーナル指定のフォーマット（本文中の引用スタイル `(Smith et al., 2026)` vs `[1]`、末尾のリスト形式）
- **スタイル指定**: ダブルスペース、行番号付け、改ページ指定、フォント要件の指示
- **Figure / Table 要件**: パネルのラベル付け（A, B...）、Legendの配置場所
- **必須のステートメント**: Data Availability, Author Contributions, Conflict of Interest 等の有無

---

## 2. 作業フロー

ユーザーが「投稿規程を満たしているかチェックして」等と依頼した場合、以下のフェーズで進行します。

### Phase 1: 規程情報の収集とルール化

まず、`../shared-references/journal_guidelines.md` の存在と内容を確認します。

- **ファイルが存在し、かつ具体的な指定が記載されている（新規URL指定もない）場合**:
  すでに抽出済みのルールがあるとみなし、ブラウザ探索はスキップしてそのファイルを読み込みます（ステップ2へ進む）。
- **ファイルが存在しない場合、ファイル内にテンプレートであることを示す目印（「これはテンプレートファイルです」等）が含まれている場合、またはユーザーから新しいURLの指定があった場合**:
  1. ユーザーにジャーナルの投稿規程（Author Guidelines等）のトップページURLの提供を求めます。
  2. **ブラウザ操作による情報収集**:
     - ツール `browser_subagent` を起動し、送信されたジャーナルURLおよび下層ページを探索します。
     - `Task`: 「提供されたURLから、英語の規程（単語数制限やUS/UK指定等）および、原稿構造の規程（セクション構成、引用形式、Figure要件など）をすべて網羅的に抽出し、マークダウン形式で `../shared-references/journal_guidelines.md` に出力して保存して。」等と設定し、**必ずファイルへ出力・保存させます**。

上記のいずれかの方法でルールファイル (`journal_guidelines.md`) が用意できたら、ファイルに記載されたチェックリスト（今回は「構造や体裁・フォーマット」に関する部分のみ）をユーザーに一度提示します（「以下の項目をチェックします」）。

### Phase 2: 原稿ファイルの検証

1. **原稿の読み込み**:
   - 対象のMarkdownファイル（Introduction, Results, Discussion, Methods 等）を読み込みます。
2. **規程との照合**:
   - Phase 1で構築したルールに沿って、原稿全体をスキャン・検証します。
3. **レポート提出**:
   - 違反箇所、要修正箇所を具体的なファイル名・行番号とともにリストアップします。必要に応じてファイルを修正（フォーマット整形等）するためのプランをユーザーに提案します。

## 3. アクションごとのプロンプト例（内部処理用）

```markdown
- **ユーザーからの曖昧な依頼への対応（例）**:
  - 「このジャーナルの規定に合ってるか見て：[URL]」
  - 「Natureのフォーマットに直して」
- **ブラウザサブエージェントへの指示（内部）**:
  「提供されたURL（またはジャーナル名から検索した規程ページ）から、セクション構成、引用形式、図表、必須ステートメント等のルールを網羅的に抽出し、`../shared-references/journal_guidelines.md` に保存してください。」
- **検証結果の提示と提案（例）**:
  - 「規程ではMethodsが末尾ですが、現在はIntroductionの直後にあります。移動しますか？」
  - 「参考文献が[1]形式になっていますが、規程は(Author, Year)形式です。修正案を作成しましょうか？」
```
