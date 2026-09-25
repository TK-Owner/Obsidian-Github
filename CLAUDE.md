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

## Skill の自動蓄積（セッション終了時に必ず行う）
1. 作業を終える前に `00_Inbox/セッションログ/YYYY-MM-DD.md` に追記する（無ければ作成）:
   - 何をしたか（3行以内）
   - 繰り返し使えそうな手順があれば「候補: <名前> — <一言>」
2. 同じ種類の作業が2回目以降なら、`20_Skills/<名前>.md` を Skill テンプレートで下書きし、`20_Skills/Skills.md` の表に「下書き」で追加する
3. 「安定」と判断できる手順書は skill-creator で `.claude/skills/<name>/` に作成し、ノート側の status を「Skill化済み」にする
4. 最後に commit & push
