## 社内勉強会で使用したOKE(Oracle Container Engine for Kubernetes)のマニフェストファイル一覧

### 前提条件

以下が完了していること

1. OCI上でのOKE、Mount Target、FSSのデプロイ
2. OKEから各種リソースを管理するためのOCIポリシー設定
3. OCI CLIのインストールとConfig設定
4. kubectlのインストール
5. OKEへアクセスするためのConfig設定

### デプロイ方法

`kubectl apply -k .`でWordpressをデプロイ

```console
[opc@test-vm1 oke-demo-aa-study]$ kubectl apply -k .
namespace/wordpress created
storageclass.storage.k8s.io/oci-fss created
secret/mysql-pass created
service/wordpress-lb created
service/wordpress-mysql-service created
persistentvolume/oke-fsspv created
persistentvolumeclaim/mysql-pv-claim created
persistentvolumeclaim/oke-fsspvc created
deployment.apps/wordpress created
deployment.apps/wordpress-mysql-deployment created
```
