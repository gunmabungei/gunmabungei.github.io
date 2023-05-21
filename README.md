# これはなに？
群馬高専文芸部のGitHubPagesです。
hugoを使っているので簡単にセットアップできると思います。  
# 使いかた
記事を  
`hugo new post/{記事名}`  
で追加します。  
書き終わったら、  
`git add .`  
`git commit -m "〇〇を追加しました"`  
`git push origin main`  
を実行します。

## 執筆時の注意
一番上の「---」で囲まれているセクションで、作品のタイトルと作者名、ジャンルを設定してください。  
設定の仕方はほかのposts以下の作品のファイルを参照してください。  

## マークダウンについて
マークダウンは文章の記法の一つで、簡単に文字の装飾ができます。  
マークダウンの書き方は調べればいくらでも出てきますが、ここで小説で応用出来そうな記法を書いておきます。  
1. 水平線  
  \---  
  と書くことで水平線を引くことができます。
  ---
2. ルビ  
  \<ruby>漢字\<rp>（\</rp>\<rt>かんじ\</rt>\<rp>）\</rp>\</ruby>  
  と書くことでルビを振ることができます(出来ないときもある)  
  <ruby>漢字<rp>（</rp><rt>かんじ</rt><rp>）</rp></ruby>

  必要な表現が出てきたら適宜学んでください。
# セットアップ方法
## 使うもの
hugo  
git  
## hugoインストール
ここ(https://gohugo.io/installation/)を観ながらがんばってください。
### Windowsの場合
パーッケージマネージャーからインストールします  
https://gohugo.io/installation/windows/  
### Linuxの場合  
パッケージマネージャーからインストールします。  
https://gohugo.io/installation/linux/  
私は[HomeBrew](https://brew.sh/index_ja)からやりました。
## gitインストール
https://gitforwindows.org/ からインストーラーをDLして、デフォルトの設定でインストールしてください  
gitについては電算部の本棚にある「わかばちゃんと学ぶGit使い方入門」とかを読んだら良いと思います  
多分電算部は貸してくれます
## 環境構築していく
適当なディレクトリで  
`git clone https://github.com/gunmabungei/gunmabungei.github.io.git`  
を実行します。  
クローンしたフォルダに移動します  
`cd gunmabungei.github.io`  
このままでは多分バグるので  
`git submodule deinit -f themes/PaperMod`  
`git add .gitmodules`  
`git rm --cached themes/beautifulhugo`  
の２つのコマンドを実行した後、  
`git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`  
`git submodule update --init --recursive `  
を実行します
ここまで出来たら、  
`hugo server -D`  
を実行してみましょう。-Dは下書き記事も表示するという意味です。  
![/static/screenshot.35.jpg](/static/screenshot.35.jpg)  
このように表示されたら示されてるリンクに飛んでローカルサーバーが動いていることを確認してください。  
この時点で何らかのエラーが出たらどこかで間違えています。  
頑張ってください。ちなみにChatGPTにエラーコード投げると解説してくれます。  