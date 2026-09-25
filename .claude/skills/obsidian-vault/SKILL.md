---
name: obsidian-vault
description: Read and write the user's Obsidian Vault（メモ・知識・Skill の蓄積）. Use when the user mentions Obsidian, the Vault, ノート, Inbox整理, 記録して, or asks to remember something in notes.
---

# Obsidian Vault の読み書き

## 場所
- このリポジトリ（TK-Owner/Obsidian-Github, main）が Vault 本体。PC 側では `C:\Users\TK-MAIN-202605\BOT\Obsidian Vault`
- Obsidian Git プラグインが PC 側で自動 commit/push/pull する。Claude Code は編集後に `git add -A && git commit -m "<日本語1行>" && git push`
- 作業前に `_Claude運用ルール.md` を読む

## フォルダ
| フォルダ | 用途 | Claude の扱い |
|---|---|---|
| Home.md | 入口・最近の更新 | 更新時に1行追記 |
| 00_Inbox | 未整理メモ | 読んで振り分け案を提示 |
| LINE/ | LINE 同期の受信箱 | 読むだけ（Inbox 扱い） |
| 10_Knowledge | 整理済み知識（索引: Knowledge.md） | 追記・新規作成 |
| 20_Skills | 手順書（索引: Skills.md） | 追記・Skill 化の提案 |
| 30_Projects | 案件（索引: Projects.md） | 状態・決定事項の追記 |
| 90_Templates | ひな形 | 新規ノート作成時に使う |
| .claude/skills | Claude Code 用 Skill | skill-creator で作成・改善 |
| .obsidian/ | Obsidian 設定 | 触らない |

## 記録の手順
1. 該当テーマの既存ノートを索引から探す。なければテンプレートから新規作成し、索引にリンクを追加
2. 末尾に `## YYYY-MM-DD` 見出しを付けて追記。既存本文は書き換えない（訂正は「訂正:」付きで追記）
3. frontmatter の `updated` を更新し、Home.md の「最近の更新」に1行足す
4. 結論を先に、根拠・出典（URL・日付）は短く。機密情報（API キー、パスワード、口座番号）は書かない

## Inbox 整理の手順
1. `00_Inbox/Inbox.md` の未チェック項目と `LINE/` 配下の未処理ノートを列挙
2. 各項目を 知識 / 手順 / 案件 / 捨てる に分類し、振り分け案を提示して確認を取る
3. 承認後に該当ノートへ追記し、Inbox にチェック、LINE ノート末尾に `processed: YYYY-MM-DD` を追記

## Skill 化
20_Skills の手順書が「安定」になったら、skill-creator を使って `.claude/skills/<name>/SKILL.md` として作成する。Vault の手順書ノートには `status: Skill化済み` と Skill 名を追記する。
