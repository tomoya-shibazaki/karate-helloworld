# karate-helloworld
## requirement
- Java
- Maven

## Quickstart
```
mvn archetype:generate \
-DarchetypeGroupId=com.intuit.karate \
-DarchetypeArtifactId=karate-archetype \
-DarchetypeVersion=1.0.1 \
-DgroupId=com.mycompany \
-DartifactId=myproject
```
## tree
```
.
├── pom.xml
├── src
   └── test
       └── java
           ├── examples
           │   ├── ExamplesTest.java
           │   └── users
           │       ├── UsersRunner.java
           │       └── users.feature
           ├── karate-config.js
           └── logback-test.xml

```

```
cd myproject
```

```
mvn test
```

### terminal
```
[INFO] Scanning for projects...
[INFO] 
[INFO] ----------------------< com.mycompany:myproject >-----------------------
[INFO] Building myproject 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ myproject ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /Users/tomoyashibazaki/karate-helloworld/myproject/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.8.1:compile (default-compile) @ myproject ---
[INFO] No sources to compile
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ myproject ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 3 resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.8.1:testCompile (default-testCompile) @ myproject ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 2 source files to /Users/tomoyashibazaki/karate-helloworld/myproject/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:2.22.2:test (default-test) @ myproject ---
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running examples.ExamplesTest
00:48:53.454 [main] DEBUG com.intuit.karate.Suite - [config] classpath:karate-config.js
00:48:53.829 [pool-1-thread-2] INFO  com.intuit.karate - karate.env system property was: null 
00:48:53.829 [pool-1-thread-1] INFO  com.intuit.karate - karate.env system property was: null 
00:48:53.968 [pool-1-thread-1] DEBUG com.intuit.karate - request:
1 > GET https://jsonplaceholder.typicode.com/users
1 > Host: jsonplaceholder.typicode.com
1 > Connection: Keep-Alive
1 > User-Agent: Apache-HttpClient/4.5.13 (Java/17)
1 > Accept-Encoding: gzip,deflate


00:48:53.968 [pool-1-thread-2] DEBUG com.intuit.karate - request:
1 > POST https://jsonplaceholder.typicode.com/users
1 > Content-Type: application/json; charset=UTF-8
1 > Content-Length: 160
1 > Host: jsonplaceholder.typicode.com
1 > Connection: Keep-Alive
1 > User-Agent: Apache-HttpClient/4.5.13 (Java/17)
1 > Accept-Encoding: gzip,deflate
{"address":{"zipcode":"54321-6789","suite":"Apt. 123","city":"Electri","street":"Has No Name"},"name":"Test User","email":"test@user.com","username":"testuser"}

00:48:54.184 [pool-1-thread-1] DEBUG com.intuit.karate - response time in milliseconds: 215
1 < 200
1 < Date: Mon, 28 Jun 2021 15:48:54 GMT
1 < Content-Type: application/json; charset=utf-8
1 < Transfer-Encoding: chunked
1 < Connection: keep-alive
1 < X-Powered-By: Express
1 < X-Ratelimit-Limit: 1000
1 < X-Ratelimit-Remaining: 999
1 < X-Ratelimit-Reset: 1622687474
1 < Vary: Origin, Accept-Encoding
1 < Access-Control-Allow-Credentials: true
1 < Cache-Control: max-age=43200
1 < Pragma: no-cache
1 < Expires: -1
1 < X-Content-Type-Options: nosniff
1 < Etag: W/"160d-1eMSsxeJRfnVLRBmYJSbCiJZ1qQ"
1 < Via: 1.1 vegur
1 < CF-Cache-Status: HIT
1 < Age: 1121
1 < cf-request-id: 0af4e83f2500002098483b0000000001
1 < Expect-CT: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
1 < Report-To: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v2?s=nM%2B7eUtT7%2FzalkT7Sfr1kXEdiY3KgpQu42Sgu3yvtOyi%2FRcEeAgNghxxS5u527X1NEglzR15II8tbHlVHHxdJDLhI7Dq2%2F0jVcFyioOrSa29sP%2FZziuO35PJkwc6j3P2fDposLbkuWGLeA%3D%3D"}],"group":"cf-nel","max_age":604800}
1 < NEL: {"report_to":"cf-nel","max_age":604800}
1 < Server: cloudflare
1 < CF-RAY: 66680fdea85c2098-NRT
1 < alt-svc: h3-27=":443"; ma=86400, h3-28=":443"; ma=86400, h3-29=":443"; ma=86400, h3=":443"; ma=86400
[{"website":"hildegard.org","address":{"zipcode":"92998-3874","geo":{"lng":"81.1496","lat":"-37.3159"},"suite":"Apt. 556","city":"Gwenborough","street":"Kulas Light"},"phone":"1-770-736-8031 x56442","name":"Leanne Graham","company":{"bs":"harness real-time e-markets","catchPhrase":"Multi-layered client-server neural-net","name":"Romaguera-Crona"},"id":1,"email":"Sincere@april.biz","username":"Bret"},{"website":"anastasia.net","address":{"zipcode":"90566-7771","geo":{"lng":"-34.4618","lat":"-43.9509"},"suite":"Suite 879","city":"Wisokyburgh","street":"Victor Plains"},"phone":"010-692-6593 x09125","name":"Ervin Howell","company":{"bs":"synergize scalable supply-chains","catchPhrase":"Proactive didactic contingency","name":"Deckow-Crist"},"id":2,"email":"Shanna@melissa.tv","username":"Antonette"},{"website":"ramiro.info","address":{"zipcode":"59590-4157","geo":{"lng":"-47.0653","lat":"-68.6102"},"suite":"Suite 847","city":"McKenziehaven","street":"Douglas Extension"},"phone":"1-463-123-4447","name":"Clementine Bauch","company":{"bs":"e-enable strategic applications","catchPhrase":"Face to face bifurcated interface","name":"Romaguera-Jacobson"},"id":3,"email":"Nathan@yesenia.net","username":"Samantha"},{"website":"kale.biz","address":{"zipcode":"53919-4257","geo":{"lng":"-164.2990","lat":"29.4572"},"suite":"Apt. 692","city":"South Elvis","street":"Hoeger Mall"},"phone":"493-170-9623 x156","name":"Patricia Lebsack","company":{"bs":"transition cutting-edge web services","catchPhrase":"Multi-tiered zero tolerance productivity","name":"Robel-Corkery"},"id":4,"email":"Julianne.OConner@kory.org","username":"Karianne"},{"website":"demarco.info","address":{"zipcode":"33263","geo":{"lng":"62.5342","lat":"-31.8129"},"suite":"Suite 351","city":"Roscoeview","street":"Skiles Walks"},"phone":"(254)954-1289","name":"Chelsey Dietrich","company":{"bs":"revolutionize end-to-end systems","catchPhrase":"User-centric fault-tolerant solution","name":"Keebler LLC"},"id":5,"email":"Lucio_Hettinger@annie.ca","username":"Kamren"},{"website":"ola.org","address":{"zipcode":"23505-1337","geo":{"lng":"71.7478","lat":"-71.4197"},"suite":"Apt. 950","city":"South Christy","street":"Norberto Crossing"},"phone":"1-477-935-8478 x6430","name":"Mrs. Dennis Schulist","company":{"bs":"e-enable innovative applications","catchPhrase":"Synchronised bottom-line interface","name":"Considine-Lockman"},"id":6,"email":"Karley_Dach@jasper.info","username":"Leopoldo_Corkery"},{"website":"elvis.io","address":{"zipcode":"58804-1099","geo":{"lng":"21.8984","lat":"24.8918"},"suite":"Suite 280","city":"Howemouth","street":"Rex Trail"},"phone":"210.067.6132","name":"Kurtis Weissnat","company":{"bs":"generate enterprise e-tailers","catchPhrase":"Configurable multimedia task-force","name":"Johns Group"},"id":7,"email":"Telly.Hoeger@billy.biz","username":"Elwyn.Skiles"},{"website":"jacynthe.com","address":{"zipcode":"45169","geo":{"lng":"-120.7677","lat":"-14.3990"},"suite":"Suite 729","city":"Aliyaview","street":"Ellsworth Summit"},"phone":"586.493.6943 x140","name":"Nicholas Runolfsdottir V","company":{"bs":"e-enable extensible e-tailers","catchPhrase":"Implemented secondary concept","name":"Abernathy Group"},"id":8,"email":"Sherwood@rosamond.me","username":"Maxime_Nienow"},{"website":"conrad.com","address":{"zipcode":"76495-3109","geo":{"lng":"-168.8889","lat":"24.6463"},"suite":"Suite 449","city":"Bartholomebury","street":"Dayna Park"},"phone":"(775)976-6794 x41206","name":"Glenna Reichert","company":{"bs":"aggregate real-time technologies","catchPhrase":"Switchable contextually-based project","name":"Yost and Sons"},"id":9,"email":"Chaim_McDermott@dana.io","username":"Delphine"},{"website":"ambrose.net","address":{"zipcode":"31428-2261","geo":{"lng":"57.2232","lat":"-38.2386"},"suite":"Suite 198","city":"Lebsackbury","street":"Kattie Turnpike"},"phone":"024-648-3804","name":"Clementina DuBuque","company":{"bs":"target end-to-end models","catchPhrase":"Centralized empowering task-force","name":"Hoeger LLC"},"id":10,"email":"Rey.Padberg@karina.biz","username":"Moriah.Stanton"}]
00:48:54.193 [pool-1-thread-1] DEBUG com.intuit.karate - request:
2 > GET https://jsonplaceholder.typicode.com/users/1
2 > Host: jsonplaceholder.typicode.com
2 > Connection: Keep-Alive
2 > User-Agent: Apache-HttpClient/4.5.13 (Java/17)
2 > Accept-Encoding: gzip,deflate


00:48:54.286 [pool-1-thread-1] DEBUG com.intuit.karate - response time in milliseconds: 92
2 < 200
2 < Date: Mon, 28 Jun 2021 15:48:54 GMT
2 < Content-Type: application/json; charset=utf-8
2 < Transfer-Encoding: chunked
2 < Connection: keep-alive
2 < X-Powered-By: Express
2 < X-Ratelimit-Limit: 1000
2 < X-Ratelimit-Remaining: 999
2 < X-Ratelimit-Reset: 1622687534
2 < Vary: Origin, Accept-Encoding
2 < Access-Control-Allow-Credentials: true
2 < Cache-Control: max-age=43200
2 < Pragma: no-cache
2 < Expires: -1
2 < X-Content-Type-Options: nosniff
2 < Etag: W/"1fd-+2Y3G3w049iSZtw5t1mzSnunngE"
2 < Via: 1.1 vegur
2 < CF-Cache-Status: HIT
2 < Age: 26892
2 < cf-request-id: 0af4e83f9200001ed49016d000000001
2 < Expect-CT: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
2 < Report-To: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v2?s=YBlbrEkAJHuTOlnzzEcZug%2BCwbvuazwoYGgiVEmnY0xMmQMCNE6IgFbaneG7sNHb6UrVWieTUgHREUFJgDbOit9gcPQhwZi9tovbU77h8QwU7b0is%2Btt69JySKu8szS2a1xXfQUwcZfhGQ%3D%3D"}],"group":"cf-nel","max_age":604800}
2 < NEL: {"report_to":"cf-nel","max_age":604800}
2 < Server: cloudflare
2 < CF-RAY: 66680fdf4caf1ed4-NRT
2 < alt-svc: h3-27=":443"; ma=86400, h3-28=":443"; ma=86400, h3-29=":443"; ma=86400, h3=":443"; ma=86400
{"website":"hildegard.org","address":{"zipcode":"92998-3874","geo":{"lng":"81.1496","lat":"-37.3159"},"suite":"Apt. 556","city":"Gwenborough","street":"Kulas Light"},"phone":"1-770-736-8031 x56442","name":"Leanne Graham","company":{"bs":"harness real-time e-markets","catchPhrase":"Multi-layered client-server neural-net","name":"Romaguera-Crona"},"id":1,"email":"Sincere@april.biz","username":"Bret"}
00:48:54.754 [pool-1-thread-2] DEBUG com.intuit.karate - response time in milliseconds: 786
1 < 201
1 < Date: Mon, 28 Jun 2021 15:48:54 GMT
1 < Content-Type: application/json; charset=utf-8
1 < Content-Length: 216
1 < Connection: keep-alive
1 < X-Powered-By: Express
1 < X-Ratelimit-Limit: 1000
1 < X-Ratelimit-Remaining: 999
1 < X-Ratelimit-Reset: 1624895338
1 < Vary: Origin, X-HTTP-Method-Override, Accept-Encoding
1 < Access-Control-Allow-Credentials: true
1 < Cache-Control: no-cache
1 < Pragma: no-cache
1 < Expires: -1
1 < Access-Control-Expose-Headers: Location
1 < Location: http://jsonplaceholder.typicode.com/users/11
1 < X-Content-Type-Options: nosniff
1 < Etag: W/"d8-pYV7+YuMGP2hxHPU9ARrf97ifDA"
1 < Via: 1.1 vegur
1 < CF-Cache-Status: DYNAMIC
1 < cf-request-id: 0af4e83f3700000b930498b000000001
1 < Expect-CT: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
1 < Report-To: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v2?s=AK76EKLOb9b8ZRZOpv%2BbcLUGhGIuVcsLV09952wT5Qc2GMAiLP1LgmdU%2FDv8bRUi5ACeKNtBZbnuBQ%2BZaCIYzKrgJaClWMwQnm8qiWPGg4iAO87AMRHQapyshjz471do7V%2B1%2FnxXHyxj5A%3D%3D"}],"group":"cf-nel","max_age":604800}
1 < NEL: {"report_to":"cf-nel","max_age":604800}
1 < Server: cloudflare
1 < CF-RAY: 66680fdebeef0b93-NRT
1 < alt-svc: h3-27=":443"; ma=86400, h3-28=":443"; ma=86400, h3-29=":443"; ma=86400, h3=":443"; ma=86400
{"address":{"zipcode":"54321-6789","suite":"Apt. 123","city":"Electri","street":"Has No Name"},"name":"Test User","id":11,"email":"test@user.com","username":"testuser"}
00:48:54.760 [pool-1-thread-2] INFO  com.intuit.karate - [print] created id is:  11 
---------------------------------------------------------
feature: classpath:examples/users/users.feature
scenarios:  2 | passed:  2 | failed:  0 | time: 1.3563
---------------------------------------------------------

00:48:55.003 [pool-2-thread-1] INFO  com.intuit.karate.Suite - <<pass>> feature 1 of 1 (0 remaining) classpath:examples/users/users.feature
Karate version: 1.0.1
======================================================
elapsed:   1.78 | threads:    5 | thread time: 1.36 
features:     1 | skipped:    0 | efficiency: 0.15
scenarios:    2 | passed:     2 | failed: 0
======================================================

HTML report: (paste into browser to view) | Karate version: 1.0.1
file:///Users/tomoyashibazaki/karate-helloworld/myproject/target/karate-reports/karate-summary.html
===================================================================

[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 1.919 s - in examples.ExamplesTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  3.348 s
[INFO] Finished at: 2021-06-29T00:48:55+09:00
[INFO] ------------------------------------------------------------------------
```

