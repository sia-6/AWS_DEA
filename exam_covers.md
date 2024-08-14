## **分析サービス**

### **Amazon Athena**
Amazon Athenaは、サーバーレスのクエリサービスで、S3に保存されたデータに対して直接SQLクエリを実行できます。Athenaは、データを取り込む手間をかけずに分析を行いたい場合に最適です。使用する分だけ料金が発生するため、コスト効率が良いのも特徴です。
- Amazon Athena ワークグループ : Athenaクエリの管理とコスト制御を行うための機能。特定のクエリや一連のクエリをグループ化し、それに関連する設定を一元管理できる。各ワークグループに対して、クエリの実行履歴やコスト、リソースの制御、クエリ結果の保存先などを設定できる。チームやプロジェクトごとにクエリ実行環境を分けて効率的に管理することが可能。
- Athena パーティション投影

### **Amazon EMR**
Amazon EMR (Elastic MapReduce) は、ビッグデータの処理と分析を行うためのクラウドサービスです。Hadoop、Spark、Hive、Prestoなどのオープンソースツールを使って、膨大なデータを分散処理することができます。EMRは、データの処理速度やコスト効率を最大化するために柔軟に設定可能です。
- Apache Hadoop
- Apache Spark

### **AWS Glue**
AWS Glueは、サーバーレスのETL（Extract, Transform, Load）サービスです。データを整理し、分析用のデータレイクやデータウェアハウスにロードするためのツールセットを提供します。Glueはデータカタログを利用して、データの発見、管理、クエリを簡素化します。
- DynamicFrame : ETLジョブで使用されるデータ構造。DynamicFrameは、Apache SparkのDataFrameに似ているが、さらに柔軟性があり、より豊富なメタデータを保持する。
- AWS Glue Data Quality
    - ルールセット
- コミットステートメント : ジョブ正常終了時にジョブブックマークを更新するために使用される。データの重複処理を防ぐ。
- PySpark 変換
    - FindMatches クラス : 入力のDynamicFrame内で一致するレコードを特定し、そのレコードの各グループに割り当てられている一意の識別子を含む新しいDynamicFrameを作成する。
- AWS Glue スキーマレジストリ
- AWS Glue ワークロード
- AWS Glue データカタログ
- AWS Glue クローラー
- パーティションインデックス
- 

### **AWS Glue DataBrew**
AWS Glue DataBrewは、コードを書くことなくデータのクレンジング、正規化、プロファイリングを行うためのビジュアルインターフェースを提供します。ETLジョブを作成する前に、データの準備を簡単に行うことができます。
- 集計関数
    - COUNT_DISTINCT : 選択したソース列の個別の値の合計数を新しい列に返す。

### **AWS Lake Formation**
AWS Lake Formationは、安全でスケーラブルなデータレイクの作成、管理を簡素化するサービスです。S3を基盤とし、さまざまなデータソースからデータを取り込み、統合するためのツールを提供します。また、データガバナンスやアクセス制御の管理を行いやすくする機能もあります。
- 行レベルのフィルター : データベースやデータレイク内で特定の条件に基づいてユーザーがアクセスできるデータの行を制限する機能。データセット全体を保持しながら、特定のユーザーが特定の行にアクセスできないように制御できる。
- FindMatches変換 : データの重複レコードを機械学習によって自動的に検出し、類似したデータをリンクするための機能。

### **Amazon Kinesis Data Firehose**
Amazon Kinesis Data Firehoseは、リアルタイムでストリーミングデータを取り込み、S3、Redshift、Elasticsearch Service、Splunkなどに送信するサービスです。データの変換やバッファリングもサポートしています。
- Splunk

### **Amazon Kinesis Data Streams**
Amazon Kinesis Data Streamsは、リアルタイムのストリーミングデータを収集し、処理するためのサービスです。データを継続的に取り込んでストリームに保存し、リアルタイムで処理を行うアプリケーションにデータを供給できます。
- Kinesis Client Library (KCL) : 

### **Amazon Managed Service for Apache Flink**
Amazon Managed Service for Apache Flinkは、Apache Flinkを管理された環境で提供し、リアルタイムのデータストリーム処理を実現します。スケーラビリティが高く、データの変換や集計をリアルタイムで行うことが可能です。

