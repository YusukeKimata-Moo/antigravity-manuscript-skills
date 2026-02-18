---
name: manuscript-translation
description: 分子生物学論文の日本語原稿を校正し、学術英語に翻訳するスキル
---

# 学術論文 日本語校正・英訳スキル

分子生物学の学術論文の日本語原稿を、英訳時に自然な表現になるよう校正したうえで、学術論文として最適な英語に翻訳する。

---

## 1. 作業フロー

```
日本語原稿 → [Phase 1] 日本語校正 → [Phase 2] 英訳 → [Phase 3] 英文校閲 → 最終英文
```

- 各Phaseの出力をユーザーに提示し、承認を得てから次のPhaseに進む
- 投稿予定の**ジャーナルと論文形式**（Article, Letterなど）を最初にユーザーに確認する

---

## 2. Phase 1: 日本語校正（英訳前処理）

意味・論理を変更せず、英訳時に自然な英語になりやすい日本語に校正する。

### 2.1 修正すべきパターン

| #   | 日本語パターン                         | 問題点                                      | 修正方針                                        |
| --- | -------------------------------------- | ------------------------------------------- | ----------------------------------------------- |
| 1   | 「AことからBと考えられている」         | Aが重い場合、英語で一文が冗長               | Aで文を切り「この知見から、B」と分割            |
| 2   | 「Aことに加え、Bことが報告されている」 | 並列が長くなり"in addition to A, B"は不自然 | 2文に分割                                       |
| 3   | 「AがBを及ぼしていない」               | 主語が不明確                                | 「AはBを及ぼさない」（「は」で主語明示）        |
| 4   | 「〜場合と〜場合とがあった」           | 英語に対応構文なし                          | 「〜または〜として観察された」に簡潔化          |
| 5   | 長い修飾節 + 名詞                      | 関係代名詞節に変換しにくい                  | 修飾節を短縮するか文を分割                      |
| 6   | 助詞「〜における〜の〜が」の連鎖       | 主語・目的語が曖昧                          | 「は」で主語を明示し構造を単純化                |
| 7   | 「〜を行った」の多用                   | "performed/conducted"の繰り返し             | 動詞を直接使う（「解析を行った」→「解析した」） |
| 8   | 二重否定「〜でないことはない」         | 英語で回りくどい                            | 肯定文に書き換え                                |

### 2.2 校正の原則

- **意味・論理の変更は禁止**
- 文の分割、助詞の変更、修飾節の簡略化のみ
- 校正箇所を**表形式で提示**し、承認後に実行

---

## 3. Phase 2: 英訳

### 3.1 翻訳の基本方針

- **直訳ではなく、英語論文として自然な表現**を採用する
- 各セクションの文体は英語学術論文の慣例に従う
- 受動態と能動態を適切に使い分ける（Methodsは受動態中心、Resultsは混在が自然）

### 3.2 セクション別の時制ルール

| セクション   | 内容                     | 時制            | 例                                                 |
| ------------ | ------------------------ | --------------- | -------------------------------------------------- |
| Introduction | 一般的事実・定説         | 現在形          | "X plays an essential role in..."                  |
|              | 先行研究の報告           | 現在完了形      | "Recent studies have revealed that..."             |
|              | 未解決の問題             | 現在形          | "However, it remains unclear whether..."           |
|              | 本研究の目的             | 過去形          | "In this study, we aimed to..."                    |
|              | 結果の要約               | 過去形          | "Our results revealed that..."                     |
| Results      | 実験操作・観察結果       | 過去形          | "We observed that..." / "X was detected..."        |
|              | 定量結果                 | 過去形          | "No significant difference was detected..."        |
|              | 他種との比較（先行研究） | 現在完了形      | "This has also been reported in..."                |
| Discussion   | 本研究知見の要約         | 過去形          | "We found that..."                                 |
|              | 先行研究との比較         | 現在完了/現在形 | "has been reported" / "is consistent with"         |
|              | 推測・可能性             | 助動詞          | "may/might/could" / "suggesting that"              |
|              | 今後の課題               | 未来・不定      | "will require" / "remains to be determined"        |
| Methods      | 実験操作                 | 過去形・受動態  | "Plants were grown..." / "Images were acquired..." |

