# argocd の練習
## argocd のインストール
`helmfile` を利用するため、事前にインストール

```bash
cd argocd
helmfile apply
```

argocd の namespace が作成され、各種サービスが展開される。

`helmfile destroy`によって、削除される。

## ログイン
[公式手順](https://argo-cd.readthedocs.io/en/stable/getting_started/#3-access-the-argo-cd-api-server)に従って、
Argo CD のAPI サーバにアクセス

## argocd-appをデプロイ

```bash
cd applications
k apply -f argocd-application.yaml -n argocd
```
