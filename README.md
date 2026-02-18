# Antigravity Skills for Academic Manuscript Writing

分子生物学の学術論文原稿を執筆・校正・英訳するための [Antigravity](https://blog.google/technology/google-deepmind/antigravity-ai-coding-agent/) スキルセットです。

### スキル一覧

| スキル                     | 説明                                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------------------ |
| **manuscript-review**      | 日本語原稿の論理構造・セクション間整合性・用語の一貫性をチェックし、英訳しやすいように修正を支援 |
| **manuscript-translation** | 日本語原稿を英訳しやすい文体に校正したうえで、学術英語に翻訳                                     |

### セットアップ

プロジェクトの `.agent/skills/` ディレクトリにスキルフォルダをコピーしてください。

```
your-project/
└── .agent/
    └── skills/
        ├── manuscript-review/
        │   └── SKILL.md
        └── manuscript-translation/
            └── SKILL.md
```

```bash
# リポジトリをクローンし、スキルをコピー
git clone https://github.com/<your-username>/antigravity-manuscript-skills.git
cp -r antigravity-manuscript-skills/manuscript-review .agent/skills/
cp -r antigravity-manuscript-skills/manuscript-translation .agent/skills/
```

スキルは Antigravity が自動的に検出します。追加の設定は不要です。

### 使い方

Antigravity に論文原稿の精査や英訳を依頼すると、関連するスキルが自動的に参照されます。

**例：原稿レビュー**

```
Introduction, Results, Discussion の内容を精査し、セクション間の整合性を確認せよ
```

**例：英訳**

```
Discussion セクションを学術英語に翻訳せよ
```

### 想定する使用環境

- 日本語で原稿を執筆し、最終的に英訳するワークフロー
- セクションごとに個別のMarkdownファイルで管理する原稿構成
- 分子生物学・生命科学分野の学術論文（他分野にも応用可能）
