# Database

## Postgresql

### Release cycle
５年サポート
[リリースサイクル　](https://www.postgresql.org/support/versioning)
- 16：2023/9
- 15：2022/10
    - ★インメモリとディスク上のソートアルゴリズムが改善（25%〜400%の速度向上）
    - ライトアヘッドログ（WAL）でLZ4とZstandard (zstd) の圧縮をサポートを追加
    - ★SQL標準のMERGEコマンドが追加→INSERT、UPDATE、DELETEを一つの文に含める条件付きSQL文が利用可能
    - ★正規表現が使用できる新しい関数regexp_count()、 regexp_instr()等 追加
    - 論理レプリケーションでの2フェーズコミットもサポート
- 14：2021/10
    - ★複数のクエリや結果を1つのネットワークトランザクションで送受信できることでクライアントのサーバに対する待ち時間が短くなる「**パイプラインモード**」が追加
    - サブスクライバに大規模なトランザクションを適用する際のパフォーマンスが大幅向上
    - 並列シーケンシャルスキャンのパフォーマンスの向上
    - 「PL/pgSQL」が「RETURN QUERY」コマンドを使用して並列クエリを実行する機
    - ★「REFRESH MATERIALIZED VIEW」が並列クエリを実行する機能追加

#### Command
- Show timezone; ：タイムゾーンを確認
- Show all;全設定確認
- Select current_timestamp;：タイムスタンプ確認
- Select setting from pg_settings where name = 'statement_timeout’：タイムアウト設定確認
- SHOW TRANSACTION ISOLATION LEVEL;分離レベル確認

#### References
-  [クエリサンプル](https://gist.github.com/linyows/d81319d00543e6d0093136fd7668637b)
-  [RDS（PostgreSQL）](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html)
   - [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.DBVersions)
   - [Release EOL](https://docs.aws.amazon.com/AmazonRDS/latest/PostgreSQLReleaseNotes/postgresql-release-calendar.html)
- チューニングガイド
  - Citus Data（米マイクロソフト買収：PostgreSQL用の分散データベースエンジンの開発）
      - https://www.citusdata.com/blog/2018/02/22/seven-tips-for-dealing-with-postgres-locks/
  - あまり知られていないPostgreSQLの機能：https://postd.cc/postgresql-unknown-features/#08
      - 連番：SERIAL（非推奨）→ GENERATED ALWAYS：連番項目を指定できないようにする（一意性制約違反が発生しにくくなる）
      - パターンマッチ：regexp（例：~ ANY(ARRAY['@gmail\.com$', '@yahoo\.com$'])）
      - UPSERT：クエリ例：INSERT ON CONFLICT
      - DISTINCT ON：重複削除したカラムの、他カラム情報が欲しい
      - gen_random_uuid()：ランダムなUUID（バージョン4）を生成する
  - ORDER(select)：https://www.postgresql.org/docs/16/sql-select.html
  - クエリサンプル
      - https://gist.github.com/linyows/d81319d00543e6d0093136fd7668637b
      - https://repost.aws/ja/knowledge-center/rds-postgresql-replication-lag
      - https://qiita.com/mkyz08/items/ff4474a5546a62adc580
      - https://learn.microsoft.com/ja-jp/azure/cosmos-db/postgresql/howto-useful-diagnostic-queries

- Postgres: https://www.postgresql.jp/document/current/index.html
    - Postgres権限：https://www.postgresql.jp/document/8.4/html/sql-grant.html
    - Postgresデータタイプ：https://www.postgresql.org/docs/14/functions-formatting.html
    - Postgres クエリサンプル：https://www.postgresqltutorial.com/
    - PostgresパフォーマンスTips：https://www.postgresql.org/docs/current/performance-tips.html
