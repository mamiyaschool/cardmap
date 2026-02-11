# GitHubへのアップロード手順

## 1. 初回コミット（まだの場合）

以下のコマンドでコミットしてください：

```bash
cd "/Users/daisukemamiya/Documents/手作りプログラム/手書きメモ"
git commit -m "Initial commit: CardMap application"
```

## 2. GitHubリポジトリの作成

1. GitHubにログインして、https://github.com/new にアクセス
2. リポジトリ名を `cardmap` に設定
3. オーナーを `mamiyaschool` に設定
4. 説明（オプション）: "カードマップ - 手書きメモアプリケーション"
5. **Public** または **Private** を選択
6. **「Initialize this repository with a README」のチェックを外す**（既にREADME.mdがあるため）
7. 「Create repository」をクリック

## 3. リモートリポジトリの追加とプッシュ

GitHubでリポジトリを作成した後、以下のコマンドを実行してください：

```bash
cd "/Users/daisukemamiya/Documents/手作りプログラム/手書きメモ"

# リモートリポジトリを追加（URLはGitHubで作成したリポジトリのURLに置き換えてください）
git remote add origin https://github.com/mamiyaschool/cardmap.git

# またはSSHを使用する場合
# git remote add origin git@github.com:mamiyaschool/cardmap.git

# メインブランチをmainに変更（GitHubのデフォルトに合わせる）
git branch -M main

# リモートリポジトリにプッシュ
git push -u origin main
```

## 4. 認証について

初回プッシュ時に認証が求められる場合があります：

- **HTTPSの場合**: GitHubのPersonal Access Tokenが必要です
  - 設定: https://github.com/settings/tokens
  - 権限: `repo` を選択
  
- **SSHの場合**: SSH鍵をGitHubに登録する必要があります
  - 設定: https://github.com/settings/keys

## 完了！

これで、https://github.com/mamiyaschool/cardmap にコードがアップロードされます。
