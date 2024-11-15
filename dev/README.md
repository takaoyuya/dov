# Dev Lifecycle
□カレンダー（As of 2024 / 11）
1月
2月
3月
4月
- （EVENT）DevOpsDays Tokyo

5月
- （EVENT）AWS Summit Online
- （EVENT）RubyKaigi
- （EVENT）Google I/O
- （EVENT）WWDC/Apple

6月
- ECMAScript（TC39）
- （EVENT）Interop Tokyo
- （EVENT）Developers Summit Boost

7月
- （EVENT）Developers Summit Summer（デブサミ）

8月
- （EVENT）Next Tokyo： [’24](https://goo.gle/3YMnwWv)

9月
- （EVENT）新製品発表/Apple

10月
- Python（5年サポート）：（★）
- PostgreSQL（5年サポート）（★）
- （EVENT）：グッドデザイン賞（結果発表）

11月
- （EVENT）PostgreSQLカンファレンス

12月
- Ruby：12/25固定（★）
- （EVENT）AWS re:Invent： [Recap](https://aws.amazon.com/jp/events/reinvent-recap)
- （EVENT）Google DevFest 

□通年
- HTML Living Standard
- https://roadmap.sh/roadmaps

# Dev Ref
■ Google Developer：
- https://developers.googleblog.com/
- https://developers-jp.googleblog.com/
- https://cloud.google.com/blog/ja
- https://io.google/
- https://bughunters.google.com/
- https://testing.googleblog.com/
- https://research.google/blog/
- https://rework.withgoogle.com/

■ MS：
https://developer.mozilla.org/en-US/blog/

# My Stacks
[my stack(stackshare)](https://stackshare.io/takaoyuya/my-stack)

### Langage
- HTML：[Examples(w3schools)](https://www.w3schools.com/html/html_examples.asp), [Compatibility(caniuse)](https://caniuse.com/)
- CSS（SCSS）：[Examples(w3schools)](https://www.w3schools.com/css/default.asp), [Updates (web.dev)](https://web.dev/series/baseline-newly-available?hl=ja)
  - Tailwind
- JS
  - TS：[Release](https://github.com/Microsoft/TypeScript/releases)
    - [5.5](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-5-5.html)
    - [5.6](https://devblogs.microsoft.com/typescript/announcing-typescript-5-6/)

  - Node：[Release](https://github.com/nodejs/release#release-schedule)
  - FW
    - Anguler：[Release Cycle](https://angular.jp/reference/releases#%E3%83%AA%E3%83%AA%E3%83%BC%E3%82%B9%E3%82%B9%E3%82%B1%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB)
    - Vue：[Release](https://vuejs.org/about/releases.html)
      - [3.5](https://blog.vuejs.org/posts/vue-3-5)：2024/09
    - React

- Python（every Oct）[Release Cycle](https://devguide.python.org/versions/), [Updates](https://docs.python.org/ja/3/whatsnew/index.html)
  - [3.13](https://docs.python.org/ja/3/whatsnew/3.13.html)：2024/10
- [Ruby](https://www.ruby-lang.org/en/downloads/branches/)：[3.3](https://www.ruby-lang.org/ja/news/2023/12/25/ruby-3-3-0-released/)
  - Rails
- Java：Spring
- C#：.Net([Release](https://dotnet.microsoft.com/ja-jp/platform/support/policy/dotnet-core))
  - [C#13](https://learn.microsoft.com/ja-jp/dotnet/csharp/whats-new/csharp-13)
- [GO](https://go.dev/doc/devel/release)
- PHP：

### DB
  - RDB：[Postgresql](https://www.postgresql.org/support/versioning/)
  - Search：Elasticsearch / Apache Solr
  - Package Manager Tools

### Build
  - OS
    - Linux（BSD系）：Unix/Darwin/MacOS（homebrew）
    - Linux：（GNU系）
      - apt：Debian系（Ubuntu）
      - yum：Red Hat系（Fedora、CentOS、RHELなど）
      - rpm：(Red Hat Package Manager)
      - pacman：Arch系（Arch Linux）
      - zypper：SUSE系（Open SUSE）
    - Lang：npm / yarn / gem / pip / composer
- Dependency Management
  - Java
    - Gradle（Java、Kotlin：build.gradle）
    - Apache Maven（Java：pom.xml）
  - JS
    - Vite（ヴィート）：高速ホットリロード
    - Webpack ：依存解決して、JSをモジュール化できる（Rspackへの切り替え推奨）
    - Rspack
    - Ruby：Bundler（Gemfile）
    - PHP：Composer	
- Formatter：ESLint / Prettier / TSLint / RuboCop / SonarQube / SonarLint / Stylelint
- CI/CD：Jenkins / GitHub Actions / Google Cloud Build / AWS CodePipeline

### Test
- API Clients：Postman（[Learn](https://learning.postman.com/) / [blog](https://blog.postman.com/)）/Swagger UI / Soap UI/Bruno
- Browser Testing：Selenium / BrowserStack
- Testing Frameworks Tools
  - xUnit系（JUnit 、QUnit）
  - Java：JUnit4/5
  - JS：Jasmine / Karma / Jest
  - Ruby：RSpec
  - Python：pytest
- Code Coverage：Codecov
- Performance Testing Tools
  - [Google Lighthouse](https://developer.chrome.com/docs/lighthouse/performance/)（Website）
  - Apache JMeter
- Monitoring
  - Visialize：Kibana / Grafana
  - Monitoring Tools：Kibana / Grafana / Prometheus
  - Performance Monitoring：New Relic / Datadog

- SaaS
  - CDN：Akamai / Netlify / Fastly / CloudFlare
  - AuthN/Z：Auth0 / Keycloak / Amazon Cognito / Firebase Authentication
  - e-Mail：SendGrid

- Open Source
  - Web Cache Tools：Varnish
  - Load Balancer / Reverse Proxy
    - HAProxy
    - Envoy：サイドカー用（Istioのデフォルトサイドカー）
  - WAF：ModSecurity