# Obsidian Vault — Claude 向けガイド

この リポジトリは Obsidian Vault。Cowork と Claude Code の両方から読み書きする共有ナレッジベース。
作業前に `_Claude運用ルール.md` を読むこと。

## 構成
- `Home.md` 入口。更新したら「最近の更新」に1行足す
- `00_Inbox/` 未整理メモ。`LINE/` は LINE 同期の受信箱（Inbox 扱い、読むだけ）
- `10_Knowledge/` 整理済み知識。索引は `10_Knowledge/Knowledge.md`
- `20_Skills/` 手順書。索引は `20_Skills/Skills.md`。状態: 下書き→試用中→安定→Skill化済み
- `30_Projects/` 案件。索引は `30_Projects/Projects.md`
- `90_Templates/` ひな形。新規ノートはここから

## 書き込みルール
- 追記は末尾に `## YYYY-MM-DD` 見出し付き。既存本文は書き換えない（訂正は「訂正:」付きで追記）
- frontmatter の `updated` を更新する
- 新規ノートは索引にリンクを追加する
- 機密情報（APIキー、パスワード、口座番号）は書かない
- `.obsidian/` は触らない

## Claude Code での運用
- 作業後は `git add -A && git commit -m "..." && git push` で同期する（Obsidian 側は Obsidian Git プラグインが pull/push）
- コミットメッセージは日本語で「何を記録したか」を1行
