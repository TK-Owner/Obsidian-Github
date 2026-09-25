# Claude 運用ルール

このVaultは Claude（Cowork）と共有し、Claude が直接ノートを読み書きする。

## Claude がやること
- 会話で得た結論・調査結果・決定事項を、該当ノートに追記する（新規テーマは新ノート）
- 追記は必ず `## YYYY-MM-DD` の日付見出し付きで、末尾に追加する
- 既存の本文は勝手に書き換えない。訂正が必要な場合は日付付きで「訂正:」と追記する
- 依頼があれば 00_Inbox を読み、10_Knowledge / 20_Skills / 30_Projects に振り分ける
- 20_Skills の手順書が安定したら、Cowork の Skill として提案する（保存はユーザーが承認）

## ノートの書き方
- ファイル名は日本語可。テーマは1ノート1つ
- 先頭に frontmatter（tags, updated）を付ける
- 関連ノートは `[[リンク]]` でつなぐ
- 機密情報（APIキー、パスワード、口座番号など）はVaultに書かない

## フォルダ
| フォルダ | 用途 | Claudeの扱い |
|---|---|---|
| 00_Inbox | 未整理メモ、LINE同期 | 読んで振り分け候補を提案 |
| 10_Knowledge | 整理済み知識 | 追記・新規作成 |
| 20_Skills | 手順書・テンプレート | 追記・Skill化の提案 |
| 30_Projects | 進行中の案件 | 状態・決定事項の追記 |
| 90_Templates | ひな形 | 使うだけ |
| LINE | LINE同期の受信箱 | 読むだけ（Inbox扱い） |

## Skill の自動蓄積
- Cowork / Claude Code とも、作業の終わりに `00_Inbox/セッションログ/YYYY-MM-DD.md` へ「何をしたか」と「繰り返せそうな手順の候補」を書く
- 同じ作業が2回目以降なら `20_Skills/` に下書きを起こし、Skills.md の表に追加する
- 毎週月曜の自動タスク（Skill 収穫）がセッションログ・Inbox・LINE・git 履歴を読み、Skill 候補を `20_Skills/` に下書きして Skills.md を更新する。人間はそれを見て「安定」にするか捨てるかを決める
- 安定した手順書は skill-creator で `.claude/skills/` に Skill 化する（Claude Code）／Cowork の Skill として提案する（Cowork）

## 2026-09-24 事業別フォルダと引っ越し
- 別事業（k-mars など）の決定事項・案件・下書きは `30_Projects/<事業名>/` 配下にまとめる。共通の知識は 10_Knowledge に置いてよい
- 事業が別の Claude 組織に移るときは、その `30_Projects/<事業名>/` フォルダと、運用ルール・CLAUDE.md・90_Templates・索引・Home を複製して新しい Vault を作る。Cowork のプロジェクトとチャットは組織間で移せないので作り直す
- 機密（契約書・口座・顧客名など）は土台づくり中もこの Vault に置かない
