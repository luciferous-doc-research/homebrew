# Makefileを作成してSubmodule管理をコマンド一つで実行できるようにする

## 目的
submoduleの管理をコマンド一つでできるようにしたい

## 要望
Makefileを作成し、クローン直後に実行するsubmoduleのinit用コマンドと、submoduleを最新に追従させるコマンドの二つを書いてください

## プラン
- Makefile をリポジトリルートに作成
- `make init`: git submodule init && git submodule update --init --recursive
- `make update`: git submodule update --remote --recursive
- `.PHONY` 宣言で明示

## 完了サマリー
完了日時: 2026-05-13T15:10:30+09:00

Makefile を作成し、以下のターゲットを実装しました：
- `make init`: クローン直後のサブモジュール初期化
- `make update`: サブモジュールの最新追従

検証：両コマンドとも正常に動作することを確認
