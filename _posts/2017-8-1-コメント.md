---
layout: post
comments: true
title:  "Jekyll-nowで作ったブログにDisqusでコメント機能をつける！"
date:   2017-08-01 
---

当ブログもJekyll-nowで作成されていますが、Jekyll-nowで作られたページは静的ページであるために  
コメントの機能がデフォルトで付いていません。

そこで、Disqusという外部のサービスを使ってコメント機能の実装を行おうと思います。  
Disqusとは、コメント機能を提供しているクラウドサービスで自分のWEBサイトやブログにコメント入力機能を簡単に追加することが出来ます。
コメントが付いた際に通知が届いたり、画像や動画もコメントにできるサービスです。  
無料のサービスで、スパムフィルタも強力なのもgood。

##導入方法
###Disqusにユーザ登録
[Disqus](https://disqus.com/)のサイトへ行き、右上の「Get Started」ボタンを押してアカウント登録をしましょう。  
登録が完了したらメールアドレスに確認メールが届くのでそちらのチェックも忘れずに！  
![サインアップ画面](http://i.imgur.com/B1qIi9O.png)

###Disqusの設定をしよう
ログインしたら右上の歯車マークをクリックして、出て来たメニューの中から「settings」をクリック

![ログイン後画面](http://i.imgur.com/pMeqUaO.png)

アカウントの情報が記載されているページにアクセスしたらさらに右上の歯車マークをクリックし、出て来たメニューから  
「Add Disqus To Site」をクリック。  
Engage your Audienceといったタイトルのページが表示されたら、ページの一番下までスクロールし、「GET STARTED」をクリック。
次のページで、「I Want to install Disqus on my site」をクリック。

Create new siteのページが表示されたら、画面に従って必要な情報を設定していきます。

![サイト登録](http://i.imgur.com/t53uux4.png) 

Websiteには自分のサイトの名前を。  
Categoryには自分のサイトはどのようなカテゴリに属するかをリストから選択してください。  
Languageには言語をリストから選んで下さい。デフォルトでJapaneseになっていたらここを弄る必要はありません。  
設定ができたら「Create site」をクリック！


サイトができたら次はプランの選択画面が表示されますが、今回は無料の「Basic」プランで進めましょう。  
「Continue Basic」をクリック。
次にプラットフォームを聞かれるので、右中央にあるJekyllをクリック!
![プラットフォーム選択](http://i.imgur.com/ss3Gs6h.png)  


すると、具体的な実装方法が記されたページが出て来ます。
このページの①のlayout~と記載されている部分と、②の「Universal Embed Code」をクリックし、表示されたページの
①のコードをメモに控えておきましょう。
![実装方法1](http://i.imgur.com/jxmrwCE.png) 
![実装方法2](http://i.imgur.com/WVKrUhX.png) 

控えたらページを戻って、「Configure」をクリック、するとサイトのURL等を入力するフォーム画面が表示されますので
必要事項を記入しましょう。
記入が完了したら「Complete Setup」をクリックして、これでDisqus側での設定は完了です。　　

###記事にコメント機能を付けよう。
次に自分のgithubに戻って、自分のgithub.ioリポジトリを見て、_layoutsの中のpost.htmlを編集します。  
ここで、先ほど控えたUniversalEmbedCodeの①のコードをここに記入します。　　  
記入例を以下に示します。
![記入例](http://i.imgur.com/GZOjhi1.png) 

記入ができたらcommitしましょう。  
あとは_Posts内に記事を作る際に、commntsをtrueにすることで記事にコメント機能が追加されます！

![記入例](http://i.imgur.com/99KJzCa.png) 

![記入例](http://i.imgur.com/W7YpGaZ.png) 

こんな感じで出て来ます！  
初期だとReadmoreをクリックした際にコメントフォームが出て来ますね！

このコメントフォームはDisqusに登録していたり、  
各種SNSのアカウントを持つ人であればコメントが出来るようになっています。

###コメント機能実装完了！
これでJekyll-nowで作られたブログにコメント機能を実装することができました！  
動画や画像も表示できたりするので、色々試して見て下さい！

