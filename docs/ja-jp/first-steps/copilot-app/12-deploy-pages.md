---
title: "レッスン 12 - GitHub Pages でサイトを公開する"
description: "GitHub Copilot app で Pages ワークフローを構成し、プルリクエストをレビューして、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Space Quiz を GitHub Pages にデプロイして、誰でも利用できるようにします。Copilot はワークフローの準備とデプロイを支援しますが、変更をレビューし、サイトが公開されたことを確認するのは自分の役割です。

このレッスンでは、次のことを行います。

- Copilot に GitHub Pages のデプロイ構成を依頼します。
- マージする前にワークフローとプルリクエストをレビューします。
- デプロイを確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、簡単に試せるようにする必要があります。GitHub Pages で単一ファイルのサイトを公開すると、サーバーやランタイム依存関係を追加せずに、公開 URL から利用できるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
このリポジトリで GitHub Pages を有効にします。必要に応じて Web サイトをビルドし、GitHub Pages にデプロイする GitHub Actions ワークフローを作成します。README がまだない場合は、アプリの説明とローカルでの実行方法を記載した README を追加します。これらの変更を含むプルリクエストを作成し、必須チェックが成功した後にマージします。デプロイが成功するまで監視し、公開された Web サイトの最終 URL を報告します。Pages の有効化やマージの権限がない場合は、承認または実行が必要な内容を正確に伝えます。サイトが公開されるまで成功したと報告しないでください。
```

![3 段階の図: マージ済みの space-quiz プルリクエスト、Build website・Upload artifact・Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントにプルリクエストの作成とマージ、およびリポジトリの Pages 設定変更を依頼します。続行する前に、diff、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローをレビューしてデプロイを確認する

1. リポジトリに README がない場合に限り、README が追加されていることを確認します。
2. ワークフローのビルドとデプロイの手順を含め、プルリクエストの変更をレビューします。
3. 必須のプルリクエストチェックが成功してからマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages の有効化やプルリクエストのマージを実行できない場合は、提示された具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまで、作業を完了したと判断しないでください。

## まとめと次のステップ

エージェントの報告だけに頼らず、デプロイを確認したうえで Space Quiz を公開できました。続けて[レッスン 13: レビューと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
