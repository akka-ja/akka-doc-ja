# 翻訳ガイドライン

## Sphinx

### インストール
```
$ pip install sphinx
$ pip install 'requests[security]'
$ pip install sphinx-intl
```

### potファイルの作成

```
$ git clone https://github.com/akka-ja/akka-doc-ja.git
$ cd akka-doc-ja/rst
$ # potファイル(テンプレートファイル)の作成
$ sphinx-build.exe -c . -D pygments_style=sphinx -a -b gettext  . _build/gettext
$ # potファイルを*.poにリネームして移動
$ sphinx-intl 
```

### htmlのビルド

```
$ cd akka-doc-ja/rst
$ sphinx-build.exe -c . -D pygments_style=sphinx -a -b html  . _build/html
```

