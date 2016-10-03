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
$ sphinx-build -b gettext . _build/gettext
$ # potファイルを*.poにリネームして移動
$ sphinx-intl update -p _build/gettext -l ja
```

### htmlのビルド

```
$ cd akka-doc-ja/rst
$ sphinx-build -c . -D pygments_style=sphinx -D language='ja' -a -b html . _build/html
```

