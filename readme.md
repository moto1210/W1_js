## document.currentScriptの記述方法

### 1. element = document.currentScript;を記述する。
### 2. element.insertAdjacentHTML('挿入方法', '&lt;p&gt;表示させたいコード&lt;/p&gt;');のように記述する。
### 3. 挿入方法における記述
    * beforebegin: 要素の直前に挿入します。
    * afterbegin: 要素の最初の子要素の前に挿入します。
    * beforeend: 要素の最後の子要素の後に挿入します。
    * afterend: 要素の直後に挿入します。
---

## HTMLの中にJavaScriptを直接記述する方法(test1.htm)

### 1. HTMLの中に&lt;script&gt;コードを記述&lt;/script&gt;のように書き込みを行う
### 2. document.write("内容");のように記述する。document.write の利用は非推奨で現在は「document.currentScript」
### 3. コードの内容によりhead要素に書かbody要素の中に書くかが分かれる
---

## 別のファイルに記述する方法(test2.htm)
### 1. &lt;script src="ファイルのパス"&gt;&lt;/script&gt;といった形でパスの指定を行う。
### 2. パスの指定は、絶対パス・相対パスどちらでも可能
### 3. 指定された方には、直接書き込んだような物を記述するれば動く
---

## ブラウザのJavaScriptが無効の時に別のコンテンツを表示する(test3.htm)
### 1. &lt;noscript&gt;HTML記述&lt;/noscript&gt;記述の時にjavascriptが適応されていない旨を記述する。
### 2. 記述されていない場合はHTML文が出力される。
### 3. 記述方法はHTMLで書く
---

## JavaScriptのコードをHTMLファイルのどこに記述するべきなのか(test4.htm)
### 1. 特に記述することなし
---

## JavaScriptの外部ファイルを非同期で読み込む(async属性,defer属性)(test5.htm)
### 1. &lt;scriptでdefer&gt; defer src="./jscode.js"&gt;&lt;/script&gt;でdefer属性を設定する。
### 2. 通常
    * HTMLをダウンロード
    * パースを開始する
    * ScriptタグのJavascriptが記述された外部ファイルを取り込む
    * その際パースは一旦ストップする
    * コードが実行された後パースを再開
### 3. defer属性
    * ScriptタグのJavascriptが記述された外部ファイルを取り込む
    * Javascriptファイルを読み込んでいる間もパースし続ける
    * 読み込みにかかる時間が原因でHTMLが遅延することはなくなる
### 4. &lt:script async src="./jscode.js"&gt;&lt;/script&gt;でasync属性を設定する
### 5. async属性
    * パースを開始する
    * パース方法自体はdefer属性と変わらない
    * javascriptファイルを読み込み完了後パースを停止しコードを実行する
    * コードが実行された後パースを再開
### 6. defer属性とasync属性の違いとしては、defer属性が設定されているscriptタグが複数ある場合、HTMLに記述された順にコードを実行することが決まっているので、順に実行しなければ行けないコードを記述する場合に便利で、読み込み完了後すぐに実行されるので、例えばアクセス解析用のコードなどできる限り早く実行したい場合に便利という違いがある。
---

## HTMLファイルに記述されたJavaScriptのコードからログをコンソールへ出力する(test6.htm)
### 1. console.log(obj [, obj, ...])を使用する
---

## JavaScriptのコードを記述する上での基本ルール(test7.htm)
### 1. 基本的にはpyhtonなどと変わらない
---

## コメントを記述する(test.js)
### 1. １行「//」
### 2. １行または複数行「/**/」
### 3. HTMLのコメントは「<!-- コメント -->」
---

## JavaScriptの予約語
### 1. 予約語とは、ifなどの予め意味を持っているもの
---

## JavaScriptのデータ型(test7.htm)
### 1. プリミティブ型とオブジェクト型がある
### 2. プリミティブ型
    * 数値 (10,3.14)
    * 長整数 ※ ES2020～ 長整数型は数値型では扱えない範囲の非常に大きな整数を扱うことができるデータ型。typeはbigint
    * 文字列 文字列型は 0 文字以上の文字の集まり
    * 論理値 ture または false
    * undefined undefined は特殊な値のひとつで値が存在していことをあらわし値がまだ未定義であることを示す undefined 
    * null null も特殊な値のひとつで値が存在していないこと
    * シンボル 作成するたびに既に作成済みのシンボルと異なるユニークな値
### 3. オブジェクト型
    * Object(オブジェクト)
    * Array(配列)
    * Function(関数)
    * StringやNumberなどのラッパーオブジェクト
    * Date(日時)
    * RegExp(正規表現)
    * JSON

