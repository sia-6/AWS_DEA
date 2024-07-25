# AWS Glue
https://docs.aws.amazon.com/ja_jp/glue/latest/dg/what-is-glue.html
### AWS Glue ジョブ
AWS Glue ジョブは、データの抽出、変換、ロード（ETL）プロセスを自動化するためのタスクです。AWS GlueはフルマネージドのETLサービスであり、データの準備と統合を簡素化します。Glueジョブは、S3、RDS、Redshiftなどのデータソースからデータを抽出し、変換処理を行い、最終的にターゲットのデータストアにロードする一連のプロセスを含みます。

### AWS Glue DataBrew
AWS Glue DataBrew は、データのクリーニング、正規化、変換のためのフルマネージド型のビジュアルデータ準備サービスです。ETL とは異なり、操作する記述コードがないという点で AWS Glue ETL とは異なります。 DataBrew には、データ変換ジョブを作成および管理するためのビジュアル point-and-click インターフェイスを備えた 250 を超える組み込み変換が用意されています。
https://docs.aws.amazon.com/ja_jp/prescriptive-guidance/latest/serverless-etl-aws-glue/databrew.html#:~:text=AWS%20Glue%20DataBrew%20%E3%81%AF%E3%80%81%E3%83%87%E3%83%BC%E3%82%BF,ETL%20%E3%81%A8%E3%81%AF%E7%95%B0%E3%81%AA%E3%82%8A%E3%81%BE%E3%81%99%E3%80%82

### AWS Glue Studio
AWS Glue Studioは、AWS Glueでのデータ統合ジョブを簡単に作成、実行、監視できる新しいグラフィカルインターフェースです1. データ変換ワークフローを視覚的に構成し、AWS GlueのApache SparkベースのサーバーレスETLエンジンでシームレスに実行できます。

### AWS Glue クローラー
AWS Glue クローラーは、データソースからメタデータを自動的に収集し、AWS Glue データカタログにテーブル定義を作成するツールです。これにより、データの構造を簡単に把握し、クエリや分析に利用できるようになります。クローラーは、データソースをスキャンし、スキーマ情報（列名、データ型、パーティション情報など）を収集して、データカタログに登録します。

### AWS Glueワークフロー
AWS Glueワークフローは、データの抽出、変換、ロード（ETL）プロセスを自動化するために複数のジョブやトリガーを統合して管理するための機能です。ワークフローを使用することで、複数のETLタスクをシーケンシャルまたは並列に実行し、データ処理のパイプラインを構築、監視、管理することができます。

### AWS Glue Connections
AWS Glueジョブやクローラーがデータソースに接続するための設定情報を提供します。データエンジニアは、データストア（例：Amazon RDS、Amazon Redshift、またはオンプレミスのデータベース）にアクセスするために必要な接続情報を定義し、それをAWS Glueジョブやクローラーに使用させることができます。

# Amazon Athena
https://docs.aws.amazon.com/ja_jp/athena/latest/ug/what-is.html

# Apache Spark
https://qiita.com/taka_yayoi/items/31190da754106b2d284e
- ブロードキャスト結合機能

https://aws.amazon.com/jp/what-is/apache-spark/

# AWS Lake Formation
AWS Lake Formationは、データレイクの構築、管理、セキュリティを簡素化するためのフルマネージドサービスです。データレイクは、様々なソースからの構造化データ、半構造化データ、非構造化データを中央のリポジトリに集約し、分析や機械学習のために容易にアクセスできるようにするシステムです。Lake Formationは、このデータレイクを迅速に設定し、セキュリティを確保し、データガバナンスを実現するためのツールと機能を提供します。

https://docs.aws.amazon.com/ja_jp/lake-formation/latest/dg/cbac-tutorial.html

# Amazon Data Firehose
https://docs.aws.amazon.com/ja_jp/firehose/latest/dev/what-is-this-service.html

- ストリーミングデータをキャプチャ、変換、データストアにロードする機能により、イベントログなどの大量のステートレストランザクションを処理する。

# Amazon S3
https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/Welcome.html
- Amazon S3イベント通知
  S3バケットで特定のイベントが発生したときに通知を受け取ることができる。

# Amazon EMR (Elastic MapReduce)
https://docs.aws.amazon.com/ja_jp/emr/latest/ManagementGuide/emr-what-is-emr.html
クラスターがEMRの中心的コンポーネントはクラスターと呼ぶ。クラスターはAmazon EC2インスタンスの集合で、クラスター内の各インスタンスは、ノードと呼ばれる。各ノードには、クラスター内にロールがあり、ノードタイプと呼ばれ、プライマリノード、コアノード、タスクノードがある。また、Amazon EMRは、各ノードタイプにさまざまなソフトウェアコンポーネントをインストールし、Apache Hadoopなどの分散型アプリケーションでのロールを各ノードに付与する。

# Amazon MSK (Amazon Managed Streaming for Apache Kafka)
https://docs.aws.amazon.com/ja_jp/msk/latest/developerguide/what-is-msk.html#:~:text=Amazon%20Managed%20Streaming%20for%20Apache%20Kafka%20(Amazon%20MSK)%20%E3%81%AF%E3%80%81,%E3%81%99%E3%82%8B%E3%80%81%E3%83%95%E3%83%AB%E3%83%9E%E3%83%8D%E3%83%BC%E3%82%B8%E3%83%89%E3%82%B5%E3%83%BC%E3%83%93%E3%82%B9%E3%81%A7%E3%81%99%E3%80%82
分散型ストリーミングプラットフォームであり、リアルタイムデータの取り込み、処理、分析のために使用される。
リアルタイムデータストリーミング、イベント駆動型アーキテクチャ、ログ収集とモニタリング、データパイプラインの構築、メッセージブローカーとしての使用などに適している。