### **Amazon Managed Streaming for Apache Kafka (Amazon MSK)**
Amazon MSKは、Apache Kafkaを完全マネージドで提供するサービスです。Kafkaを利用して、ストリーミングデータの取り込みや配信を行うことができます。MSKは、Kafkaクラスターの運用管理を自動化し、スケーリングやパッチ適用も容易です。

### **Amazon OpenSearch Service**
Amazon OpenSearch Serviceは、リアルタイムの検索、ログ分析、モニタリングに使用されるマネージドサービスです。大規模なデータセットに対して、高速で検索可能なインデックスを作成し、分析を行うことができます。

### **Amazon QuickSight**
Amazon QuickSightは、クラウド上のBI（ビジネスインテリジェンス）サービスです。データの可視化やダッシュボードの作成を行い、ビジネスインサイトを迅速に得るためのツールを提供します。QuickSightは、S3、Redshift、Athenaなどのデータソースと統合されており、インタラクティブな分析が可能です。

## **アプリケーション統合サービス**

### **Amazon AppFlow**
Amazon AppFlowは、SaaSアプリケーションとAWSサービス間でデータを安全かつ容易に転送するためのマネージドサービスです。ノーコードでデータフローを構築し、データの変換、検証、フィルタリングなども行うことができます。

### **Amazon EventBridge**
Amazon EventBridgeは、サーバーレスのイベントバスサービスで、異なるAWSサービス、SaaSアプリケーション、カスタムアプリケーション間でイベントをルーティングします。イベント駆動型アーキテクチャの構築に最適です。

### **Amazon Managed Workflows for Apache Airflow (Amazon MWAA)**
Amazon MWAAは、Apache Airflowをマネージドサービスとして提供します。Airflowを使用して、複雑なデータパイプラインをオーケストレーションし、自動化できます。MWAAは、スケーリングや運用管理の負担を軽減します。
- 有向非巡回グラフ (DAG)
- 
### **Amazon Simple Notification Service (Amazon SNS)**
Amazon SNSは、プッシュ型のメッセージングサービスで、アプリケーション間での通知やアラートを実現します。SNSは、メッセージを複数のサブスクライバーに同時に送信でき、モバイルアプリケーションやエンドユーザーに通知を配信するのに適しています。

### **Amazon Simple Queue Service (Amazon SQS)**
Amazon SQSは、分散メッセージキューイングサービスで、メッセージの送受信を非同期に行うことができます。アプリケーション間のデカップリングや、処理の並列化を容易にするために使用されます。

### **AWS Step Functions**
AWS Step Functionsは、ワークフローオーケストレーションサービスで、複数のAWSサービスをつなぎ合わせて複雑なワークフローを作成します。視覚的なインターフェースを使って、ステートマシンを構築し、エラー処理や分岐ロジックを組み込むことができます。

## **クラウド財務管理サービス**

### **AWS Budgets**
AWS Budgetsは、コストと使用量を管理するためのサービスで、予算を設定し、その範囲を超えた場合に通知を受け取ることができます。コスト管理に役立つアラート機能が充実しており、予算を超える前に対策を講じることができます。

### **AWS Cost Explorer**
AWS Cost Explorerは、AWSのコストと使用量を視覚化するツールです。詳細なレポートを作成し、コストのトレンドを分析することで、コスト効率の最適化を図ることができます。

## **コンピューティングサービス**

### **AWS Batch**
AWS Batchは、バッチ処理ジョブの実行を簡素化するサービスです。ジョブのスケジューリング、リソースのプロビジョニング、実行の監視を自動化します。特に、数百万のジョブを効率的に処理するのに適しています。

### **Amazon EC2**
Amazon EC2は、仮想サーバー（インスタンス）を提供するサービスです。ユーザーは、必要なコンピューティングリソースを柔軟に選択・設定できるため、さまざまなワークロードに対応可能です。

### **AWS Lambda**
AWS Lambdaは、サーバーレスコンピューティングサービスで、コードをイベント駆動で実行します。インフラの管理が不要で、必要な時にだけリソースを使用するため、コスト効率が高いのが特徴です。

### **AWS Serverless Application Model (AWS SAM)**
AWS SAMは、サーバーレスアプリケーションを定義するためのフレームワークです。SAMテンプレートを使って、Lambda、API Gateway、DynamoDBなどのリソースを簡単にデプロイできます。

