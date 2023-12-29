## document.currentScriptの記述方法

### 1.element = document.currentScript;を記述する。
### 2.element.insertAdjacentHTML('挿入方法', '&lt;p&gt;表示させたいコード&lt;/p&gt;');のように記述する。
### 3.挿入方法における記述
    ### -beforebegin: 要素の直前に挿入します。
    ### -afterbegin: 要素の最初の子要素の前に挿入します。
    ### -beforeend: 要素の最後の子要素の後に挿入します。
    ### -afterend: 要素の直後に挿入します。
---

## HTMLの中にJavaScriptを直接記述する方法(test1.htm)

### 1.HTMLの中に&lt;script&gt;コードを記述&lt;/script&gt;のように書き込みを行う
### 2.document.write("内容");のように記述する。document.write の利用は非推奨で現在は「document.currentScript」
### 3.コードの内容によりhead要素に書かbody要素の中に書くかが分かれる
---

## 別のファイルに記述する方法(test2.htm)
### 1.&lt;script src="ファイルのパス"&gt;&lt;/script&gt;といった形でパスの指定を行う。
### 2.パスの指定は、絶対パス・相対パスどちらでも可能
### 3.指定された方には、直接書き込んだような物を記述するれば動く
---


