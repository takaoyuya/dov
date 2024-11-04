# Lanuguege / Framework

## ECMAScript


### Release cycle
[リリースノート(TC39)](https://github.com/tc39/ecma262/releases)
* ES2024：2024/6
* ES2023：2023/6
* ES2022：2022/6
    * ★クラスフィールド宣言が可能に（★★★プライベートフィールドには接頭辞に#を利用）
    * ★Array, String, TypedArray の .at()：負の整数を指定すると配列の末尾から参照
    * ★Top-Level Await：asyncなしでもトップレベルでawaitが利用できるよう変更
    * Object.hasOwn()追加
    * Error.cause：第2引数にcauseフィールドを含むオブジェクトを指定可能に
    * RegExp Match Indices：正規表現にマッチインデックス機能（/dフラグ）が追加
* ES2021：2021/6
    * ★_区切り数値：100_000_000; // 1億（100,000,000）
    * .replaceAll()：マッチした文字列をすべて置換
    * Promise.any：最初のresolveを待つ（Promise.race()との違いはresolve/reject両方待つ）
    * ??=演算子：nullかundefinedの時に代入
    * ★||=演算子：falsyな時に代入
    * ★&&=演算子：truthyな時に代入
* ES2020：2020/6
    * 任意精度整数(BigInt)：2^53（10億以上の数字を扱える）
    * ★Nullish Coalescing： ??
    * ★Optional Chaining：?
    * string.matchAll()：イテレータを返す
    * ダイナミックインポート(Dynamic Import)：promiseを返す

#### References
[ECMAScript 202x](https://www.w3schools.com/js/js_2024.asp)
[compat-table](https://compat-table.github.io/compat-table/es6/)

--- 

## TypeScript
### Release cycle
3ヶ月ごとのマイナーアップ（Feb・Mar・Aug・Dec）

[リリースノート（Git）](https://github.com/Microsoft/TypeScript/releases)
[リリースノート](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-5-2.html)


- 5.5：2024/6
- 5.4：2024/3
- 5.3：2023/11
- 5.2：2023/8
    - using宣言
    - Decorator（★）
- 5.0：2023/Mar
    - Decorators（★）
    - All enums Are Union enums（★）

#### References
--- 
## NodeJS

メジャーバージョンは６ヶ月ごと、偶数がLTSサポート：v18（10月25～）
### Release cycle
[リリーススケジュール](https://github.com/nodejs/release#release-schedule)

- 22：2024/4（LTS）
- 20：2023/4（LTS）
    - URLパーサー「Ada」がv2.0へと更新
    - 「Web Crypto API」が利用可能
- 19：2022/10
    - ★HTTP(S)/1.1 KeepAliveが既定で有効化I'd appreciate it if you could reply to me.
    - V8（v10.7）の新機能：数値のフォーマットで要望の多かった箇所が改善
- 18：2022/4（LTS）
    - fetch API（undiciベース：指定したURLのコンテンツを取得）が利用可能（★）
    - Web Streams APIが利用可能
    - HTTPタイムアウトの設定追加（★）
        - server.headersTimeout：HTTPヘッダーの受信完了までの待機時間。既定値は60秒
        - server.requestTimeout：HTTPリクエスト全体の受信完了までの待機時間。既定値は5分
    - V8（v10.1）の新機能：配列メソッド「findLast()」「findLastIndex()」が利用可能

#### References

--- 

## React.js

### Release cycle
リリースサイクル不明
[リリースノート](https://legacy.reactjs.org/versions)

- 19：TBD
- 18：2022/3/29
- 17：2020/10

#### References
--- 

## Vue.js

### Release cycle
[リリースノート](https://vuejs.org/about/releases.html)
[What's New in 3.4](https://blog.vuejs.org/posts/vue-3-4)

###　History
- 3.4：2023/12
- 3：2020/09
    - filterは削除
    - TypeScriptをサポート
    - Composition APIで大規模なコンポーネントが作成しやすくなった

#### References
--- 

## Angular

### Release cycle
6ヶ月ごとのメジャーアップ（メジャーリリースは18ヶ月サポート）
[リリースノート](https://angular.jp/guide/releases/)

###　History
- 17：2023/11
- 16：2023/5
- 15：2022/11
- 14：2022/6
- 13：2021/11
- 12：2021/5

#### References
--- 
