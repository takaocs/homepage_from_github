# homepage_from_github
GitHubからリポジトリを作成し開発を進める


## 【概要】

作業はAさん、Bさん、Cさんの3人で行う。リーダーはAさんとする。  
作業担当は以下の通り。

* Aさん: ナビゲーションバー作成を担当。リポジトリ名は「navigation」。
* Bさん: コンテンツ作成を担当。リポジトリ名は「contents」。
* Cさん: フッター作成を担当。リポジトリ名は「footer」。


## 【GitHubから新規リポジトリを作成】

作業者: Aさん

GitHubからリポジトリを作成。  
統合ブランチとして「develop」ブランチもGitHubから作成しておく。


## 【Aさんの作業】

作業者: Aさん

「develop」ブランチから「navigation」ブランチを作成。  
「navigation」ブランチでナビゲーションバーを作成し、GitHubへプッシュするまでの作業を行う。  
なお、Bさん・Cさんはまだ作業を開始しない状態である。

### 手順1: 手元の開発環境(Mac等)にGitHubで作成したリポジトリを持ってくる

まずは「**git clone**」コマンドでGitHubで作成したリポジトリを手元の開発環境に持ってくることから。  
適当な場所に移動して以下のコマンドを実行。

    git clone git@github.com:ユーザ名/リポジトリ名.git

「**git branch -a**」コマンドでGitHubで作成したリポジトリも含め確認できるので、cloneしたら一度確認しておく。

    git branch -a
        * master
          remotes/origin/HEAD -> origin/master
          remotes/origin/develop
          remotes/origin/master

### 手順2: GitHubの「develop」ブランチをチェックアウトする

続けて以下のコマンドを実行する。  
なお、ブランチ名はわかりやすいように同じにする。

    git checkout -b develop origin/develop

「git branch -a」で確認。アスタリスクは「develop」の横にある。

    git branch -a
          master
        * develop
          remotes/origin/HEAD -> origin/master
          remotes/origin/develop
          remotes/origin/master

### 手順3: 「navigation」ブランチを作成し、GitHubにpushする

次に「navigation」ブランチを作成し、GitHubにpushする。

    git checkout -b navigation
    git push -u origin navigation
