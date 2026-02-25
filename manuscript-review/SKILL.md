---
name: manuscript-review
description: Review and proofread molecular biology manuscript sections for structural consistency, logical flow, and cross-section coherence. Use when checking, reviewing, or proofreading Japanese or English manuscript drafts, verifying section consistency (Introduction/Results/Discussion/Methods), or analyzing manuscript structure.
---

# 学術論文原稿レビュー・修正スキル

分子生物学の学術論文原稿を精査・修正するためのスキル。

## 前提条件

- 原稿は**日本語**で執筆し、最終的に英訳することを前提とする
- 英語原稿のレビューの場合、文体チェック（日本語パターン修正）はスキップし、構造・一貫性チェックのみ実施する
- 英訳作業には `manuscript-translation` スキルを使用する

---

## 1. 原稿読み込みと全体構造の把握

### 1.1 ファイル構成の確認

- 原稿ディレクトリ内のすべてのセクションファイルを特定する
- 典型的な構成: Introduction, Results, Discussion, Methods, Supplemental Methods

### 1.2 セクション間の対応関係マッピング

各セクション間で以下の対応関係を確認する：

| 確認項目     | Introduction → Results                         | Results → Discussion                          | Methods ↔ Supplemental Methods                    |
| ------------ | ---------------------------------------------- | --------------------------------------------- | ------------------------------------------------- |
| トピック順序 | Introで予告した順序でResultsが展開されるか     | Resultsの順序でDiscussionが議論されるか       | 同一手法が矛盾なく記述されているか                |
| 用語の一貫性 | 同一概念に同一用語を使用しているか             | 同左                                          | 同左                                              |
| 情報の過不足 | Introで伏線を張った項目がResultsで回収されるか | Resultsで示した知見がDiscussionで議論されるか | Methodsの簡略記述がSupplementalで補完されているか |

---

## 2. セクション別チェックリスト

各セクションの詳細なチェック項目と具体例は [section_checklists.md](references/section_checklists.md) を参照。

主要チェック観点：

- **Introduction**: パラグラフ構造、トピック順序とResultsの対応、最終パラグラフの役割
- **Results**: セクション見出し、手法切り替え、定量データ、Figure参照
- **Discussion**: Resultsとの対応、論理の飛躍、パラグラフ間の重複、新規情報の導入
- **Methods**: MethodsとSupplemental Methodsの整合性

---

## 3. 日本語文体チェック（英訳前処理）

英訳時に自然な英語になりやすい日本語へ校正する。修正パターンと具体例は [japanese_patterns.md](../shared-references/japanese_patterns.md) を参照。

---

## 4. 修正実行のルール

### 4.1 修正前に必ずユーザーに確認

- 投稿予定の**ジャーナルと論文形式**を [journal_guidelines.md](../shared-references/journal_guidelines.md) に記入してもらい、内容を参照する
- 修正箇所と修正案を**表形式で一覧提示**する
- 各修正の**理由**を明記する
- ユーザーの承認後に実行する

### 4.2 修正の粒度

- 同一ファイル内の非連続な変更はまとめて実施する
- 変更は**最小限の文字列置換**にとどめ、パラグラフ全体の書き換えは避ける
- 変更完了後に**変更サマリを表形式で報告**する

### 4.3 提案と実行の分離

- 「検討せよ」「確認せよ」→ **分析結果のみ提示**、修正は実行しない
- 「修正せよ」→ **修正案を提示し承認を得てから**実行する
- 「反映」「OK」「はい」→ 承認された修正を実行する

---

## 5. 分析レポートのフォーマット

セクション間の整合性チェック結果の報告フォーマットは [report_format.md](references/report_format.md) を参照。

---

## 6. スキル間連携

```
[manuscript-review] 日本語原稿の構造・一貫性チェック + 日本語校正
        ↓ 修正完了後
[manuscript-translation] 日本語校正(Phase 1) → 英訳(Phase 2) → 英文校閲(Phase 3)
```