### 3.3 学術英語の表現ガイド

#### 動詞・述語の選択

| 日本語                   | 推奨英訳                               | 避けるべき訳                        |
| ------------------------ | -------------------------------------- | ----------------------------------- |
| 〜を明らかにした         | revealed / demonstrated / showed       | made clear                          |
| 〜が示された             | was shown / was demonstrated           | was indicated                       |
| 〜が示唆された           | suggested / implied                    | was suggested to be                 |
| 〜が認められた           | was observed / was detected            | was recognized                      |
| 〜と一致する             | is consistent with / corroborates      | matches                             |
| 〜に重要/必須である      | is essential for / is required for     | is important for（弱い場合は可）    |
| 〜の可能性がある         | may / might / could                    | there is a possibility that         |
| 〜とは異なる             | differs from / is distinct from        | is different from（口語的）         |
| 有意差は検出されなかった | No significant difference was detected | There was no significant difference |
| 〜を目的とした           | aimed to / sought to                   | purposed to                         |

#### 主張の強度（hedging）

| 強度 | 英語表現                              | 使用場面                   |
| ---- | ------------------------------------- | -------------------------- |
| 強   | demonstrate, establish, determine     | 直接的な実験証拠がある場合 |
| 中   | show, reveal, indicate                | 明確なデータに基づく場合   |
| 弱   | suggest, imply, raise the possibility | 間接的証拠や推測の場合     |
| 最弱 | may, might, could, is conceivable     | 仮説レベルの議論           |

#### 接続・展開表現

| 機能   | 推奨表現                                                         |
| ------ | ---------------------------------------------------------------- |
| 追加   | Furthermore, Moreover, In addition, Additionally                 |
| 対比   | However, In contrast, By contrast, Conversely, On the other hand |
| 因果   | Therefore, Thus, Consequently, Accordingly                       |
| 具体化 | Specifically, In particular, Notably                             |
| 譲歩   | Although, Despite, Notwithstanding                               |
| 要約   | Taken together, Collectively, Overall                            |

### 3.4 翻訳の粒度

- パラグラフ単位で翻訳し、ユーザーに提示する
- 原文と英訳を**対照表形式**または**段落ごとの並列表示**で提示する
- 複数の訳語候補がある場合は注釈で選択肢を示す

---

## 4. Phase 3: 英文校閲

### 4.1 チェック項目

- [ ] **時制の一貫性**: セクション内で時制が統一されているか
- [ ] **冠詞**: a/an/the の使い分け（初出 vs 既出、特定 vs 不特定）
- [ ] **数の一致**: 主語と動詞、名詞と代名詞の数
- [ ] **学名の表記**: イタリック体、初出はフルネーム+著者名
- [ ] **略語**: 初出でフルスペルアウト＋括弧内に略語
- [ ] **同一語の反復回避**: 同一パラグラフ内の同一動詞・形容詞の多用
- [ ] **hedgingの強度**: 推測表現と主張内容の一致
- [ ] **接続詞の多様性**: 同一接続詞の連続使用を回避
- [ ] **パラレリズム**: 列挙・対比で文法構造が揃っているか

---

## 5. 出力フォーマット

### 5.1 日本語校正の提示

| #   | 箇所          | 現在の表現 | 修正案 | 理由           |
| --- | ------------- | ---------- | ------ | -------------- |
| 1   | Section, Line | 原文引用   | 修正文 | 英訳時の問題点 |

### 5.2 英訳の提示

```
【原文】
日本語パラグラフ

【英訳】
English paragraph

【注記】（任意）
- 訳語の選択理由や代替案
```
