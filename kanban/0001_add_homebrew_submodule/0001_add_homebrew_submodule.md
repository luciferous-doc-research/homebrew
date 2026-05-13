# Homebrewをサブモジュールとして追加

## 目的
参照できるようにしたい

## 要望
`git@github.com:Homebrew/brew.git` を `source` というディレクトリにサブモジュールとして追加してください

## プラン
1. `git submodule add git@github.com:Homebrew/brew.git source` コマンドを実行
2. `.gitmodules` ファイルの自動生成と `source/` ディレクトリの作成を確認
3. `git status` と `git submodule status` で変更内容を検証
4. コミット対象となった `.gitmodules` と `source/` を確認

## 完了サマリー
完了日時：2026-05-13T20:36:00+09:00

Homebrew リポジトリをサブモジュールとして正常に追加しました。

**実施内容**：
- `git submodule add git@github.com:Homebrew/brew.git source` を実行
- `.gitmodules` ファイルが自動生成され、サブモジュール設定が記録された
- `source/` ディレクトリにクローンが完了（Homebrew 2.7.4-23995 相当）
- 変更はステージング済み（`.gitmodules` と `source/` が Changes to be committed に表示）

**確認完了**：
- `git submodule status` で `e7b7e19556cc6714cc2feb472c21fde63d8e2a16 source (2.7.4-23995-ge7b7e19556)` が表示される
- `source/` ディレクトリ内にブリューリポジトリのファイルが存在することを確認
- `.gitmodules` に正しくサブモジュール設定が記録されていることを確認

詳細なログは `log.md` を参照
