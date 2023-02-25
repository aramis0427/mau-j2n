- git とは
- github とは
- markdown とは
- git インストール
https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB
- git セットアップ
- git の使い方
https://qiita.com/konweb/items/621722f67fdd8f86a017
    - git init
    - git add
    - git commit
    - git push

- githubアカウントの作成
https://qiita.com/ayatokura/items/9eabb7ae20752e6dc79d

- githubでリポジトリ(mau-j2n)を作る

- ローカルで使えるように、cloneする
`git clone https://github.com/aramis0427/mau-j2n`

- README.mdを作る

- 試しにcommitする
`git add *`
`git commit -m "initial commit"`
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
e-mailとnameを設定すればよさそう。
`git config --global user.email　"..........@gmail.com"`
`git config --global user.name "aramis0427"`

もう一度commitしてみる。
`git commit -m "initial commit"`
```
[main (root-commit) 5165500] initial commit
 1 file changed, 17 insertions(+)
 create mode 100644 README.md
```

`git push origin main`をやればよさそうだけど、originとは？
このサイトによると、originとしてリポジトリを紐づける必要があるhttps://qiita.com/Leonardom/items/5b94cd7e96a6fe87c6a4

`git remote add origin https://github.com/aramis0427/mau-j2n`

`git push -u origin main`

サインインが求められた
![](fig01.png)

pushできてそうなので、githubで確認する。

- 誤ってディレクトリが作られてしまったから、修正する。

![](fig02.png)

- 再度、pushする。
```
git add *
git commit -m "delete directory"
git push -u origin main
```