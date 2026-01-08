# jawiki-aisearch-example

## 概要

Microsoft Fabricのノートブックで動作する、日本語Wikipedia全文を加工するデモです。一般的なアプリケーションではなく、サンプルノートブックを置いたレポジトリです。加工結果をもとに、Azure AI Searchへデータ登録するためのJSONファイルを出力できます。

## ノートブック

[download_jawiki_latest_pages_articles.ipynb](example/download_jawiki_latest_pages_articles.ipynb)

## ノートブックで行う処理

ノートブックを見ながら確認できる主な処理は以下のとおりです。

- 日本語Wikipediaのダンプデータを読み込み、不要な要素を取り除いてテキスト化
- 記事本文の正規化（見出しやリンクの処理、余計な記号の整理など）
- AI Searchに登録しやすい単位への分割と、メタデータ（タイトル、URLなど）の付与
- 出力先に合わせたJSON形式への変換と保存

ノートブックを順に実行していくと、どのセルでどのような加工が行われるかを確認しながら、最終的なJSON出力まで追える構成です。

## 事前準備

動作には、Fabric上でノートブック用のEnvironmentを作成し、`mwparserfromhell`を追加する必要があります。
