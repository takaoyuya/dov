# Email
 
[Internet Message Format: RFC5322](https://www.rfc-editor.org/rfc/rfc5322)

###  Total Length(local-part@domain)
  - local-part: 64 octets MAX
  - domain: 255 octets MAX
  - local-part@domain ：256 octets MAX

### Local-part
  - 入力可能
      - アルファベット52文字 
      - 数字10文字
      - 記号19文字：! # $ % & ' * + - / = ? ^ _ ` { | } ~
  - ドット（.）：先頭と末尾以外、かつ連続しなければ入力可能
      - o.k@email.com
      - ng1.@email.com
      - .ng2@email.com
      - n..g3@email.com
  - quoted-string（ダブルクオート・バックスラッシュでくくると使える）
      - 記号10文字 → ( ) , : ; < > @ [ ]

### Domain
##### ユニコードドメインも利用可能：Punycode（xn--）変換される
- ❤️🍺.ws

[7月17日は世界絵文字デー](https://prtimes.jp/main/html/rd/p/000000407.000006942.html)

### メール 認証
- [DMARC、DKIM、SPFとは](https://www.cloudflare.com/ja-jp/learning/email-security/dmarc-dkim-spf/)
- [SPF, DKIMの特徴と違い](https://sendgrid.kke.co.jp/blog/?p=10121)
  - [DMARC：認証されなかったメールを迷惑メールに振り分けるか、まとめてブロックするかコントロールする]()
https://sendgrid.kke.co.jp/blog/?p=3137)
  - [SPF：IPアドレス認証（DNSサーバが送信側のIPアドレスを登録）](https://sendgrid.kke.co.jp/blog/?p=3509)
  - [DKIM（RFC6376）](https://www.rfc-editor.org/rfc/rfc6376)：電子署名認証（送信側が秘密鍵による電子署名を付与、受信側が公開鍵で検証する）
- [DMARC検証](https://domain-checker.valimail.com/dmarc/)

### DNSレコード
[DNSレコードとは](https://www.cloudflare.com/ja-jp/learning/dns/dns-records/)
- CNAMEレコード：他のレコード（A、TXT）と共存できない。（名前解決できなくなる）
- A（AAAA）レコード
- MXレコード
- TXTレコード
- SOAレコード
- PTRレコード 

### その他
#### Gmail
- [Gmail の制限とポリシー](https://support.google.com/a/topic/28609?hl=ja&ref_topic=9202&sjid=428464682027573043-AP)
- エイリアス機能（アドレス拡張）：local-partの直後に+つけて、テスト利用推奨

#### Amazon SES
[バウンスレート、苦情レート（迷惑メールを報告）がAmazon SESチームの定めたレートを越えると容赦なく停止](https://repost.aws/ja/knowledge-center/ses-reputation-dashboard-bounce-rate)


<br>

### References
##### メール送信テスト
- [swaks](https://github.com/jetmore/swaks)