## Apache Kafka

# Amazon DynamoDB
https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/Introduction.html

- 低レイテンシー、高可用性、およびリージョン間レプリケーションを提供し、ステートフルトランザクションを処理するのに最適。

# AWS Data Exchange
https://docs.aws.amazon.com/ja_jp/data-exchange/latest/userguide/what-is.html#:~:text=AWS%20Data%20Exchange%20%E3%81%AF%E3%80%81AWS,%E8%BF%BD%E8%B7%A1%E3%81%8A%E3%82%88%E3%81%B3%E7%AE%A1%E7%90%86%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%99%E3%80%82
AWS Data Exchange はクラウド内のサードパーティデータを検出してサブスクライブするために特別に設計されており、これらのデータセットへの直接 API アクセスを提供します。
サードパーティデータを購入、配布、および管理するためのマネージドサービスです。企業や個人は、様々な業界のデータセットを簡単に検索し、購読して利用することができます。このサービスは、データプロバイダーがデータをセキュアに配布し、データ消費者が簡単にアクセスできるようにすることを目的としています。

# Amazon Managed Workflows for Apache Airflow (Amazon MWAA)
https://docs.aws.amazon.com/ja_jp/mwaa/latest/userguide/what-is-mwaa.html#:~:text=Amazon%20Managed%20Workflows%20for%20Apache%20Airflow%20%E3%81%AF%E3%80%81%E3%80%8CApache%20Airflow%20%E3%80%8D,%E3%81%9F%E3%82%81%E3%81%AB%E4%BD%BF%E7%94%A8%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%99%E3%80%82

## Apache Airflow
Apache Airflowは、データパイプラインのスケジューリングとモニタリングを行うためのオープンソースのワークフローオーケストレーションツールです。Airflowを使用すると、複雑なデータ処理タスクを定義し、依存関係を管理し、スケジュールに基づいて自動的に実行することができます。

# Amazon Redshift Data
https://docs.aws.amazon.com/ja_jp/redshift/latest/mgmt/welcome.html
Redshift Data API

------------------------

## ステートフルトランザクションとステートレストランザクション

### ステートフルトランザクション (Stateful Transaction)

#### 特徴
- **状態の維持**: ステートフルトランザクションは、トランザクションの実行中にその状態を保持します。トランザクションの各ステップが前のステップの出力に依存するため、一貫性と整合性が重要です。
- **高い整合性**: 一連の処理が全て成功するか、全て失敗するかのいずれかです。ACID (Atomicity, Consistency, Isolation, Durability) 特性をサポートすることが多いです。
- **トランザクション管理**: ロールバックやコミットなどの操作が可能であり、失敗した場合には一貫性を保つために全ての操作を元に戻すことができます。

#### 適用例
- **データベーストランザクション**: SQL データベースでの複雑な取引処理など。例えば、銀行の振込処理では、送金元の口座から引き落とし、送金先の口座に入金という一連の操作がすべて成功するか失敗するかを保証します。
- **ワークフロー管理**: AWS Step Functions などを使用して、状態を保持しながら複数のステップを順に実行するワークフローを管理します。

#### AWS サービス例
- **Amazon RDS**: リレーショナルデータベースでトランザクション管理を行います。
- **AWS Step Functions**: ステートマシンを使って複雑なワークフローを管理します。

### ステートレストランザクション (Stateless Transaction)

#### 特徴
- **状態の非依存性**: 各リクエストが独立して処理され、以前のリクエストの状態に依存しません。このため、各リクエストは自己完結型であり、他のリクエストからの影響を受けません。
- **高いスケーラビリティ**: ステートレスな処理は、同時に多くのリクエストを処理できるため、スケーラビリティが高いです。
- **簡単なトランザクション管理**: 各リクエストは独立しているため、複雑なトランザクション管理は不要です。

#### 適用例
- **ウェブリクエスト**: HTTP リクエストなど。各リクエストは独立して処理され、ステートレスであることが多いです。
- **マイクロサービスアーキテクチャ**: 各サービスが独立して機能し、状態を持たずにリクエストを処理します。

#### AWS サービス例
- **AWS Lambda**: 各実行が独立した関数を実行し、ステートレスで処理を行います。
- **Amazon API Gateway**: RESTful API を提供し、各リクエストが独立して処理されます。

## JDBC (Java Database Connectivity)
JDBC (Java Database Connectivity) は、Javaアプリケーションがデータベースと対話するための標準APIです。JDBCを使用することで、Javaアプリケーションはリレーショナルデータベースに接続し、SQLクエリを実行し、結果を処理することができます。JDBCはJavaプラットフォームの一部として提供されており、データベース独立性を確保しつつ、各種データベースへの接続を容易にします。

## ODBC (Open Database Connectivity) 
ODBC (Open Database Connectivity) は、Windows環境で標準化されたデータベースアクセスAPIです。ODBCを使用することで、アプリケーションは特定のデータベースに依存せず、共通のインターフェースを介してさまざまなデータベースに接続できます。ODBCは、Microsoftによって開発され、Windowsプラットフォームに広く採用されています。


## データメッシュ
データメッシュは、分散型かつ非中心の所有権を通じてデータセキュリティに関する高度な課題を解決するアーキテクチャフレームワークです。
https://aws.amazon.com/jp/what-is/data-mesh/

