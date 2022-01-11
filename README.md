# portfolio-with-markdown
簡単なポートフォリオページをMarkdownで作成して、GitHub PagesでWebに公開する。

## ポートフォリオとは？

- ポートフォリオとは何か、作る際に最初にやること、などを確認
  - [paizaラーニング. ITエンジニアの就活準備編2: ポートフォリオ制作 ＃01:Webページを作ろう](https://paiza.jp/works/career/primer/career2/8010)
- ポートフォリオの例
  - [Chomado’s Portfolio (ちょまど)](https://chomado.com/chomado/)
  - [この講義での作例]()
- ポートフォリオ自動作成サービスでどのような項目が記載されているかを確認
  - [LAPRAS Inc. ポートフォリオ自動作成サービス](https://lapras.com/)

## リポジトリの作成とクローン
Webページ用のリポジトリをGitHubに作成して、手軽に編集できるようにクローンして、Atomで編集する。

### リポジトリの作成

1. https://github.com を開いて、自分のアカウントでサインインする
1. 右上の + アイコンをクリックして、 New repository を選択して新しいリポジトリの作成ページを開く
1. 以下を入力してリポジトリを作成する
  - Repository name 欄に `portfolio` と入力
  - Description 欄に `ポートフォリオページ` と入力
  - Public のままでよい
  - Add a README file にチェック
  - 以上入力したら、 Create repository ボタンをクリック

### 作成したリポジトリをクローン

1. GitHub Desktop を起動する
1. File メニューから Options を選択して、自分のアカウントでサインインしているかを確認する。サインインされていなかったり、自分以外のアカウントだったら自分のアカウントでサインインする
1. 作成した portfolio リポジトリページに切り替えて、右上の Code ボタンをクリックして Open with GitHub Desktop を選択
1. ポップアップが表示されたら プログラムを選択 ボタンをクリックして、GitHubDesktop.exe が選択された状態で リンクを開く をクリック
1. GitHub Desktopの Clone a repository が表示されたら Choose... ボタンをクリックして、ドキュメント > 自分の名前のフォルダーの中の適当なフォルダーを選択して Select をクリックして Clone ボタンをクリック

### Atomで開いて編集

1. GitHub Desktop の Repository メニューをクリックして Open in Atom を選択

Atomエディターでリポジトリの内容を編集する。

1. Atomエディターの左の Project ビューから README.md を選択
1. Packages メニューから Markdown preview plus を選択。見当たらない場合は以下の手順でインストールする
  - Fileメニューから Settings を選択
  - Settingsビューから Install をクリック
  - Search packages欄に `markdown plus` と入力
  - markdown-preview-plus が一覧に表示されたら Install をクリック
  - インストールが完了したら、Atomを閉じて、開き直す
1. README.md の最後の行に `atomで追加` と入力して、Ctrl + S キーで保存

### 変更をGitHubにプル
1. Atomで変更を保存したら、GitHub Desktopに切り替える
1. Summary欄に変更点を簡潔に入力して Commit to main をクリック
1. Push origin をクリック

以上で更新完了。Webブラウザでportfolioリポジトリを開いて更新すると、先ほど追加した行が追加されていることが確認できる。

以上でポートフォリオ用のリポジトリの作成と編集環境の構築は完了である。次にマークダウン記法を練習する。

## マークダウン
GitHubやブログなど多くのサービスで採用されている作文フォーマット。記号を文章に埋め込むことで、見出しやリンク、画像の挿し込みなどをプレーンテキストで手軽に作成することができる。

- [GitHub Markdownの文法](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

上記の公式ドキュメントを参考に、README.md ページに以下の項目を追加せよ。作例は[こちら](example-markdown.md)

- 見出し1, 見出し2, 見出し3
- 太字(Bold)、斜体(Italic)、打消し線(Strikethrough)
- 埋め込みコードブロック( code block within a line )
- 独立したコードブロック( its own distinct block )
- unityroomやclusterへのリンク
- 作品のスクリーンショットなどの画像
  - 左のProjectビューのリポジトリ名を右クリックして Show in Explorer を選択すれば、作業用フォルダーが開く。スクリーンショットなどの表示したい画像はそのフォルダー内にコピーする。画像は`images`などのフォルダーを作成してまとめておくとよい
  - マークダウン内にはimgタグが使える。画像のサイズ指定をしたい場合はimgタグを使う
    - `<img src="images/sample.png" style="width: 320px">`など
- 箇条書き(Lists)
- 通し番号つきリスト(Order Lists)
- 箇条書きの字下げ(Nested Lists)
- タスクリスト
- 段落(Paragraphs)
- セパレーター
- 補足(Footnotes)
  - Atom上では表示されないので、GitHubにプッシュして確認

以上を把握していればおおよそのドキュメントは記載可能。更に以下のような記法もある。

- [高度な書式](https://docs.github.com/en/github/writing-on-github/working-with-advanced-formatting)
  - 表、折り畳み、コードブロックの拡張、添付ファイル、キーワードの利用など

その他の記法や忘れたらドキュメントを調べよう。

## マークダウンで作成したWebページをGitHub Pagesで公開する
GitHubには、Webページをホストする**GitHub Pages**という機能がある。ポートフォリオ用のリポジトリーを作成して、GitHub Pagesを使ってポートフォリオページを作成して公開する。

### GitHub Pagesとは
- [GitHub Pagesとは](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
- [GitHub Pagesの作り方](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

GitHub PagesはHTMLかマークダウン(md)ファイルをWebページとして表示できる。今回はマークダウンで作成する。

トップページは以下の優先順位で決まる。3つともない場合はトップページは File not found になる。

1. index.html
1. index.md
1. README.md

まずは既存のREADME.mdをトップページとして表示してみよう。

### GitHub Pagesを設定
1. Webブラウザで portfolio リポジトリを開く。閉じていたらGitHub DesktopのRepositoryメニューから View on GitHub を選択
1. Settings タブをクリック。見当たらない場合はWebブラウザを広げる
1. ページ左から Pages をクリック
  - Upgrade or make this repository public to enable Pages のように表示されたらリポジトリがPublicになっていないので以下の手順で公開にする
    - ページ左から Options をクリック
    - 一番下までスクロールさせて Change repository visibility 欄の右の Change visibility ボタンをクリック
    - Make public を選択
    - 空欄に、すぐ上に太字で表示されている アカウント名/リポジトリ名 をコピペするか入力すると、I understand... のボタンが押せるようになるのでクリック
    - ページ左の Pages をクリック
1. None をクリックして main を選択したら Save をクリック

以上で設定完了。青い枠内に表示されるリンクがポートフォリオページのURLなので、右クリックした新しいタブで開く。この時点では404エラーになることが多い。

**GitHub Pagesは更新がすぐには反映しない。初回は長くて10分程度、通常時でも1分は反映しないことが多い。更新してページに変化がなくても、しばらく待ってページを更新するなど様子を見ること。**

しばらく待ってREADME.mdが反映されたら準備完了。

## ポートフォリオの雛形


## テーマの変更


## 参考URL
- [paizaラーニング. ITエンジニアの就活準備編2: ポートフォリオ制作](https://paiza.jp/works/career/primer/career2)
- [Chomado’s Portfolio (ちょまど)](https://chomado.com/chomado/)
- [LAPRAS Inc. ポートフォリオ自動作成サービス](https://lapras.com/)
- [GitHub Pagesとは](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
- [GitHub Markdownの文法](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
