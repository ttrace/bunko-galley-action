# bunko-galley-action
文庫本スタイルのゲラをテキストファイルから作る、github actionsのワークフローです。

## インストールの方法
このプロジェクトの`.github/`と`package.json`を、原稿を管理しているレポジトリに含めてGithubにpushすると、[Github Actions Workflow](https://github.co.jp/features/actions)が有効になり、テキストファイルから文庫本風のPDFを作るワークフローを利用できるようになります。

## 使い方
`publish/`ディレクトリの直下に、HTMLを含む青空文庫記法のdraft.txtを配置してください。

`galley`で始まる名前のリモートタグをGithubにpushすると、PDFの生成が始まります（例：`galley20210725`や`galley初稿`など）。

分量にもよりますが、数分でGithubのリリースにタグ名を含むリリースが登録されて、PDFがダウンロードできるようになります。

## 修飾とマークアップ
マークアップと文書の修飾にはHTMLとCSSを用いてください。  
このGithub Actionsは、[VivlioStyle CLI](https://docs.vivliostyle.org/ja/vivliostyle-cli)を用いて、文庫本風のPDFを生成します。

## 集版の方法
プロジェクト中にあるファイルをかき集めるために、Gulpを利用することができます。
