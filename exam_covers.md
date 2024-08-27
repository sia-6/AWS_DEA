参考
https://tech.nri-net.com/entry/aws_certified_data_engineer_associate

### 試験ガイド
### Apache Project

Apacheプロジェクトを理解することは、AWS DEA資格取得を目指す上で重要です。なぜならAWSとApacheのツールやフレームワークが多くのデータ処理および分析ワークフローにおいて連携して用いられているからです。

1. **データ処理の理解**: Apache HadoopやSparkなどのツールは、大規模データの処理においてAWSのサービスと連携して利用されます。これにより、データ処理のパイプラインやワークフローを効率的に設計できます。

2. **AWSとの連携**: AWS GlueやEMRは、Apacheベースのツールをサポートしており、これらのツールの動作を理解することは、AWS上での効果的なデータ処理に直結します。

3. **実践的な知識**: Apacheプロジェクトを学ぶことで、実際のデータ処理環境における課題解決能力が向上し、資格試験のシナリオ問題にも対応しやすくなります。

したがって、AWSとApacheプロジェクトの両方を理解することは、資格試験において非常に役立つと言えます。

- Apache Hadoop
https://projects.apache.org/project.html?hadoop
- Apache Hive
https://projects.apache.org/project.html?hive
- Apache Spark
https://projects.apache.org/project.html?spark
- Apache Parquet
https://projects.apache.org/project.html?parquet
- Apache Flink
https://projects.apache.org/project.html?flink
- Apache Airflow
https://projects.apache.org/project.html?airflow
- Apache Iceberg
https://projects.apache.org/project.html?iceberg
- Apache Kafka
https://projects.apache.org/project.html?kafka

## **分析サービス**

### [**Amazon Athena**](https://docs.aws.amazon.com/ja_jp/athena/latest/ug/what-is.html)
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/user-created-workgroups.html
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/partition-projection.html
https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/reusing-query-results.html
https://docs.aws.amazon.com/athena/latest/ug/troubleshooting-athena.html#troubleshooting-athena-create-table-as-select-ctas
https://docs.aws.amazon.com/athena/latest/ug/ctas-examples.html#ctas-example-format
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/notebooks-spark-getting-started.html
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/columnar-storage.html
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/msck-repair-table.html
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/data-sources-glue.html

### [**Amazon EMR**](https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-what-is-emr.html)
https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-overview.html#emr-overview-clusters
https://aws.amazon.com/jp/blogs/news/migrate-and-deploy-your-apache-hive-metastore-on-amazon-emr/
https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-data-encryption-options.html
https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-plan-ha-applications.html
https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/architecture.html

### [**AWS Glue**](https://docs.aws.amazon.com/ja_jp/glue/latest/dg/what-is-glue.html)
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/add-crawler.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/aws-glue-api-crawler-pyspark-extensions-dynamic-frame.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/grouping-input-files.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/glue-data-quality.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/machine-learning.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/schema-registry.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/workflows_overview.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/manage-catalog.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/aws-glue-api-jobs-job.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/monitor-continuations.html
https://aws.amazon.com/jp/blogs/big-data/introducing-aws-glue-flex-jobs-cost-savings-on-etl-workloads/
https://docs.aws.amazon.com/glue/latest/dg/add-job.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/data-quality-using-apis.html
https://aws.amazon.com/jp/blogs/big-data/implement-a-cdc-based-upsert-in-a-data-lake-using-apache-iceberg-and-aws-glue/
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/transforms-pivot-rows-to-columns.html
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/set-up-iam.html

### [**AWS Glue DataBrew**](https://docs.aws.amazon.com/databrew/latest/dg/what-is.html)
https://docs.aws.amazon.com/databrew/latest/dg/profile.data-quality-rules.html

### [**AWS Lake Formation**](https://docs.aws.amazon.com/ja_jp/lake-formation/latest/dg/what-is-lake-formation.html)
https://docs.aws.amazon.com/ja_jp/lake-formation/latest/dg/onboarding-lf-permissions.html
https://docs.aws.amazon.com/ja_jp/lake-formation/latest/dg/data-filtering.html

### [**Amazon Kinesis Data Firehose**](https://docs.aws.amazon.com/ja_jp/firehose/latest/dev/what-is-this-service.html)
Amazon Kinesis Data Firehoseは、リアルタイムでストリーミングデータを取り込み、S3、Redshift、Elasticsearch Service、Splunkなどに送信するサービスです。データの変換やバッファリングもサポートしています。
https://docs.aws.amazon.com/ja_jp/firehose/latest/dev/record-format-conversion.html

### **Amazon Kinesis Data Streams**
Amazon Kinesis Data Streamsは、リアルタイムのストリーミングデータを収集し、処理するためのサービスです。データを継続的に取り込んでストリームに保存し、リアルタイムで処理を行うアプリケーションにデータを供給できます。
https://docs.aws.amazon.com/streams/latest/dev/monitoring-with-cloudwatch.html
https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/logs/CrossAccountSubscriptions-Kinesis.html
https://docs.aws.amazon.com/ja_jp/streams/latest/dev/tutorial-stock-data-lambda.html

