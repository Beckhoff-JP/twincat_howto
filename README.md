# TwinCAT Howto

## 構成

- docs
  - contents : コンテンツ
  - faq : FAQ ページ
  - manual : Manual ページ
- mkdocs.yml : サイトの構成ファイル

## 記事作成の環境構築

1. Python環境と、リポジトリ中にある `requirements.txt` パッケージをインストールしてください。

    ```shell
    $ pip install -r requirements.txt
    ```

2.  以下のコマンドを発行するとローカルコンピュータ上にWEBサーバが起動し、 `http://localhost:8000` にアクセスすることで作成したMarkdown文書をプレビューすることができます。

    ```shell
    $ mkdocs serve
    ```

3. 次項の記事の作成方法に記載した手順で文書を作成し、プレビューで問題ない事をご確認の上、プルリクエストを送付してください。

## 記事の作成

1. 本リポジトリ [Beckhoff-JP/twincat_howto](https://github.com/Beckhoff-JP/twincat_howto) から **fork** してください。

2. `docs/Contents` 以下にサブディレクトリを作成いただき、下記の構成のMarkdown文書でご記入ください。Markdown書式は　[mkdocs-material](https://squidfunk.github.io/mkdocs-material/) に準じてご記載ください。
サブディレクトリ名はBAJP社員が作成する記事については内部管理番号となっていますが、一般の方は特に規約はございません。ユニークな文字を使ってください。

   - assets : 画像保存フォルダ
   - index.md : 記事本文

!!! warning
    * Markdownの記述方式を拡張するため plugin の追加が必要な場合、次のファイルにプラグインの定義を漏れなく行ってください。
      * requirements.txt
      * .github/workflows/ci.yml
    * 記事の単位はアトミックな単位（これ以上分解できない程度）で作成願います。文書構成は次の手順に示す`nav`ツリーで定義します。これにより情報の再利用性を高められるようにします。

3. ルートディレクトリにある `mkdocs.yml` を編集し、`nav` ツリーに作成した文書に対するリンクを登録してください。