## **コンテナサービス**

### **Amazon Elastic Container Registry (Amazon ECR)**
Amazon ECRは、Dockerコンテナイメージを保存、管理、デプロイするためのレジストリサービスです。安全でスケーラブルなコンテナイメージのストレージを提供します。

### **Amazon Elastic Container Service (Amazon ECS)**
Amazon ECSは、コンテナ化されたアプリケーションを簡単にデプロイ、管理できるサービスです。ECSは、クラスタ内のコン

テナを効率的にオーケストレーションし、スケーリングも自動で行います。

### **Amazon Elastic Kubernetes Service (Amazon EKS)**
Amazon EKSは、Kubernetesをマネージドサービスとして提供します。EKSは、Kubernetesクラスターを簡単に設定、管理し、スケーリングや更新を自動化します。

## **データベースサービス**

### **Amazon DocumentDB (MongoDB互換)**
Amazon DocumentDBは、MongoDB互換のドキュメントデータベースサービスです。スケーラブルで高可用性を備えたドキュメントストアを提供します。

### **Amazon DynamoDB**
Amazon DynamoDBは、キーと値のペアを保存するNoSQLデータベースサービスです。ミリ秒単位のレスポンスが求められるアプリケーションに適しており、スケーラブルで高パフォーマンスなデータストアを提供します。

### **Amazon Keyspaces (Apache Cassandra向け)**
Amazon Keyspacesは、Apache Cassandra互換のマネージドデータベースサービスです。Cassandra APIを使用して、スケーラブルで高可用性のデータベースを運用できます。

### **Amazon MemoryDB for Redis**
Amazon MemoryDB for Redisは、Redis互換のインメモリデータベースサービスです。高パフォーマンスなキャッシュとデータストアを提供し、低レイテンシーのデータアクセスが可能です。

### **Amazon Neptune**
Amazon Neptuneは、グラフデータベースサービスです。プロパティグラフモデルとRDFトリプルストアの両方をサポートし、グラフベースのデータクエリを効率的に実行できます。

### **Amazon RDS**
Amazon RDSは、リレーショナルデータベースの設定、運用、スケーリングを自動化するサービスです。MySQL、PostgreSQL、MariaDB、Oracle、SQL Serverなど、複数のエンジンをサポートしています。

### **Amazon Redshift**
Amazon Redshiftは、データウェアハウスサービスで、大規模なデータセットに対する高速なクエリ処理を提供します。クラスター内の並列処理を活用し、クエリパフォーマンスを最大化します。
- 分散スタイル
- Amazon Redshift Streaming Ingestion : Kinesis Data StreamsやAmazon Managed Streaming for Apache Kafkaなどのデータストリームからのデータを即座にRedshiftに取り込み、分析を可能にする。
- Amazon Redshift Serverless : インフラを管理することなくデータ分析を実行、拡張できる。ワークロードに応じてコンピュート容量が自動的に拡張されるため、使用した分だけ料金を支払う。

## **デベロッパーツール**

### **AWS CLI**
AWS CLIは、AWSサービスを操作するためのコマンドラインツールです。スクリプトやバッチ処理を使用して、AWSリソースを自動化するのに役立ちます。

### **AWS Cloud9**
AWS Cloud9は、クラウドベースの統合開発環境（IDE）です。コードの編集、デバッグ、実行をブラウザから行うことができます。

### **AWS Cloud Development Kit (AWS CDK)**
AWS CDKは、プログラミング言語を使用してAWSリソースを定義し、デプロイするためのフレームワークです。インフラストラクチャをコードとして記述し、管理することができます。

### **AWS CodeBuild**
AWS CodeBuildは、ソースコードのビルドとテストを行うマネージドサービスです。複数のビルド環境に対応しており、継続的インテグレーション（CI）パイプラインの構築に利用されます。

### **AWS CodeCommit**
AWS CodeCommitは、ソースコードを管理するGit互換のリポジトリサービスです。プライベートなリポジトリを簡単に作成し、コードを安全に管理できます。

### **AWS CodeDeploy**
AWS CodeDeployは、アプリケーションの自動デプロイを行うサービスです。EC2、ECS、Lambdaなどのリソースに対して、シームレスなデプロイを実現します。

