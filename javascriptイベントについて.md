# javascriptイベントについて

現在webエンジニア目指して学習中のりんころです！

javascriptの理解度がやばいと感じたので基礎から学び直してます！

JavaScriptで開発する際に絶対つかうイベントについて基礎から復習します！！

## イベントって何？

webページを開いているとき、キーボードを操作したり、スクロールしたり、ボタンをクリックしたするなどjavascriptの動作のきっかけとなる事象がユーザーの動きによって、発生しています。**この事象をイベントと言います！**ブラウザはイベントが起きてないか常に監視していて、javascriptでは特定のイベントが発生した時に、予定していた動作を実行するよう定義（予約）することができます！

## イベントの定義方法

どんな感じでイベントを予め定義（予約）すればいいのかという話ですが、次の例を使って説明します！

```html

<body>
<button id="btn" class="bg-blue-500 text-white font-bold py-2 px-4 rounded">送信</button>
</body>

<script>
//定数btnにid="btn"を持つタグ内の要素を取得しています。 
const btn = document.querySelector('#btn'); 
btn.addEventListener('click',() => {
if(btn.textContent === '送信'){
btn.textContent = '送信済み';
}else{
btn.textContent = '送信';
}
});

</script>
```

上記のコードを解説すると、

まず、**addEventListener**を使ってイベントを予約しています。今回は、定数btnに、clickイベントが発生した時に、どのような処理をするのか？という部分を定義しています。

じゃあどこが処理の具体的な内容なの？って話なんですけど

下の青色マーカー部分です。

```jsx
btn.addEventListener('click',() => {
if(btn.textContent === '送信'){
btn.textContent = '送信済み';
}else{
btn.textContent = '送信';
}
});
```

この場合、clickイベントが発生した時、if文を使って、定数btn内のテキストの内容によってボタンの表示内容を切り替えるようにしています。

このようにJavaScriptでは、イベントを使ってwebページを動的なものにすることが出来ます！
