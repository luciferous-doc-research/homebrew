# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 概要

Homebrewのドキュメント（`source/docs/`）を探索・調査するためのリポジトリ。
`source/` は [Homebrew/brew](https://github.com/Homebrew/brew) のgitサブモジュール。

## サブモジュール管理

```bash
make init    # サブモジュールを初期化・クローン（初回セットアップ）
make update  # サブモジュールをリモートの最新に更新
```

## 調査の進め方

Homebrewドキュメントの調査は **report-kit** プラグインを使って行う。

- `/add-report` — 新しい調査タスクを `reports/` に作成
- `/report` — 調査タスクを実行

調査対象は `source/docs/` 配下の `.md` ファイル（約82ファイル）。

ワークフローの詳細は `/report` スキルの `references/report-workflow.md` を参照。

**kanban-kit** は調査以外の作業（環境整備・実装タスクなど）に使用する。

## ディレクトリ構成

- `source/` — Homebrew本体のサブモジュール
- `source/docs/` — 探索対象のHomebrewドキュメント群
- `reports/` — report-kitの調査タスクと結果（`{番号}_{タイトル}/`形式）
- `kanban/` — kanban-kitのタスクファイルと作業ログ（`{番号}_{タイトル}/`形式）
