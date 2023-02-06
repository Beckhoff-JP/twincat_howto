# TwinCAT Howto

## 構成

- docs
  - contents : コンテンツ
  - faq : FAQ ページ
  - manual : Manual ページ
- mkdocs.yml : サイトの構成ファイル

## 記事作成の環境構築

### Repository の作成

[Beckhoff-JP/twincat_howto](https://github.com/Beckhoff-JP/twincat_howto)  
上記リンクから **fork** を個人アカウントに作成する。  
fork された Repository は **Beckhoff-JP/twincat_howto** に対する作業エリアになります。

### fork された Repository を Clone する

作業を行いたいディレクトリに fork した Repository の Clone を作成する。  
実作業は個々で行う。

## コンテンツ追加手順

### Redmine にチケットを登録する

[Redmine](https://beckhoff.cloud.redmine.jp/projects/cutomer_support/issues)  
上記リンクから作成するコンテンツのチケットを作成する。

### 記事の作成

docs > Contents 直下に作成した**チケット番号**のディレクトリを作成する。  
内部の構成ディレクトリは極力下記で設定することを推奨です。  
(既に作成済み等であればそのままでもよい。)

- assets : 画像保存フォルダ
- index.md : 記事本文

### 記事のアップロード

作成したデータを Push して PullRequest を作成してください。  
PullRequest は **Beckhoff-JP/twincat_howto** に申請されます。  
PullRequest が Merge されると自動的に **Twincat Howto** に反映されます。
