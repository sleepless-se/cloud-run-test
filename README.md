# Google Cloud Run auto deploy example

This is example for auto deploy for Google Cloud Run with GitHub.

1. [Enable Cloud Run](https://console.cloud.google.com/run)
1. [Enable Cloud Registry](https://console.cloud.google.com/gcr/images/)
1. [Enable Cloud Run Administrator Status](https://console.cloud.google.com/cloud-build/settings/service-account)
1. [Connect your GitHub repository.Then add trigger](https://console.cloud.google.com/cloud-build/triggers)
1. Push any change to git branch! It's build automatically `build` and `deploy` on Cloud Run!

You can change Cloud Run setting in `cloudbuild.yaml`.

If you want to change service name, replace `hello` to your service name.

Default options

* --allow-unauthenticated (Allow from pulic access)
* --region us-central1 (select [region](https://cloud.google.com/compute/docs/regions-zones))
* --memory 1024Mi (setting memory size. 256Mi 512Mi 2028Mi etc)
* --image gcr.io/$PROJECT_ID/hello (select run container)
* --platform managed (managed is run on Cloud Run)


## Google Cloud Run自動デプロイの例

これは、GitHubを使用したGoogle Cloud Runの自動デプロイの例です。

1. [Cloud Runを有効にする]（https://console.cloud.google.com/run）
1. [Cloud Registryを有効にする]（https://console.cloud.google.com/gcr/images/）
1. [Cloud Run管理者ステータスを有効にする]（https://console.cloud.google.com/cloud-build/settings/service-account）
1. [GitHubリポジトリを接続します。次にトリガーを追加します]（https://console.cloud.google.com/cloud-build/triggers）
1. 何か変更をgitブランチにプッシュします！ Cloud Runで自動的に「ビルド」および「デプロイ」されます。

Cloud Runの設定は、 `cloudbuild.yaml`で変更できます。

サービス名を変更する場合は、 `hello`をサービス名に置き換えます。

初期設定

* --allow-unauthenticated (外部アクセスを許可する)
* --region us-central1 ([リージョン](https://cloud.google.com/compute/docs/regions-zones)を選択)
* --memory 1024Mi (メモリサイズ設定 256Mi 512Mi 2028Mi)
* --image gcr.io/$PROJECT_ID/hello (コンテナを選択)
* --platform managed (managedはCloud Runで実行)