## tree
```
.
├── pom.xml
├── src
│   └── test
│       └── java
│           ├── examples
│           │   ├── ExamplesTest.java
│           │   └── users
│           │       ├── UsersRunner.java
│           │       └── users.feature
│           ├── karate-config.js
│           └── logback-test.xml
└── target
    ├── generated-test-sources
    │   └── test-annotations
    ├── karate-reports
    │   ├── examples.users.users.html
    │   ├── examples.users.users.karate-json.txt
    │   ├── favicon.ico
    │   ├── karate-logo.png
    │   ├── karate-logo.svg
    │   ├── karate-progress-json.txt
    │   ├── karate-summary-json.txt
    │   ├── karate-summary.html
    │   ├── karate-tags.html
    │   ├── karate-timeline.html
    │   └── res
    │       ├── bootstrap.min.css
    │       ├── bootstrap.min.js
    │       ├── jquery.min.js
    │       ├── jquery.tablesorter.min.js
    │       ├── karate-report.css
    │       └── karate-report.js
    ├── karate.log
    ├── maven-status
    │   └── maven-compiler-plugin
    │       └── testCompile
    │           └── default-testCompile
    │               ├── createdFiles.lst
    │               └── inputFiles.lst
    ├── surefire-reports
    │   ├── TEST-examples.ExamplesTest.xml
    │   └── examples.ExamplesTest.txt
    └── test-classes
        ├── examples
        │   ├── ExamplesTest.class
        │   └── users
        │       ├── UsersRunner.class
        │       └── users.feature
        ├── karate-config.js
        └── logback-test.xml

```

### browser
<img width="1440" alt="Screen Shot 2021-06-29 at 0 53 19" src="https://user-images.githubusercontent.com/24289696/123668048-ac64ea00-d875-11eb-8e8a-08114482e56c.png">

## reference
- https://github.com/intuit/karate
