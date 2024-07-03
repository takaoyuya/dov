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

--- 