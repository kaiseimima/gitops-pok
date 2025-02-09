``` text
.
├── terraform/                  # インフラ管理用Terraformコード
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── providers.tf
├── k8s/                        # Kubernetesマニフェスト（ArgoCDが監視するGitOpsリポジトリ）
│   ├── deployment.yaml         # NginxのDeployment定義
│   ├── service.yaml            # Service定義（LoadBalancerやNodePortなど）
│   └── argocd-app.yaml         # ArgoCD Application定義（オプション）
├── docker/                     # Docker関連ファイル
│   ├── Dockerfile              # Nginxイメージ作成用Dockerfile
│   └── default.conf            # 必要に応じたNginxの設定ファイル
├── .github/
│   └── workflows/
│       └── ci.yml              # GitHub Actionsワークフロー
└── README.md
```