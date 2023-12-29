#HTMLの中にJavaScriptを直接記述する方法(test1.htm)
1.HTMLの中に<script>コードを記述</script>のように書き込みを行う
2.document.write("内容");のように記述する。document.write の利用は非推奨で現在は「document.currentScript」
3.コードの内容によりhead要素に書かbody要素の中に書くかが分かれる

#別のファイルに記述する方法(test2.htm)
1.<script src="ファイルのパス"></script>といった形でパスの指定を行う。
2.パスの指定は、絶対パス・相対パスどちらでも可能
3.指定された方には、直接書き込んだような物を記述するれば動く
4.