### **Amazon Managed Service for Apache Flink**
Amazon Managed Service for Apache Flinkは、Apache Flinkを管理された環境で提供し、リアルタイムのデータストリーム処理を実現します。スケーラビリティが高く、データの変換や集計をリアルタイムで行うことが可能です。
- Apache Flink コネクタ

### **Amazon Managed Streaming for Apache Kafka (Amazon MSK)**
Amazon MSKは、Apache Kafkaを完全マネージドで提供するサービスです。Kafkaを利用して、ストリーミングデータの取り込みや配信を行うことができます。MSKは、Kafkaクラスターの運用管理を自動化し、スケーリングやパッチ適用も容易です。

### **Amazon OpenSearch Service**
Amazon OpenSearch Serviceは、リアルタイムの検索、ログ分析、モニタリングに使用されるマネージドサービスです。大規模なデータセットに対して、高速で検索可能なインデックスを作成し、分析を行うことができます。OpenSearchダッシュボード（以前はKibanaとして知られていた）は、OpenSearchデータに直接アクセスし、リアルタイムでデータを視覚化するための最も適したツールです。

### **Amazon QuickSight**
Amazon QuickSightは、クラウド上のBI（ビジネスインテリジェンス）サービスです。データの可視化やダッシュボードの作成を行い、ビジネスインサイトを迅速に得るためのツールを提供します。QuickSightは、S3、Redshift、Athenaなどのデータソースと統合されており、インタラクティブな分析が可能です。
https://docs.aws.amazon.com/ja_jp/quicksight/latest/user/spice.html

### [**Amazon CloudWatch Logs**](https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html)
https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/logs/CrossAccountSubscriptions-Kinesis.html

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
https://docs.aws.amazon.com/ja_jp/step-functions/latest/dg/concepts-states.html

### [**AWS Lambda**](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/welcome.html)
https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/chapter-layers.html
https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/lambda-intro-execution-role.html
https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/with-sns.html

### **Amazon DynamoDB**
https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/AutoScaling.html
https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/ql-reference.html

### [**Amazon RDS**](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/Welcome.html)
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html

### [**Amazon Redshift**](https://docs.aws.amazon.com/ja_jp/redshift/latest/mgmt/welcome.html)
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/c_choosing_dist_sort.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/mgmt/working-with-serverless.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/materialized-view-streaming-ingestion.html
https://docs.aws.amazon.com/redshift/latest/dg/federated-overview.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/materialized-view-overview.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/c_intro_STL_tables.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/datashare-overview.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/c-using-spectrum.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/r_VACUUM_command.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/r_EXTRACT_function.html
https://aws.amazon.com/jp/blogs/big-data/real-time-analytics-with-amazon-redshift-streaming-ingestion/
https://aws.amazon.com/jp/blogs/big-data/using-the-amazon-redshift-data-api-to-interact-with-amazon-redshift-clusters/
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/t_Loading-data-from-S3.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/c_best-practices-single-copy-command.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/t_Unloading_tables.html
https://docs.aws.amazon.com/ja_jp/redshift/latest/dg/t_rls.html

### [**Amazon API Gateway**](https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/welcome.html)
https://docs.aws.amazon.com/ja_jp/lambda/latest/dg/services-apigateway-tutorial.html

### [**AWS Systems Manager**](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/what-is-systems-manager.html)
https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/systems-manager-parameter-store.html

### [**AWS Database Migration Service (AWS DMS)**](https://docs.aws.amazon.com/ja_jp/dms/latest/userguide/Welcome.html)
https://docs.aws.amazon.com/ja_jp/dms/latest/userguide/CHAP_Task.CDC.html
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Troubleshooting_Latency.html

### [**Amazon VPC**](https://docs.aws.amazon.com/ja_jp/vpc/latest/privatelink/what-is-privatelink.html)
https://docs.aws.amazon.com/ja_jp/vpc/latest/privatelink/vpc-endpoints-s3.html
https://docs.aws.amazon.com/ja_jp/vpc/latest/userguide/vpc-network-acls.html

### [**AWS Key Management Service (AWS KMS)**](https://docs.aws.amazon.com/ja_jp/kms/latest/developerguide/overview.html)
https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/UsingDSSEncryption.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
https://docs.aws.amazon.com/ja_jp/kms/latest/developerguide/key-policy-modifying-external-accounts.html

### [**Amazon Elastic Block Store (Amazon EBS)**](https://docs.aws.amazon.com/ja_jp/ebs/latest/userguide/what-is-ebs.html)
https://docs.aws.amazon.com/ja_jp/ebs/latest/userguide/ebs-modify-volume.html

### [**Amazon Elastic File System (Amazon EFS)**](https://docs.aws.amazon.com/ja_jp/efs/latest/ug/whatisefs.html)
https://docs.aws.amazon.com/ja_jp/efs/latest/ug/accessing-fs.html

### [**Amazon S3**](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/Welcome.html)
https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/Versioning.html
https://aws.amazon.com/jp/blogs/aws/introducing-amazon-s3-object-lambda-use-your-code-to-process-data-as-it-is-being-retrieved-from-s3/
https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html
https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/selecting-content-from-objects.html
