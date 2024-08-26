参考
https://tech.nri-net.com/entry/aws_certified_data_engineer_associate

- Apache Hadoop
- Apache Spark

## **分析サービス**

### [**Amazon Athena**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/what-is.html)
Amazon Athenaは、サーバーレスのクエリサービスで、S3に保存されたデータに対して直接SQLクエリを実行できる。Athenaは、データを取り込む手間をかけずに分析を行いたい場合に最適で、使用する分だけ料金が発生するためコスト効率が良い。
- **[ワークグループの仕組み
](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/user-created-workgroups.html)** : Amazon Athenaのワークグループは、クエリの実行環境を分離し、管理するための機能。各アカウントにはデフォルトでプライマリワークグループがあり、他のワークグループを作成できる。ワークグループごとにクエリ履歴や設定が独立しており、他のワークグループのクエリには影響を与えない。ワークグループを無効にするとクエリは実行できなくなり、必要な設定を強制的に適用することもできる。
- **[Amazon Athena でのパーティション射影 (Partition Projection)](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/partition-projection.html)** : 高度にパーティション化されたテーブルのクエリパフォーマンスを改善するための機能。AWS Glueのテーブルプロパティを使用して、Athenaがパーティション情報を「射影」することで、パーティションの検索や管理が迅速化される。これによりクエリの実行時間が短縮され、パーティション管理が自動化され、パーティションプルーニングを行うことで必要なパーティションのみをクエリに適用し効率をさらに高める。
- **[Amazon Athena フェデレーテッドクエリを使用する](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html)** : Athenaを使用してAmazon S3以外のデータソースにもクエリを実行できる機能です。これにより、Redshift、RDS、さらには外部のオンプレミスデータベースなど、さまざまなデータソースに対してSQLクエリを実行し、統合的にデータを分析できます。フェデレーテッドクエリを利用することで、複数のデータソースをシームレスに接続し、統一的な分析を実現します。
- [**Amazon Athenaの新しいフェデレーテッド・クエリによる複数データソースの検索**](https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html)
- **[Amazon Athena クエリ結果の再利用機能](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/reusing-query-results.html)** : 同一のクエリが複数回実行される際に、以前の結果を再利用することでコスト削減とクエリの応答時間短縮を実現する機能。クエリが再利用されるとAthenaは既存の結果を返し、不要な計算を避けることができる。この機能は、クエリの実行状況に基づいて自動的に適用され、データ分析効率を向上させる。
- SQL クエリのパフォーマンス
- [**Athena の問題のトラブルシューティング**](https://docs.aws.amazon.com/athena/latest/ug/troubleshooting-athena.html#troubleshooting-athena-create-table-as-select-ctas)
- [**クエリ結果からのテーブルの作成 (CTAS)**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/ctas.html)
- [**クエリ結果を別の形式で書き込む**](https://docs.aws.amazon.com/athena/latest/ug/ctas-examples.html#ctas-example-format)
- [**Amazon Athena で Apache Spark を開始**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/notebooks-spark-getting-started.html)
- [**列指向ストレージ形式とは**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/columnar-storage.html)
<<<<<<< HEAD
- [**MSCK REPAIR TABLE**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/msck-repair-table.html)
=======
>>>>>>> 44e5177bad7ffdc149c4a5bff7ce6ead0860fccb

### [**Amazon EMR**](https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-what-is-emr.html)
Amazon EMR (Elastic MapReduce)は、ビッグデータ処理と分析のためのフルマネージドクラウドサービス。ユーザーはApache Hadoop、Apache Spark、Prestoなどのフレームワークを使用して膨大なデータを分散処理できる。EMRは柔軟なスケーリング、コスト効率、そしてセキュリティの統合を提供し、データの収集、処理、分析が容易となる。また、オンデマンドやスポットインスタンスを利用して、リソースの最適な利用が可能。EMRクラスターは、複数のAmazon EC2インスタンス（仮想マシン）で構成され、各インスタンスが「ノード」として機能する。
- [**ノードタイプ**](https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-overview.html#emr-overview-clusters) : Amazon EMRのノードタイプには「プライマリーノード」「コアノード」「タスクノード」がある。
- [**Apache Hive メタストアを Amazon EMR に移行してデプロイする**](https://aws.amazon.com/jp/blogs/news/migrate-and-deploy-your-apache-hive-metastore-on-amazon-emr/)
- [**セキュリティとアクセス制御**](https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-data-encryption-options.html)
- [**サポートされるアプリケーションと機能**](https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-plan-ha-applications.html)

### **AWS Glue**
AWS Glueは、サーバーレスのETL（Extract, Transform, Load）サービス。データを整理し、分析用のデータレイクやデータウェアハウスにロードするためのツールセットを提供している。Glueはデータカタログを利用して、データの発見、管理、クエリを簡素化。
- DynamicFrame : ETLジョブで使用されるデータ構造。DynamicFrameは、Apache SparkのDataFrameに似ているが、さらに柔軟性があり、より豊富なメタデータを保持する。
- **[大きなグループの入力ファイルの読み取り](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/grouping-input-files.html)** : テーブルのプロパティを設定することで、Amazon S3に保存されている多数の小さなファイルをグループ化し、ETLジョブの効率を向上させることができる。これにより、各ETLタスクが一度に複数のファイルを単一のインメモリパーティションに読み取ることができるため処理が効率化される。
- [**AWS Glue Data Quality**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/glue-data-quality.html) : データ品質を管理および監視するための機能を提供するサービス。ETL（抽出、変換、ロード）ジョブを実行する際に、データの品質を自動的に評価し、定義されたルールセットに基づいてデータが基準を満たしているかどうかを確認できる。Data Qualityは、ルールの作成、実行、および評価をサポートし、異常を検出して修正するための手段を提供している。
- [**AWS Lake Formation FindMatches によるレコードのマッチング**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/machine-learning.html) : 重複したレコードや一致するレコードを識別するための機械学習ベースの変換機能。FindMatchesは、異なるデータセット間で似たレコードを特定し、クレンジングや統合のプロセスを簡素化する。FindMatchesはトレーニングされたモデルを使って、一意の識別子がない場合でもレコードを一致させることができ、データの重複を排除したり、データの品質を向上させるために役立つ。
- [**AWS Glue スキーマレジストリ**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/schema-registry.html) : データストリームのスキーマを管理するためのサーバーレス機能。このレジストリを使用すると、データストリーム（例えば、Apache Kafka、Amazon Kinesisなど）で扱うデータのスキーマを中央で一元管理し、スキーマの進化を追跡できる。
- [**AWS Glue ワークフロー**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/workflows_overview.html) : 複数のクローラ、ジョブ、トリガーを組み合わせて、複雑なETL（抽出、変換、ロード）アクティビティを管理および可視化するための機能。各ワークフローは、含まれる全てのジョブとクローラの実行状況と進捗を記録し、グラフィカルに表示する。ワークフローは設計図から作成でき、コンソールやAPIを使って手動で構築することもでき、トリガーを活用して依存関係のあるジョブやクローラの自動実行が可能。
- **[AWS Glue データカタログ](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/manage-catalog.html)** : Amazon S3データセットの構造メタデータと運用メタデータを保存する中央メタデータリポジトリ。データカタログを適切に管理することでデータ品質、パフォーマンス、セキュリティ、ガバナンスを維持できる。
- AWS Glue クローラー
- パーティションインデックス
- AWS Glue 接続
- AWS Glue トリガー
    - オンデマンドトリガー
- [**AWS Glue ジョブ**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/aws-glue-api-jobs-job.html)
- [**ジョブ ブックマーク**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/monitor-continuations.html) : AWS Glueが以前に処理したデータを記憶し、ジョブの再実行時にそのデータをスキップする機能。すでに処理されたデータの再処理を防ぎ、ETLジョブの効率を向上させる。特に大規模なデータ処理において処理時間とコストを削減するのに有効。
    - コミットステートメント　(job.commit()): ジョブが正常に終了した際にジョブブックマークを更新するための機能。次回のジョブ実行時にどこまでデータが処理されたかを正確に追跡し、重複処理を防ぐ。コミットステートメントを使用することで、データ処理の整合性と効率性が向上する。
- [**AWS Glue Flex ジョブのご紹介: ETL ワークロードのコスト削減**](https://aws.amazon.com/jp/blogs/big-data/introducing-aws-glue-flex-jobs-cost-savings-on-etl-workloads/) : Flex と呼ばれるAWS Glueジョブ実行クラスは、コストを最大34%削減できる実行モード。緊急度が低く、すぐに開始する必要のないデータ統合ワークロードに最適で、AWSの予備キャパシティーを使用して実行される。ジョブの開始時間や実行時間は変動する可能性があるが、通常のジョブ機能はそのまま利用できる。重要なワークロードには通常のオプションを、急を要しないワークロードにはFlexを利用することで、コスト効率を最大化できる。
- [**AWS Glue でSparkジョブのジョブプロパティを構成する**](https://docs.aws.amazon.com/glue/latest/dg/add-job.html)
- AWS Glue Studio
    - Detect PII 変換
- AWSGlueServiceRole
- FindMatches 機械学習 (ML) 変換
- AWS Glue PySpark ジョブ
- AWS Glue Python シェルジョブ
- [**API を使用したデータ品質の測定および管理**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/data-quality-using-apis.html)
- [**Apache Iceberg と AWS Glue を使用してデータレイクに CDC ベースの UPSERT を実装する**](https://aws.amazon.com/jp/blogs/big-data/implement-a-cdc-based-upsert-in-a-data-lake-using-apache-iceberg-and-aws-glue/)
- [**[行から列へのピボット] 変換の使用**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/transforms-pivot-rows-to-columns.html)

### **AWS Glue DataBrew**
AWS Glue DataBrewは、コードを書くことなくデータのクレンジング、正規化、プロファイリングを行うためのビジュアルインターフェースを提供します。ETLジョブを作成する前に、データの準備を簡単に行うことができます。
- 集計関数
    - COUNT_DISTINCT : 選択したソース列の個別の値の合計数を新しい列に返す。
- コーディング
    - NEST_TO_MAP 変換
- [**AWS Glue DataBrew でのデータ品質の検証**](https://docs.aws.amazon.com/databrew/latest/dg/profile.data-quality-rules.html)

### **AWS Lake Formation**
AWS Lake Formationは、安全でスケーラブルなデータレイクの作成、管理を簡素化するサービスです。S3を基盤とし、さまざまなデータソースからデータを取り込み、統合するためのツールを提供します。また、データガバナンスやアクセス制御の管理を行いやすくする機能もあります。
- 行レベルのフィルター : データベースやデータレイク内で特定の条件に基づいてユーザーがアクセスできるデータの行を制限する機能。データセット全体を保持しながら、特定のユーザーが特定の行にアクセスできないように制御できる。
- FindMatches変換 : データの重複レコードを機械学習によって自動的に検出し、類似したデータをリンクするための機能。
- [**Lake Formation 許可へのオンボーディング**](https://docs.aws.amazon.com/ja_jp/lake-formation/latest/dg/onboarding-lf-permissions.html)

### **Amazon Kinesis Data Firehose**
Amazon Kinesis Data Firehoseは、リアルタイムでストリーミングデータを取り込み、S3、Redshift、Elasticsearch Service、Splunkなどに送信するサービスです。データの変換やバッファリングもサポートしています。
- Splunk

### **Amazon Kinesis Data Streams**
Amazon Kinesis Data Streamsは、リアルタイムのストリーミングデータを収集し、処理するためのサービスです。データを継続的に取り込んでストリームに保存し、リアルタイムで処理を行うアプリケーションにデータを供給できます。
- Kinesis Client Library (KCL) :
- シャードの負荷
    - WriteThroughputExceeded
- [**Amazon CloudWatch で Amazon Kinesis Data Streams サービスを監視する**](https://docs.aws.amazon.com/streams/latest/dev/monitoring-with-cloudwatch.html)
- [**Kinesis Data Streams を使用したクロスアカウントクロスリージョンログデータ共有**](https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/logs/CrossAccountSubscriptions-Kinesis.html)
- [**Amazon Kinesis Data Streams で AWS Lambda を使用する**](https://docs.aws.amazon.com/ja_jp/streams/latest/dev/tutorial-stock-data-lambda.html)

### **Amazon Managed Service for Apache Flink**
Amazon Managed Service for Apache Flinkは、Apache Flinkを管理された環境で提供し、リアルタイムのデータストリーム処理を実現します。スケーラビリティが高く、データの変換や集計をリアルタイムで行うことが可能です。
- Apache Flink コネクタ

### **Amazon Managed Streaming for Apache Kafka (Amazon MSK)**
Amazon MSKは、Apache Kafkaを完全マネージドで提供するサービスです。Kafkaを利用して、ストリーミングデータの取り込みや配信を行うことができます。MSKは、Kafkaクラスターの運用管理を自動化し、スケーリングやパッチ適用も容易です。

### **Amazon OpenSearch Service**
Amazon OpenSearch Serviceは、リアルタイムの検索、ログ分析、モニタリングに使用されるマネージドサービスです。大規模なデータセットに対して、高速で検索可能なインデックスを作成し、分析を行うことができます。OpenSearchダッシュボード（以前はKibanaとして知られていた）は、OpenSearchデータに直接アクセスし、リアルタイムでデータを視覚化するための最も適したツールです。

### **Amazon QuickSight**
Amazon QuickSightは、クラウド上のBI（ビジネスインテリジェンス）サービスです。データの可視化やダッシュボードの作成を行い、ビジネスインサイトを迅速に得るためのツールを提供します。QuickSightは、S3、Redshift、Athenaなどのデータソースと統合されており、インタラクティブな分析が可能です。
- [**SPICE へのデータのインポート**](https://docs.aws.amazon.com/ja_jp/quicksight/latest/user/spice.html)

## **アプリケーション統合サービス**

### [**Amazon AppFlow**](https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html)
Amazon AppFlowは、SaaSアプリケーションとAWSサービス間でデータを安全かつ容易に転送するためのマネージドサービスです。ノーコードでデータフローを構築し、データの変換、検証、フィルタリングなども行うことができます。

### **Amazon EventBridge**
Amazon EventBridgeは、サーバーレスのイベントバスサービスで、異なるAWSサービス、SaaSアプリケーション、カスタムアプリケーション間でイベントをルーティングします。イベント駆動型アーキテクチャの構築に最適です。

### **Amazon Managed Workflows for Apache Airflow (Amazon MWAA)**
Amazon MWAAは、Apache Airflowをマネージドサービスとして提供します。Airflowを使用して、複雑なデータパイプラインをオーケストレーションし、自動化できます。MWAAは、スケーリングや運用管理の負担を軽減します。
- 有向非巡回グラフ (DAG)
- 
### **Amazon Simple Notification Service (Amazon SNS)**
Amazon SNSは、プッシュ型のメッセージングサービスで、アプリケーション間での通知やアラートを実現します。SNSは、メッセージを複数のサブスクライバーに同時に送信でき、モバイルアプリケーションやエンドユーザーに通知を配信するのに適しています。
- [**CloudWatchを使用した Amazon SNS トピックのモニタリング**](https://docs.aws.amazon.com/ja_jp/sns/latest/dg/sns-monitoring-using-cloudwatch.html)

### **Amazon Simple Queue Service (Amazon SQS)**
Amazon SQSは、分散メッセージキューイングサービスで、メッセージの送受信を非同期に行うことができます。アプリケーション間のデカップリングや、処理の並列化を容易にするために使用されます。
- SQS デッドレターキュー

### [**AWS Step Functions**](https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/welcome.html)
AWS Step Functionsは、ワークフローオーケストレーションサービスで、複数のAWSサービスをつなぎ合わせて複雑なワークフローを作成します。視覚的なインターフェースを使って、ステートマシンを構築し、エラー処理や分岐ロジックを組み込むことができます。
- AWS Step Functions タスク
- [**Step Functions 状態**](https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/concepts-states.html)
- Step Functions ステートマシンコード
- AWS Step Functions ワークフロー

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
- lambda レイヤー
- [**実行ロールを使用した Lambda 関数のアクセス許可の定義**](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/lambda-intro-execution-role.html)

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
- [**DynamoDB Auto Scaling によるスループットキャパシティの自動管理**](https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/AutoScaling.html)
<<<<<<< HEAD
- [**PartiQL: Amazon DynamoDB 用の SQL 互換クエリ言語**](https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/ql-reference.html)
=======
>>>>>>> 44e5177bad7ffdc149c4a5bff7ce6ead0860fccb

### **Amazon Keyspaces (Apache Cassandra向け)**
Amazon Keyspacesは、Apache Cassandra互換のマネージドデータベースサービスです。Cassandra APIを使用して、スケーラブルで高可用性のデータベースを運用できます。

### **Amazon MemoryDB for Redis**
Amazon MemoryDB for Redisは、Redis互換のインメモリデータベースサービスです。高パフォーマンスなキャッシュとデータストアを提供し、低レイテンシーのデータアクセスが可能です。

### **Amazon Neptune**
Amazon Neptuneは、グラフデータベースサービスです。プロパティグラフモデルとRDFトリプルストアの両方をサポートし、グラフベースのデータクエリを効率的に実行できます。

### **Amazon RDS**
Amazon RDSは、リレーショナルデータベースの設定、運用、スケーリングを自動化するサービスです。MySQL、PostgreSQL、MariaDB、Oracle、SQL Serverなど、複数のエンジンをサポートしています。
- Amazon RDS パフォーマンスインサイト
- [**Amazon RDSリソースの暗号化**](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html)

### **Amazon Redshift**
Amazon Redshiftは、データウェアハウスサービスで、大規模なデータセットに対する高速なクエリ処理を提供します。クラスター内の並列処理を活用し、クエリパフォーマンスを最大化します。
- [**分散スタイル**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/c_choosing_dist_sort.html)
- Amazon Redshift Streaming Ingestion : Kinesis Data StreamsやAmazon Managed Streaming for Apache Kafkaなどのデータストリームからのデータを即座にRedshiftに取り込み、分析を可能にする。
- [**Amazon Redshift Serverless**](https://docs.aws.amazon.com/ja_jp/redshift/latest/mgmt/working-with-serverless.html) : インフラを管理することなくデータ分析を実行、拡張できる。ワークロードに応じてコンピュート容量が自動的に拡張されるため、使用した分だけ料金を支払う。
<<<<<<< HEAD
- [**Amazon Redshift のフェデレーテッドクエリによるデータのクエリ**](https://docs.aws.amazon.com/redshift/latest/dg/federated-overview.html)
=======
- Amazon Redshiftフェデレーテッドクエリ
>>>>>>> 44e5177bad7ffdc149c4a5bff7ce6ead0860fccb
- データ共有
- [**Amazon Redshift でのマテリアライズドビューの作成**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/materialized-view-overview.html)
- Amazon Redshift Data API
- ワークロード管理 (WLM) キュー
- クラスター ノード
- SQL クエリを実行したデータの変換 (Amazon Redshift ストアドプロシージャなど)
- Redshift テーブルビュー
    - STL_ALERT_EVENT_LOG
- Amazon Redshift のクエリエディタ v2
- Amazon Redshift マニフェストファイル
- ステージング Redshift テーブル
- テーブルの複合ソートキー
- [**VACUUM**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/r_VACUUM_command.html)
- [**EXTRACT 関数**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/r_EXTRACT_function.html)
- [**Amazon Redshift ストリーミング取り込みによるリアルタイム分析**](https://aws.amazon.com/jp/blogs/big-data/real-time-analytics-with-amazon-redshift-streaming-ingestion/)
- [**Amazon Redshift データ API を使用して Amazon Redshift クラスターを操作する**](https://aws.amazon.com/jp/blogs/big-data/using-the-amazon-redshift-data-api-to-interact-with-amazon-redshift-clusters/)
- [**Amazon S3 からデータをロードする**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/t_Loading-data-from-S3.html)
- [**データを Amazon S3 にアンロードする**](https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/t_Unloading_tables.html)

## **デベロッパーツール**

### **AWS CLI**
AWS CLIは、AWSサービスを操作するためのコマンドラインツールです。スクリプトやバッチ処理を使用して、AWSリソースを自動化するのに役立ちます。

### **AWS Cloud9**
AWS Cloud9は、クラウドベースの統合開発環境（IDE）です。コードの編集、デバッグ、実行をブラウザから行うことができます。

### **AWS Cloud Development Kit (AWS CDK)**
AWS CDKは、プログラミング言語を使用してAWSリソースを定義し、デプロイするためのフレームワークです。インフラストラクチャをコードとして記述し、管理することができます。

### [**AWS CodeBuild**](https://docs.aws.amazon.com/ja_jp/codebuild/latest/userguide/welcome.html)
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
- [**API Gateway で Lambda を使用する**](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/services-apigateway-tutorial.html)

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
- [**AWS Systems Manager Parameter Store**](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/systems-manager-parameter-store.html)

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

https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Troubleshooting_Latency.html
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
- [**Amazon S3 のゲートウェイエンドポイント**](https://docs.aws.amazon.com/ja_jp/vpc/latest/privatelink/vpc-endpoints-s3.html)
- [**ネットワークアクセスコントロールリストを使用して、サブネットのトラフィックを制御する**](https://docs.aws.amazon.com/ja_jp/vpc/latest/userguide/vpc-network-acls.html)

## **セキュリティ、アイデンティティ、コンプライアンス**

### **AWS Identity and Access Management (IAM)**
AWS IAMは、ユーザーやグループに対してAWSリソースへのアクセス権限を管理するサービスです。きめ細かいアクセス制御を実現し、セキュリティを強化します。

### **AWS Key Management Service (AWS KMS)**
AWS KMSは、暗号化キーの作成、管理、使用をサポートするマネージドサービスです。データの暗号化と保護を簡単に実現します。
- [**AWS KMS キーによる二層式サーバー側の暗号化 (DSSE-KMS) の使用**](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/UsingDSSEncryption.html)
- [**AWS KMS キーによるサーバー側暗号化 (SSE-KMS) の使用**](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html)

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
- [**Amazon Elastic Volumes EBS を使用してボリュームを変更する**](https://docs.aws.amazon.com/ja_jp/ebs/latest/userguide/ebs-modify-volume.html)

### **Amazon Elastic File System (Amazon EFS)**
Amazon EFSは、NFS互換のファイルストレージサービスです。複数のEC2インスタンスからアクセスできるスケーラブルなファイルシステムを提供します。

### **Amazon S3**
Amazon S3は、オブジェクトストレージサービスで、大量のデータを安全に保存できます。スケーラビリティと耐久性に優れており、データのバックアップやアーカイブに適しています。
- Amazon S3 Storage Lens : Amazon S3バケットとオブジェクトのストレージメトリクスを可視化して分析できるツール。
- Amazon S3 Object Lambda : Amazon S3バケットからデータを取得する際に、AWS Lambda関数を使ってデータをリアルタイムで動的に処理・変換できる機能。
- S3 ストレージクラス
- S3 アクセス アナライザー
- S3 Select
- S3 バージョン管理
- [**Amazon S3 Object Lambda のご紹介 – S3 から取得されるデータをコードで処理**](https://aws.amazon.com/jp/blogs/aws/introducing-amazon-s3-object-lambda-use-your-code-to-process-data-as-it-is-being-retrieved-from-s3/)
- [**Amazon S3 イベント通知**](https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html)

### **Amazon S3 Glacier**
Amazon S3 Glacierは、長期アーカイブ向けの低コストなストレージサービスです。データのリストアは、数分から数時間で行えるオプションが用意されています。
- Amazon S3 Glacier Select
