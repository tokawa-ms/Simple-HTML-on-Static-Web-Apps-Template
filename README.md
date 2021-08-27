# Simple-HTML-on-Static-Web-Apps-Template

## What's this repo?
このリポジトリは、単純な HTML ファイル と CSS ファイル、それに画像などのアセットのみで構成される静的サイトを Azure Static Web Apps でホストする際の非公式のテンプレートとして使えるように構成しました。

## How to Use
- このリポジトリをテンプレートとして新たなリポジトリを各自の GitHub アカウント配下に作成
    - このリポジトリ上部の "Use this template" ボタンをクリック
- Azure Static Web App (静的 Web アプリ) を新規作成
    - リソースグループ : 任意
    - 名前 : 任意
    - ホスティングプラン : 任意 (テスト用途なら Free で良いと思います。)
    - Azure Functions とステージングの詳細 : East Asia
    - ソース : GitHub
    - 組織 : GitHub の組織名
    - リポジトリ : このリポジトリをもとに作成したリポジトリを選択
    - 分岐 : main
    - ビルドのプリセット : Custom
    - アプリの場所 : **/src**
        - ここを設定し忘れるとコンテンツが正しく表示されません。要注意です。
    - API の場所 : 空欄
    - 出力先 : 空欄
- 「確認及び作成」でデプロイ
- GitHub Actions で自動的にデプロイされるのでしばし待機
- Azure Portal から作成した Static WebApp を開いて、基本 > URL にある URL を開く
- あとは、このリポジトリを VSCode 等で開いて HTML や CSS を変更して、リモートに反映するたびに自動で GitHub Action が走って Static Web Apps で公開されている内容がアップデートされます。