### **AWS CodePipeline**
AWS CodePipelineは、ビルド、テスト、デプロイメントのプロセスを自動化するサービスです。継続的インテグレーションと継続的デリバリー（CI/CD）をサポートします。

## **フロントエンドのウェブとモバイル**

### **Amazon API Gateway**
Amazon API Gatewayは、APIの作成、管理、デプロイを簡素化するサービスです。バックエンドサービスへのアクセスを制御し、APIをセキュアに公開できます。

## **機械学習**

### **Amazon SageMaker**
Amazon SageMakerは、機械学習モデルの構築、訓練、デプロイを行うための統合環境です。Jupyter Notebookを使用してデータ探索、モデルのトレーニング、推論の実行が可能です。

## **マネジメントとガバナンス**

### **AWS CloudFormation**
AWS CloudFormationは、AWSリソースをコードとして定義し、デプロイするサービスです。テンプレートを使用して、インフラストラクチャ全体を一貫して管理できます。

### **AWS CloudTrail**
AWS CloudTrailは、AWSアカウント内での操作を追跡するサービスです。操作ログを取得し、セキュリティ監査やコンプライアンスに活用できます。

### **Amazon CloudWatch**
Amazon CloudWatchは、AWSリソースやアプリケーションのモニタリングを行うサービスです。メトリクスの収集、アラームの設定、ログの分析が可能です。

### **Amazon CloudWatch Logs**
Amazon CloudWatch Logsは、ログデータを収集し、リアルタイムでモニタリングするためのサービスです。ログのクエリを実行して、システムの状態を分析することができます。

### **AWS Config**
AWS Configは、AWSリソースの構成変更を追跡するサービスです。リソースの設定や変更履歴を記録し、コンプライアンスのチェックを行います。

### **Amazon Managed Grafana**
Amazon Managed Grafanaは、Grafanaをマネージドサービスとして提供し、データの可視化を行います。AWSのメトリクスやログ、他のデータソースを統合して、カスタムダッシュボードを作成できます。

### **AWS Systems Manager**
AWS Systems Managerは、AWSリソースの運用管理を一元化するサービスです。インスタンスのパッチ適用、設定管理、自動化スクリプトの実行を行います。

### **AWS Well-Architected Tool**
AWS Well-Architected Toolは、AWSのベストプラクティスに基づいたシステム設計のレビューを行うツールです。セキュリティ、パフォーマンス、コスト効率などの観点から、システムを評価します。

## **移行と転送**

### **AWS Application Discovery Service**
AWS Application Discovery Serviceは、オンプレミスのアプリケーションをAWSに移行する際に、アプリケーションの依存関係や使用状況を調査するためのツールです。

### **AWS Application Migration Service**
AWS Application Migration Serviceは、オンプレミスサーバーをAWSに移行するためのマネージドサービスです。シームレスに仮想マシンをAWSにレプリケートし、移行を自動化します。

### **AWS Database Migration Service (AWS DMS)**
AWS DMSは、データベースをAWSに移行するためのサービスです。最小限のダウンタイムでデータをレプリケートし、異なるデータベースエンジン間の移行もサポートします。
- CDC(Change Data Capture) : データベース内で行われた変更（挿入、更新、削除）をキャプチャし、その変更をリアルタイムで別のデータベースに反映させるプロセス。
    - CDC レイテンシーのタイプ
        - ソースのレイテンシー : CDCLatencySource メトリクス
        - ターゲットのレイテンシー : CDCLatencyTarget メトリクス

### **AWS DataSync**
AWS DataSyncは、オンプレミスのデータをAWSに移行するためのサービスです。大量のデータを効率的に転送し、継続的な同期も可能です。

### **AWS Schema Conversion Tool (AWS SCT)**
AWS SCTは、異なるデータベースエンジン間でスキーマを変換するためのツールです。DMSと連携して、データベースの移行をサポートします。

### **AWS Snow ファミリー**
AWS Snowファミリーは、大量のデータを物理デバイスを使ってAWSに転送するためのサービスです。オフラインでのデータ転送をサポートし、データセンターからAWSへのデータ移行に適しています。

