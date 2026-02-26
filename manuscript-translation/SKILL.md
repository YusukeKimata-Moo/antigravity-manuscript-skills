---
name: manuscript-translation
description: Translate Japanese molecular biology manuscript sections into academic English through a structured 3-phase workflow (Japanese proofreading, translation, English editing). Also use for standalone English proofreading and editing of molecular biology manuscripts. Use when translating Japanese manuscript text to English, proofreading Japanese text for translation readiness, proofreading or editing English manuscript sections, or checking English grammar, style, and terminology in scientific manuscripts.
---

# 学術論文 日本語校正・英訳・英文校正スキル

分子生物学の学術論文の日本語原稿を校正・英訳するスキル。英文原稿の校正（校閲）にも単独で使用できる。

---

## 1. 作業フロー

### フローA: 日本語原稿 → 英訳（全Phase実行）

```
日本語原稿 → [Phase 1] 日本語校正 → [Phase 2] 英訳 → [Phase 3] 英文校閲 → 最終英文
```

### フローB: 英文校正のみ（Phase 3 単独実行）

```
英文原稿 → [Phase 3] 英文校閲 → 修正済み英文
```

ユーザーが英文の校正・校閲・proofreading を依頼した場合、**フローB**（Phase 3 のみ）を実行する。

### 共通ルール

- 各Phaseの出力をユーザーに提示し、承認を得てから次のPhaseに進む
- 投稿予定の**ジャーナルと論文形式**を [journal_guidelines.md](../shared-references/journal_guidelines.md) に記入してもらい、内容を参照する

### ユーザー承認ルール

- 「検討せよ」「確認せよ」→ **分析結果のみ提示**、修正は実行しない
- 「修正せよ」「翻訳せよ」「校正せよ」→ **案を提示し承認を得てから**実行する
- 「反映」「OK」「はい」→ 承認された内容を実行する

---

## 2. Phase 1: 日本語校正（英訳前処理）

意味・論理を変更せず、英訳時に自然な英語になりやすい日本語に校正する。

修正パターンと具体例は [japanese_patterns.md](../shared-references/japanese_patterns.md) を参照。

校正箇所を**表形式で提示**し、承認後に実行する。

### 出力フォーマット

| #   | 箇所          | 現在の表現 | 修正案 | 理由           |
| --- | ------------- | ---------- | ------ | -------------- |
| 1   | Section, Line | 原文引用   | 修正文 | 英訳時の問題点 |

---

## 3. Phase 2: 英訳

### 3.1 翻訳の基本方針

- **直訳ではなく、英語論文として自然な表現**を採用する
- 各セクションの文体は英語学術論文の慣例に従う
- 受動態と能動態を適切に使い分ける（Methodsは受動態中心、Resultsは混在が自然）

### 3.2 翻訳手順

1. **セクション全体を通読**し、文脈・論理の流れを把握する
2. **パラグラフ単位で翻訳**する
3. **セクション全体の接続・一貫性をチェック**する（接続詞の整合性、用語統一）

### 3.3 時制・表現リファレンス

- セクション別時制ルール: [tense_rules.md](references/tense_rules.md)
- 動詞選択・hedging・接続表現: [academic_english_guide.md](references/academic_english_guide.md)

### 3.4 学名・略語のルール

- **学名**: イタリック体。初出はフルネーム（例: _Marchantia polymorpha_）、以降は省略可（例: _M. polymorpha_）
- **略語**: 初出でフルスペルアウト＋括弧内に略語（例: green fluorescent protein (GFP)）

### 3.5 出力フォーマット

```
【原文】
日本語パラグラフ

【英訳】
English paragraph

【注記】（任意）
- 訳語の選択理由や代替案
```

---

## 4. Phase 3: 英文校閲

翻訳後の後処理として、またはフローBとして英文原稿の単独校正に使用する。

### 4.1 校正手順

1. **セクション全体を通読**し、論理の流れと文脈を把握する
2. **チェック項目に沿って精査**する（§4.2）
3. 指摘事項を**表形式で提示**し、承認後に修正する

### 4.2 チェック項目

#### 文法・文体

- [ ] **時制の一貫性**: セクション内で時制が統一されているか（[tense_rules.md](references/tense_rules.md) 参照）
- [ ] **冠詞**: a/an/the の使い分け（初出 vs 既出、特定 vs 不特定）
- [ ] **数の一致**: 主語と動詞、名詞と代名詞の数
- [ ] **受動態/能動態のバランス**: セクションの慣例に沿った適切な使い分け
- [ ] **同一語の反復回避**: 同一パラグラフ内の同一動詞・形容詞の多用
- [ ] **接続詞の多様性**: 同一接続詞の連続使用を回避
- [ ] **パラレリズム**: 列挙・対比で文法構造が揃っているか

#### 論旨の明確化・簡潔化

- [ ] **冗長表現の削除**: 意味に寄与しない語句（"Interestingly,", "It should be noted that", "It is well known that", "As mentioned above," 等）を削除し、論旨を直接述べる
- [ ] **重複の排除**: 同一パラグラフ内や隣接パラグラフ間で同じ主張が繰り返されていないか
- [ ] **文構造の簡素化**: 複雑な入れ子節や過剰な修飾語句を整理し、一文一意の原則に近づける
- [ ] **空語の削減**: データに基づかない過度な主張や、内容の伴わない惣美語句を削除する

#### 学術表現

- [ ] **hedgingの強度**: 推測表現と主張内容の一致（[academic_english_guide.md](references/academic_english_guide.md) 参照）
- [ ] **動詞選択の適切性**: 学術英語として適切な動詞を使用しているか（[academic_english_guide.md](references/academic_english_guide.md) 参照）
- [ ] **学名の表記**: イタリック体、初出はフルネーム
- [ ] **略語**: 初出でフルスペルアウト＋括弧内に略語

#### 分子生物学論文特有のチェック

- [ ] **統計表現**: 統計手法・サンプル数・p値の記載が正確か（例: "Student's _t_-test, _n_ = 3, _P_ < 0.05"）
- [ ] **定量データの記述**: 数値に単位・誤差範囲（±SD, ±SEM）が付されているか
- [ ] **Figure/Table参照**: 本文とFigure legend間で番号・パネル記号が一致しているか
- [ ] **Figure legend**: 各パネルの説明が過不足なく記載されているか。スケールバー・サンプル数・統計情報の記載
- [ ] **遺伝子/タンパク質の表記**: 遺伝子名はイタリック、タンパク質名はローマン体で統一されているか
- [ ] **試薬・抗体の記載**: メーカー名・カタログ番号・濃度や希釈倍率が適切に記載されているか（Methods）
- [ ] **再現性の記述**: 独立した生物学的反復（biological replicates）と技術的反復（technical replicates）が区別されているか

### 4.3 出力フォーマット

| #   | 箇所          | 現在の表現 | 修正案 | カテゴリ | 理由       |
| --- | ------------- | ---------- | ------ | -------- | ---------- |
| 1   | Section, Line | 原文引用   | 修正文 | 時制     | 具体的説明 |

カテゴリ: 時制 / 冠詞 / 数の一致 / 学名 / 略語 / hedging / 簡潔化 / 統計 / Figure参照 / 表記 / 文体 / その他
