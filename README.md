# terraform-github-actions-aws-cicd-exercises

Terraform と GitHub Actions を使用した AWS リソースの CI/CD の練習用コード集

## ■ 使用法

### ◎ EC2 インスタンスの CI/CD を行う場合

1. ブランチを切る<br>
    `main` ブランチから別ブランチを作成する
    ```sh
    git checkout -b ${BRANCH_NAME}
    ```

1. `terraform/aws/ec2/main.tf` を修正する<br>
    EC2 インスタンスに対しての tf ファイル `terraform/aws/ec2/main.tf` を修正する

1. Pull Request を発行する。<br>
    GitHub レポジトリ上で main ブランチに対しての [PR](https://github.com/Yagami360/terraform-github-actions-aws-cicd-exercises/pulls) を出す。

1. PR の内容を `main` ブランチに merge し、EC2 インスタンスに対しての CI/CD を行う。<br>
    PR の内容に問題なければ、`main` ブランチに merge する。
    merge 処理後、`.github/workflows/terrafform-aws-workflow.yml` で定義したワークフローが実行され 、EC2 インスタンスへの CI/CD が自動的に行われる。

1. [GitHub リポジトリの Actions タブ](https://github.com/Yagami360/terraform-github-actions-aws-cicd-exercises/actions)から、実行されたワークフローのログを確認する

### ◎ IAM の CI/CD を行う場合

準備中...

### ◎ EKS クラスターの CI/CD を行う場合

準備中...

## ■ 参考サイト
- https://github.com/Yagami360/ai-product-dev-tips/tree/master/ml_ops/66