### **AWS Transfer Family**
AWS Transfer Familyは、SFTP、FTPS、FTPプロトコルを使ってデータをAWSに転送するためのマネージドサービスです。既存のデータ転送ワークフローをAWSに簡単に移行できます。

## **ネットワークとコンテンツ配信**

### **Amazon CloudFront**
Amazon CloudFrontは、グローバルに分散したコンテンツ配信ネットワーク（CDN

）です。ウェブサイト、API、動画コンテンツを高速で配信し、セキュリティ機能も強化されています。

### **AWS PrivateLink**
AWS PrivateLinkは、AWSサービスとプライベートに接続するためのサービスです。インターネットを経由せずに、セキュアな接続を実現します。

### **Amazon Route 53**
Amazon Route 53は、スケーラブルで信頼性の高いDNSウェブサービスです。ドメイン名の登録、ルーティング、ヘルスチェックなどを提供します。

### **Amazon VPC**
Amazon VPCは、AWSクラウド内に論理的に分離された仮想ネットワークを作成するサービスです。ネットワーク設定を柔軟に管理でき、セキュリティとスケーラビリティに優れたインフラストラクチャを構築できます。
- Gatewayエンドポイント : VPCのルートテーブルにエントリを追加することで、指定されたAWSサービスへのアクセスを可能にする。VPC内のサブネットから、指定されたサービスへの直接的な通信を提供する。
- Interfaceエンドポイント : AWS PrivateLinkを使用し、VPC内にエラスティックネットワークインターフェイス（ENI）を作成し、このENIを通じてAWSサービスへの通信を行う。

## **セキュリティ、アイデンティティ、コンプライアンス**

### **AWS Identity and Access Management (IAM)**
AWS IAMは、ユーザーやグループに対してAWSリソースへのアクセス権限を管理するサービスです。きめ細かいアクセス制御を実現し、セキュリティを強化します。

### **AWS Key Management Service (AWS KMS)**
AWS KMSは、暗号化キーの作成、管理、使用をサポートするマネージドサービスです。データの暗号化と保護を簡単に実現します。

### **Amazon Macie**
Amazon Macieは、機械学習を使用して、機密データの検出と保護を行うサービスです。S3バケット内のPII（個人を特定できる情報）などを自動的に識別し、セキュリティリスクを可視化します。

### **AWS Secrets Manager**
AWS Secrets Managerは、アプリケーションのシークレット（パスワード、APIキーなど）を安全に管理するサービスです。シークレットのローテーション、アクセス制御、監査を自動化します。

### **AWS Shield**
AWS Shieldは、分散型サービス拒否（DDoS）攻撃からアプリケーションを保護するサービスです。標準的な保護に加え、高度な保護オプションも提供されています。

### **AWS WAF**
AWS WAFは、ウェブアプリケーションファイアウォールで、アプリケーションを攻撃から保護します。ルールを設定して、特定の攻撃パターンを検出し、ブロックできます。

## **ストレージ**

### **AWS Backup**
AWS Backupは、AWSリソースのバックアップを一元的に管理するサービスです。スケジュール設定、保持ポリシー、復元を簡単に行えます。

### **Amazon Elastic Block Store (Amazon EBS)**
Amazon EBSは、EC2インスタンスに接続されるブロックストレージサービスです。高性能でスケーラブルなストレージを提供し、バックアップやリストアも容易に行えます。

### **Amazon Elastic File System (Amazon EFS)**
Amazon EFSは、NFS互換のファイルストレージサービスです。複数のEC2インスタンスからアクセスできるスケーラブルなファイルシステムを提供します。

### **Amazon S3**
Amazon S3は、オブジェクトストレージサービスで、大量のデータを安全に保存できます。スケーラビリティと耐久性に優れており、データのバックアップやアーカイブに適しています。
- Amazon S3 Storage Lens : Amazon S3バケットとオブジェクトのストレージメトリクスを可視化して分析できるツール。
- Amazon S3 Object Lambda : Amazon S3バケットからデータを取得する際に、AWS Lambda関数を使ってデータをリアルタイムで動的に処理・変換できる機能。
### **Amazon S3 Glacier**
Amazon S3 Glacierは、長期アーカイブ向けの低コストなストレージサービスです。データのリストアは、数分から数時間で行えるオプションが用意されています。
