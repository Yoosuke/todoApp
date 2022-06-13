# todoApp

## Visual Studio Code ASP.NET Core プロジェクト生成

Visual Studio Code では ターミナルを使ってASP.NET Coreのプロジェクトを生成します。

以下のように dotnet new コマンドを利用して作成します。
```dotnet new プロジェクトの種類 -o プロジェクト名```


```
dotnet new web -o TodoApp
```

## v0.1 TodoApp のプロジェクトの確認

Visual Studio Code で開発する際に、httpsで起動するためにセキュリティ証明書を事前に作成しておきます。

以下のコマンドを実行して、証明書を発行してください。
```
dotnet dev-certs https --trust
```

続いて、以下のコマンドを実行してWeb Serverを起動してください。

```
dotnet run
```

実行したら、localhost:ポート番号でブラウザよりアクセスして確認ください。

ポート番号の確認は、```Properties/launchSettings.json```を確認してください。

```json
  "profiles": {
    "TodoApp": {
      "commandName": "Project",
      "dotnetRunMessages": true,
      "launchBrowser": true,
      "applicationUrl": "https://localhost:7045;http://localhost:5220",
      "environmentVariables": {
        "ASPNETCORE_ENVIRONMENT": "Development"
      }
    },
```

applicationUrl のところにポート番号が書かれています。
httpsとhttpの２種類があり、どちらでアクセスするかで変わってきます。確認したら、早速ブラウザでアクセスして確認してください。

ブラウザに Hello World！と表示されていたら、正常に動いてます。

## [v0.2 MVCの設定を構築](./Description/v0.2.md)


