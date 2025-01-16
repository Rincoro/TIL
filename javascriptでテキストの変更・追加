# javascriptでテキストの変更・追加

エンジニア転職目指しているりんころです！今回はJavaScriptでの基本的な構文や、使い方を復習します。

既存の表記を条件によって書き換える場面が多くあります。

（例）ボタンをクリックしたときに、そのボタンのテキストを「送信」から「送信済み」に変更するなど…。

**⭐️こういったテキストの変更・更新をするときは、『textContent』を使うといいんです！**

### **手順**

**①** 変更したいHTML要素を識別します。通常、id 属性や class 属性を使用して識別させます。（つまり変更させたい部分にidやclassづけする）

**②** 要素の取得: JavaScriptを使って、特定の要素（idかclass）を取得します。これには、document.getElementById() や document.querySelector() メソッドを使用します。

**③** textContent プロパティを使用して、テキスト内容を変更します。

```html
<p id="idA"> Hello! </P>

<script>
document.querySelector('#idA').textContent = "Good Morning!";
</script>
```

以上の例のように、id=”idA”の要素内のテキストをdocument.querySelectorで取得して、textContent で上書きします。

## innerHTMLとどう違う？

よくHTMLのテキストを扱うもので、innerHTMLがありますが、違いがわからんかったので調べてみました。

ざっくりいうとこんな感じです…

### innerHTMLは、要素に含まれるすべてのテキストを扱う（htmlタグも含む!!）

です！

実例

```html
<p id="idA"> Hello! </P>

<script>
  const text =document.querySelector('#idA');
  console.log("text.innerHTML=${text.innerHTML}");
  console.log("text.textContent=${text.textContent}");
  
  // consoleの出力結果
//text.innerHTML
<p id="idA"> Hello! </P>
  
//text.textContent
 Hello!

</script>
```

この様に、innerHTMLは要素内に含まれるタグも全て取得するので、既存のHTMLのタグに影響を与える可能性があります。テキストだけ変えたければtextContentがベターかもです☺️
