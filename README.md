# Git、GitHub についてのリサーチと実践

## 課題1 Git とは
分散型バージョン管理システムのこと。言い換えれば、ファイルのバージョン管理が簡単にできるツールである。

Gitを使ってファイルを管理すると、コンピューター上でファイルの編集履歴を管理できるので、編集前のファイルを残したまま、新しく編集したファイルを保存することができる。なので古いバージョンから新しいバージョンまでの管理が簡単になる。

プログラマーにとっては、多くのコードを編集した上で何か不具合が起きたときに、元のバージョンへ戻すことは日常茶飯事である。しかし、ひとつひとつコードの編集の度に古いバージョンの確認、作業を加えるようなことをすれば、時間はかかるしミスも増えてしまう。そういった作業を無駄なく、効率的に行うことができるのがGitの強みである。

### 参考文献
- https://tcd-theme.com/2019/12/what-is-git.html

## 課題2 GitHub とは
世界中の人々がプログラムコードやデザインデータを保存・公開できるソースコード管理サービスのこと。Gitはツールの名前で、GitHubはWebサービスの名前である。

GitHub上で、エンジニア各々が公開用のプログラムをアップして自分以外のエンジニアに共有したり、その後、履歴を残しながら更新したり、自分以外のエンジニアも修正を加えるということができる。

GitHubを使うためにはアカウントを作成する必要があるが、GitHubは企業や個人を問わずにベースとなる部分は無料で使うことができる。また、GitHubに作成されたリポジトリ（保存するスペース）は、基本的にすべて公開することになるが、指定したユーザーだけがアクセスできるプライベートリポジトリを作成することもできる。

### 参考文献
- https://www.modis.co.jp/candidate/insight/column_30

## 課題3 markdown とは
markdownは文章構造を明示して書くことができる軽量マークアップ言語である。プレーンテキストで書いた文書からHTMLを生成するために、ジョン・グルーバーによって開発された。HTMLだけでなくパワーポイントやLaTeXなどに変換するソフトウェアも開発されている。

Stack Overflow、Redditといった掲示板サービスを筆頭に広く利用されている。サービスごとで基本の機能は共通している一方、独自の"方言"が存在する。そのため書き方がサービスごとに異なることで混乱を引き起こしたり、あるサービスでしか使えない機能があって不便であったりする。

基本的に使える機能として、見出し・文字装飾・URLリンク・引用・コードブロック・文字色・チェックリスト・箇条書きリスト・番号付きリスト・表・図の挿入・注釈・数式・絵文字がある。どれも文頭に記号を付け加えたり、文章を記号で囲んだりをするだけのため、プレーンテキストを読んでも可読性が高いという特徴がある。  

### 参考文献
- https://www.markdown.jp/what-is-markdown/  
- https://notepm.jp/help/how-to-markdown  
- https://ja.wikipedia.org/wiki/Markdown

## 作業ログ
- Git インストール
  
  ***参考文献　https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB***

- Git セットアップ

- Git の使い方
  参考文献を見て、使い方を学ぶ
  - `git init`
    - ディレクトリのgitの初期設定を行う
    - gitを使うなら必ず行う必要がある
  - `git add {ファイル名}`  
    - gitで記録をするファイルを追加する
    - `*`ですべてのファイルを追加できる
  - `git commit -m "メッセージ"`
    - commit をする
    - `-m` を使うことでメッセージを書き入れる
  - `git push origin main`
    - origin リポジトリのmain ブランチにpushする

  ***参考文献　https://qiita.com/konweb/items/621722f67fdd8f86a017***

- GitHubアカウントの作成

  [GitHub](https://GitHub.co.jp/)のHPでアカウント作成

  ***参考文献　https://qiita.com/ayatokura/items/9eabb7ae20752e6dc79d***

- GitHubでリポジトリ(mau-j2n)を作る

  左のメニューのnewから選択

  パブリックリポジトリにして作成

- ローカルでREADME.mdを作る

  課題内容の一部を記述

- 試しにcommit、pushする

  - `git add *`

  - `git commit -m "initial commit"`

    commitしようとしたらエラーが出た

    ```
    Author identity unknown

    *** Please tell me who you are.

    Run

      git config --global user.email "you@example.com"
      git config --global user.name "Your Name"       

    to set your account's default identity.
    Omit --global to set the identity only in this repository.

    fatal: unable to auto-detect email address (got 'solar@DESKTOP-3V9BKLL.(none)')
    ```

    > Run\
    \
    git config --global user.email "you@example.com" \
    git config --global user.name "Your Name"

    とあるから、e-mailとnameを設定すればよさそう。エラーコード通りに実行する
    
    `git config --global user.email　"..........@gmail.com"`
    
    `git config --global user.name "aramis0427"`

    もう一度commitしてみる。

    `git commit -m "initial commit"`

    ```
    [main (root-commit) 5165500] initial commit
    1 file changed, 17 insertions(+)
    create mode 100644 README.md
    ```

    commit が成功した

  - `git push origin main`をやればよさそうだが、originとは？
  
    [このサイト](https://qiita.com/Leonardom/items/5b94cd7e96a6fe87c6a4)によると、originとしてリポジトリを紐づける必要がある 

    - `git remote add origin https://GitHub.com/aramis0427/mau-j2n`

      これでリポジトリを紐づけられた

  - `git push -u origin main`

    サインインが求められた
    
    ![](fig01.png)

    ログインして解決

- pushできてそうなので、GitHubで確認する。

- 誤ってディレクトリが作られてしまったから、修正する。

![](fig02.png)

- 再度、pushする。

```
git add *
git commit -m "delete directory"
git push -u origin main
```

修正できた

![](fig03.png)

- 課題1~3を追記して、再度pushする。
```
git add *
git commit -m "1st edit"
git push -u origin main
```