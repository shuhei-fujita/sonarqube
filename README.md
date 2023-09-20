# SonarQube with ReactJS Project

このプロジェクトでは、ReactJSアプリケーションにSonarQubeを統合してコード品質を分析します。

## SonarQubeのセットアップ

1. SonarQubeをローカルマシンにインストールします。

```
brew install sonarqube
```

2. SonarQubeサーバーを起動します。

```
docker run -d --name sonarqube -p 9000:9000 sonarqube:latest
```

## プロジェクトのセットアップ

1. 必要な依存関係をインストールします。

```
npm install
```

2. SonarQubeのスキャナーを実行します。

```
sonar-scanner -Dsonar.login=your_token
```

## 分析結果

分析が完了すると、以下のURLでSonarQubeのダッシュボードを開いて結果を確認できます。
[http://localhost:9000/dashboard?id=your_project_key](http://localhost:9000/dashboard?id=your_project_key)

## 注意

- `.scannerwork/` ディレクトリは、`sonar-scanner`がプロジェクトの分析中に一時的に使用するディレクトリです。このディレクトリはGitリポジトリに追跡・コミットする必要はありません。

