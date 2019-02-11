# aozorabunko_text

青空文庫( https://www.aozora.gr.jp )のサーバ内にある青空文庫形式のテキストのみをアーカイブしたものです。

個別にzipコマンドで展開したりせずにすべてのテキストが読めます。

## 動作のしくみ

https://github.com/aozorabunko/aozorabunko の中身を取得して、cardsディレクトリ内にあるzipファイルの中からtxtファイルを取り出して、同様の階層のディレクトリ内に保存しています。

動作はCircleCI上で行っており、1日1回バッチで動作します。

なお、zip内のテキストファイルはタイトルに合わせたファイル名が命名されているのですが、このレポジトリではzipファイル名に合わせたファイル名にしています。
例えば、`cards/000005/files/53194_ruby_44732.zip`内のテキストなら`cards/000005/files/53194_ruby_44732/53194_ruby_44732.txt`というパスになります。
これは元のテキストファイル名は「作家別作品一覧CSV」などにも書かれておらず、確認するにはzipファイルの中身を見ないといけないためです。

## 最新版の取得方法

ふつうのgithub repoなので、git pullで持ってきてもらえばいいのですが、履歴不要で最新版だけ欲しい場合は以下のコマンドの方が早いはずです。

```console
$ git clone --depth 1 https://github.com/takahashim/aozorabunko_text.git
```

zipで欲しい場合には、緑色の「Clone or download」ボタンから「Download ZIP」でダウンロードできます。

なお、cardsディレクトリ以外は無視してください。

## 権利関係

cardsディレクトリ内のファイルについては、[「青空文庫収録ファイルの取り扱い規準」](https://www.aozora.gr.jp/guide/kijyunn.html)の元でご利用ください。

著作権保護期間が終了しておらず、クリエイティブ・コモンズ・ライセンス等による許諾の元で再配布されているファイルも含まれています。ご注意ください。