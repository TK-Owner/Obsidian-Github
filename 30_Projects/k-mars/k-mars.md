---
tags: [project, k-mars]
status: 進行中
updated: 2026-09-24
---
# k-mars（別事業）

## 目的
k-mars.com 名義で運用する別事業の土台を、当面はこの Vault（kurakawa 側）で作り、固まったら k-mars 組織の Vault へ丸ごと引っ越す。この事業に関する決定事項・案件・下書きはすべて `30_Projects/k-mars/` 配下に置く（共通の知識は 10_Knowledge に置いてよい）。

## 決定事項・期限
- 2026-09-24: Claude の Team 組織「k-mars」を作成し、tk-owner@kurakawa.co.jp をメンバーとして追加（許可ドメインに kurakawa.co.jp を追加して招待）。k-mars.com の DNS は お名前.com（GMO）で管理
- 2026-09-24: Skill・プラグイン・コネクタ・記憶・スケジュールタスクは組織単位で共有されないため、k-mars 側では入れ直す。自作 Skill は obsidian-vault の 1 つ（k-mars 用に Vault パスを変えて渡す）
- 2026-09-24: 土台づくりはこの Vault で進め、プロジェクト単位で k-mars 組織へ引っ越す方式にする（Cowork のプロジェクト・チャットは組織間で移せないので、Vault のフォルダと Skill の ZIP を持っていき、プロジェクトは作り直す）
- 機密（契約書・口座・顧客名など）はこの Vault には置かず、早めに k-mars 側で扱う

## 引っ越し手順（固まったら）
1. `30_Projects/k-mars/` を新しい Vault フォルダ（例: `C:\Users\TK-MAIN-202605\BOT\k-mars Vault`）に移す
2. `_Claude運用ルール.md`・`CLAUDE.md`・`90_Templates/`・各索引（Knowledge.md / Skills.md / Projects.md）・`Home.md` を複製する
3. 持っていきたい共通ノート（10_Knowledge、20_Skills）はコピーする
4. k-mars 組織で obsidian-vault Skill（k-mars 版）をアップロードし、必要なプラグインとコネクタを入れ直す
5. k-mars 組織の Cowork で新しい Vault フォルダを連携し、プロジェクトとスケジュールタスクを作り直す

## 2026-09-24
- フォルダ `30_Projects/k-mars/` を作成。以後、この事業のノートはここに置く
