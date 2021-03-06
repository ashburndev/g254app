# g254app
a simple Grails 2.5.4 web application

```
cd ~/g2projects
grails create-app g254app
cd g254app
tree
grails dependency-report
grails integrate-with --git
git init
git add .
git commit -a -m "first commit"
git status
git remote add origin git@github.com:ashburndev/g254app.git
git push -u origin master
```

```
ashburndave@dphnuc4:~/g2projects/g254app$ tree .
.
├── application.properties
├── grails-app
│   ├── assets
│   │   ├── images
│   │   │   ├── apple-touch-icon.png
│   │   │   ├── apple-touch-icon-retina.png
│   │   │   ├── favicon.ico
│   │   │   ├── grails_logo.png
│   │   │   ├── skin
│   │   │   │   ├── database_add.png
│   │   │   │   ├── database_delete.png
│   │   │   │   ├── database_edit.png
│   │   │   │   ├── database_save.png
│   │   │   │   ├── database_table.png
│   │   │   │   ├── exclamation.png
│   │   │   │   ├── house.png
│   │   │   │   ├── information.png
│   │   │   │   ├── shadow.jpg
│   │   │   │   ├── sorted_asc.gif
│   │   │   │   └── sorted_desc.gif
│   │   │   ├── spinner.gif
│   │   │   └── springsource.png
│   │   ├── javascripts
│   │   │   └── application.js
│   │   └── stylesheets
│   │       ├── application.css
│   │       ├── errors.css
│   │       ├── main.css
│   │       └── mobile.css
│   ├── conf
│   │   ├── BootStrap.groovy
│   │   ├── BuildConfig.groovy
│   │   ├── Config.groovy
│   │   ├── DataSource.groovy
│   │   ├── hibernate
│   │   ├── spring
│   │   │   └── resources.groovy
│   │   └── UrlMappings.groovy
│   ├── controllers
│   ├── domain
│   ├── i18n
│   │   ├── messages_cs_CZ.properties
│   │   ├── messages_da.properties
│   │   ├── messages_de.properties
│   │   ├── messages_es.properties
│   │   ├── messages_fr.properties
│   │   ├── messages_it.properties
│   │   ├── messages_ja.properties
│   │   ├── messages_nb.properties
│   │   ├── messages_nl.properties
│   │   ├── messages_pl.properties
│   │   ├── messages.properties
│   │   ├── messages_pt_BR.properties
│   │   ├── messages_pt_PT.properties
│   │   ├── messages_ru.properties
│   │   ├── messages_sv.properties
│   │   ├── messages_th.properties
│   │   └── messages_zh_CN.properties
│   ├── services
│   ├── taglib
│   ├── utils
│   └── views
│       ├── error.gsp
│       ├── index.gsp
│       └── layouts
│           └── main.gsp
├── grailsw
├── grailsw.bat
├── lib
├── scripts
├── src
│   ├── groovy
│   └── java
├── test
│   ├── integration
│   └── unit
├── web-app
│   ├── css
│   ├── images
│   ├── js
│   ├── META-INF
│   └── WEB-INF
│       ├── applicationContext.xml
│       ├── sitemesh.xml
│       └── tld
│           ├── grails.tld
│           ├── spring-form.tld
│           └── spring.tld
└── wrapper
    ├── grails-wrapper.properties
    ├── grails-wrapper-runtime-2.5.4.jar
    └── springloaded-1.2.4.RELEASE.jar

33 directories, 59 files
ashburndave@dphnuc4:~/g2projects/g254app$ 
```

```
ashburndave@dphnuc4:~/g2projects/g254app$ history | tail -5
 1859  tree .
 1860  grails help
 1861  grails help integrate-with
 1862  grails integrate-with --git
 1863  history | tail -5
ashburndave@dphnuc4:~/g2projects/g254app$ cat .gitignore 
*.iws
*Db.properties
*Db.script
.settings
stacktrace.log
/*.zip
/plugin.xml
/*.log
/*DB.*
/cobertura.ser
.DS_Store
/target/
/out/
/web-app/plugins
/web-app/WEB-INF/classes
/.link_to_grails_plugins/
/target-eclipse/
ashburndave@dphnuc4:~/g2projects/g254app$ 
```

```
ashburndave@dphnuc4:~/g2projects/g254app$ grails dependency-report

| Environment set to development.

build - Dependencies for the build system only (total: 33)
+--- xalan:serializer:2.7.2
+--- org.grails:grails-bootstrap:2.5.4
|    \--- org.apache.ant:ant-launcher:1.9.4
|    \--- org.apache.ant:ant-junit:1.9.4
|    \--- org.slf4j:jcl-over-slf4j:1.7.5
|    \--- org.codehaus.groovy:groovy-all:2.4.4
|    \--- jline:jline:2.12
|    \--- net.java.dev.jna:jna:4.0.0
|    \--- org.fusesource.jansi:jansi:1.11
|    \--- org.codehaus.gant:gant_groovy1.8:1.9.6
|    \--- org.apache.ant:ant-trax:1.7.1
|    \--- org.apache.ivy:ivy:2.3.0
|    \--- org.slf4j:slf4j-api:1.7.5
|    \--- org.apache.ant:ant:1.9.4
+--- org.grails:grails-project-api:2.5.4
+--- org.grails:grails-scripts:2.5.4
+--- org.grails:grails-docs:2.5.4
|    \--- org.jsoup:jsoup:1.7.3
|    \--- com.lowagie:itext:2.0.8
|         \--- bouncycastle:bcmail-jdk14:138
|         \--- bouncycastle:bcprov-jdk14:138
|    \--- commons-lang:commons-lang:2.6
|    \--- org.xhtmlrenderer:core-renderer:R8
|    \--- org.yaml:snakeyaml:1.8
|    \--- org.grails:grails-gdoc-engine:1.0.1
+--- org.grails.plugins:tomcat:7.0.55.3
|    \--- org.apache.tomcat:tomcat-catalina-ant:7.0.55
|    \--- org.apache.tomcat.embed:tomcat-embed-jasper:7.0.55
|         \--- org.apache.tomcat.embed:tomcat-embed-el:7.0.55
|    \--- org.apache.tomcat.embed:tomcat-embed-logging-log4j:7.0.55
|    \--- org.apache.tomcat.embed:tomcat-embed-websocket:7.0.55
|    \--- org.eclipse.jdt.core.compiler:ecj:3.7.2
|    \--- org.apache.tomcat.embed:tomcat-embed-core:7.0.55


provided - Dependencies needed at development time, but not during deployment (total: 1)
+--- javax.servlet:javax.servlet-api:3.0.1


compile - Dependencies placed on the classpath for compilation (total: 72)
+--- org.codehaus.groovy:groovy-all:2.4.4
+--- org.grails:grails-plugin-rest:2.5.4
|    \--- org.grails:grails-web:2.5.4
|         \--- org.grails:grails-web-mvc:2.5.4
|         \--- org.grails:grails-web-databinding:2.5.4
|              \--- org.grails:grails-databinding:2.5.4
|         \--- org.grails:grails-web-gsp:2.5.4
|         \--- org.grails:grails-web-sitemesh:2.5.4
|              \--- opensymphony:sitemesh:2.4
|         \--- org.grails:grails-web-jsp:2.5.4
|         \--- org.grails:grails-web-common:2.5.4
|              \--- org.springframework:spring-webmvc:4.1.8.RELEASE
|              \--- org.springframework:spring-context-support:4.1.8.RELEASE
|         \--- org.grails:grails-web-url-mappings:2.5.4
|         \--- org.grails:grails-web-fileupload:2.5.4
|              \--- commons-fileupload:commons-fileupload:1.3.1
|                   \--- commons-io:commons-io:2.2
|    \--- org.slf4j:jcl-over-slf4j:1.7.5
|    \--- org.grails:grails-plugin-controllers:2.5.4
|         \--- org.grails:grails-plugin-validation:2.5.4
|    \--- com.google.code.gson:gson:2.2.4
|    \--- org.grails:grails-plugin-datasource:2.5.4
|         \--- org.springframework:spring-jdbc:4.1.8.RELEASE
|         \--- org.apache.tomcat:tomcat-jdbc:7.0.50
|              \--- org.apache.tomcat:tomcat-juli:7.0.50
|         \--- org.springframework:spring-context:4.1.8.RELEASE
|              \--- org.springframework:spring-aop:4.1.8.RELEASE
|              \--- org.springframework:spring-expression:4.1.8.RELEASE
|    \--- org.slf4j:slf4j-api:1.7.5
+--- org.grails:grails-plugin-databinding:2.5.4
|    \--- org.grails:grails-core:2.5.4
|         \--- org.springframework:spring-core:4.1.8.RELEASE
|         \--- org.grails:grails-bootstrap:2.5.4
|         \--- org.hibernate.javax.persistence:hibernate-jpa-2.1-api:1.0.0.Final
|         \--- aopalliance:aopalliance:1.0
|         \--- org.grails:grails-spring:2.5.4
|         \--- org.springframework:spring-beans:4.1.8.RELEASE
+--- org.grails:grails-plugin-i18n:2.5.4
|    \--- commons-lang:commons-lang:2.6
+--- org.grails:grails-plugin-filters:2.5.4
+--- org.grails:grails-plugin-gsp:2.5.4
|    \--- org.grails:grails-plugin-codecs:2.5.4
|         \--- org.grails:grails-encoder:2.5.4
|              \--- org.springframework:spring-web:4.1.8.RELEASE
|         \--- commons-codec:commons-codec:1.6
|    \--- org.grails:grails-logging:2.5.4
|    \--- org.grails:grails-web-gsp-taglib:2.5.4
+--- org.grails:grails-plugin-log4j:2.5.4
|    \--- org.slf4j:jul-to-slf4j:1.7.5
+--- org.grails:grails-plugin-services:2.5.4
|    \--- org.springframework:spring-tx:4.1.8.RELEASE
+--- org.grails:grails-plugin-servlets:2.5.4
+--- org.grails:grails-plugin-url-mappings:2.5.4
|    \--- com.googlecode.concurrentlinkedhashmap:concurrentlinkedhashmap-lru:1.4
|    \--- org.grails:grails-validation:2.5.4
|         \--- commons-validator:commons-validator:1.4.0
+--- org.grails:grails-plugin-async:2.5.4
|    \--- org.grails:grails-async:2.5.4
|         \--- org.codehaus.gpars:gpars:1.2.1
|              \--- org.codehaus.jsr166-mirror:jsr166y:1.7.0
+--- org.grails.plugins:scaffolding:2.1.2
+--- org.grails.plugins:cache:1.1.8
|    \--- org.javassist:javassist:3.17.1-GA
|    \--- org.grails.plugins:webxml:1.4.1
+--- org.grails.plugins:asset-pipeline:2.5.7
|    \--- com.bertramlabs.plugins:asset-pipeline-core:2.5.5


runtime - Dependencies needed at runtime but not for compilation (total: 109)
+--- org.codehaus.groovy:groovy-all:2.4.4
+--- org.grails:grails-plugin-rest:2.5.4
|    \--- org.grails:grails-web:2.5.4
|         \--- org.grails:grails-web-mvc:2.5.4
|         \--- org.grails:grails-web-databinding:2.5.4
|              \--- org.grails:grails-databinding:2.5.4
|         \--- org.grails:grails-web-gsp:2.5.4
|         \--- org.grails:grails-web-sitemesh:2.5.4
|              \--- opensymphony:sitemesh:2.4
|         \--- org.aspectj:aspectjweaver:1.8.7
|         \--- org.grails:grails-web-jsp:2.5.4
|         \--- org.grails:grails-web-common:2.5.4
|              \--- org.springframework:spring-webmvc:4.1.8.RELEASE
|              \--- org.springframework:spring-context-support:4.1.8.RELEASE
|         \--- org.aspectj:aspectjrt:1.8.7
|         \--- org.grails:grails-web-url-mappings:2.5.4
|         \--- org.springframework:spring-aspects:4.1.8.RELEASE
|         \--- org.grails:grails-web-fileupload:2.5.4
|              \--- commons-fileupload:commons-fileupload:1.3.1
|                   \--- commons-io:commons-io:2.2
|    \--- org.slf4j:jcl-over-slf4j:1.7.5
|    \--- org.grails:grails-plugin-controllers:2.5.4
|         \--- org.grails:grails-plugin-validation:2.5.4
|    \--- com.google.code.gson:gson:2.2.4
|    \--- org.grails:grails-plugin-datasource:2.5.4
|         \--- org.springframework:spring-jdbc:4.1.8.RELEASE
|         \--- org.apache.tomcat:tomcat-jdbc:7.0.50
|              \--- org.apache.tomcat:tomcat-juli:7.0.50
|         \--- org.apache.tomcat.embed:tomcat-embed-logging-log4j:7.0.50
|         \--- org.springframework:spring-context:4.1.8.RELEASE
|              \--- org.springframework:spring-aop:4.1.8.RELEASE
|              \--- org.springframework:spring-expression:4.1.8.RELEASE
|    \--- org.slf4j:slf4j-api:1.7.5
+--- org.grails:grails-plugin-databinding:2.5.4
|    \--- org.grails:grails-core:2.5.4
|         \--- org.springframework:spring-core:4.1.8.RELEASE
|         \--- xalan:serializer:2.7.2
|         \--- org.grails:grails-bootstrap:2.5.4
|         \--- org.hibernate.javax.persistence:hibernate-jpa-2.1-api:1.0.0.Final
|         \--- aopalliance:aopalliance:1.0
|         \--- org.grails:grails-spring:2.5.4
|         \--- org.springframework:spring-beans:4.1.8.RELEASE
+--- org.grails:grails-plugin-i18n:2.5.4
|    \--- commons-lang:commons-lang:2.6
+--- org.grails:grails-plugin-filters:2.5.4
+--- org.grails:grails-plugin-gsp:2.5.4
|    \--- org.grails:grails-plugin-codecs:2.5.4
|         \--- org.grails:grails-encoder:2.5.4
|              \--- org.springframework:spring-web:4.1.8.RELEASE
|         \--- commons-codec:commons-codec:1.6
|    \--- org.grails:grails-logging:2.5.4
|    \--- org.grails:grails-web-gsp-taglib:2.5.4
+--- org.grails:grails-plugin-log4j:2.5.4
|    \--- org.slf4j:jul-to-slf4j:1.7.5
+--- org.grails:grails-plugin-services:2.5.4
|    \--- org.springframework:spring-tx:4.1.8.RELEASE
+--- org.grails:grails-plugin-servlets:2.5.4
+--- org.grails:grails-plugin-url-mappings:2.5.4
|    \--- com.googlecode.concurrentlinkedhashmap:concurrentlinkedhashmap-lru:1.4
|    \--- org.grails:grails-validation:2.5.4
|         \--- commons-validator:commons-validator:1.4.0
+--- org.grails:grails-plugin-async:2.5.4
|    \--- org.grails:grails-async:2.5.4
|         \--- org.codehaus.gpars:gpars:1.2.1
|              \--- org.codehaus.jsr166-mirror:jsr166y:1.7.0
+--- com.h2database:h2:1.3.176
+--- log4j:log4j:1.2.17
+--- org.grails:grails-resources:2.5.4
+--- org.grails.plugins:scaffolding:2.1.2
+--- org.grails.plugins:cache:1.1.8
|    \--- org.javassist:javassist:3.17.1-GA
|    \--- org.grails.plugins:webxml:1.4.1
+--- org.grails.plugins:asset-pipeline:2.5.7
|    \--- org.mozilla:rhino:1.7R4
|    \--- com.bertramlabs.plugins:asset-pipeline-core:2.5.5
|         \--- com.google.javascript:closure-compiler:v20141023
|              \--- com.google.javascript:closure-compiler-externs:v20141023
|              \--- args4j:args4j:2.0.26
|              \--- com.google.guava:guava:18.0
|              \--- com.google.protobuf:protobuf-java:2.5.0
|              \--- com.google.code.findbugs:jsr305:1.3.9
|         \--- commons-logging:commons-logging:1.1.1
+--- org.grails.plugins:hibernate4:4.3.10
|    \--- org.hibernate:hibernate-validator:5.1.3.Final
|         \--- javax.validation:validation-api:1.1.0.Final
|         \--- com.fasterxml:classmate:1.0.0
|    \--- org.hibernate:hibernate-ehcache:4.3.10.Final
|         \--- org.hibernate:hibernate-core:4.3.10.Final
|              \--- org.jboss.spec.javax.transaction:jboss-transaction-api_1.2_spec:1.0.0.Final
|              \--- antlr:antlr:2.7.7
|              \--- org.jboss:jandex:1.1.0.Final
|    \--- net.sf.ehcache:ehcache:2.9.0
|    \--- org.jboss.logging:jboss-logging:3.1.0.GA
|    \--- org.grails:grails-datastore-core:3.1.5.RELEASE
|    \--- org.grails:grails-datastore-gorm:3.1.5.RELEASE
|    \--- org.grails:grails-datastore-gorm-hibernate4:3.1.5.RELEASE
|         \--- org.grails:grails-datastore-gorm-hibernate-core:3.1.5.RELEASE
|              \--- org.grails:grails-datastore-gorm-plugin-support:3.1.5.RELEASE
|              \--- org.springframework:spring-orm:4.1.8.RELEASE
|         \--- org.hibernate.common:hibernate-commons-annotations:4.0.4.Final
|              \--- org.jboss.logging:jboss-logging-annotations:1.2.0.Beta1
|         \--- dom4j:dom4j:1.6.1
|    \--- org.grails:grails-datastore-simple:3.1.5.RELEASE
+--- org.grails.plugins:database-migration:1.4.0
|    \--- org.liquibase:liquibase-core:2.0.5
+--- org.grails.plugins:jquery:1.11.1


test - Dependencies needed for test compilation and execution but not at runtime (total: 127)
+--- javax.servlet:javax.servlet-api:3.0.1
+--- org.codehaus.groovy:groovy-all:2.4.4
+--- org.grails:grails-plugin-rest:2.5.4
|    \--- org.grails:grails-web:2.5.4
|         \--- org.grails:grails-web-mvc:2.5.4
|         \--- org.grails:grails-web-databinding:2.5.4
|              \--- org.grails:grails-databinding:2.5.4
|         \--- org.grails:grails-web-gsp:2.5.4
|         \--- org.grails:grails-web-sitemesh:2.5.4
|              \--- opensymphony:sitemesh:2.4
|         \--- org.aspectj:aspectjweaver:1.8.7
|         \--- org.grails:grails-web-jsp:2.5.4
|         \--- org.grails:grails-web-common:2.5.4
|              \--- org.springframework:spring-webmvc:4.1.8.RELEASE
|              \--- org.springframework:spring-context-support:4.1.8.RELEASE
|         \--- org.aspectj:aspectjrt:1.8.7
|         \--- org.grails:grails-web-url-mappings:2.5.4
|         \--- org.springframework:spring-aspects:4.1.8.RELEASE
|         \--- org.grails:grails-web-fileupload:2.5.4
|              \--- commons-fileupload:commons-fileupload:1.3.1
|                   \--- commons-io:commons-io:2.2
|    \--- org.slf4j:jcl-over-slf4j:1.7.5
|    \--- org.grails:grails-plugin-controllers:2.5.4
|         \--- org.grails:grails-plugin-validation:2.5.4
|    \--- com.google.code.gson:gson:2.2.4
|    \--- org.grails:grails-plugin-datasource:2.5.4
|         \--- org.springframework:spring-jdbc:4.1.8.RELEASE
|         \--- org.apache.tomcat:tomcat-jdbc:7.0.50
|              \--- org.apache.tomcat:tomcat-juli:7.0.50
|         \--- org.apache.tomcat.embed:tomcat-embed-logging-log4j:7.0.50
|         \--- org.springframework:spring-context:4.1.8.RELEASE
|              \--- org.springframework:spring-aop:4.1.8.RELEASE
|              \--- org.springframework:spring-expression:4.1.8.RELEASE
|    \--- org.slf4j:slf4j-api:1.7.5
+--- org.grails:grails-plugin-databinding:2.5.4
|    \--- org.grails:grails-core:2.5.4
|         \--- org.springframework:spring-core:4.1.8.RELEASE
|         \--- xalan:serializer:2.7.2
|         \--- org.grails:grails-bootstrap:2.5.4
|         \--- org.hibernate.javax.persistence:hibernate-jpa-2.1-api:1.0.0.Final
|         \--- aopalliance:aopalliance:1.0
|         \--- org.grails:grails-spring:2.5.4
|         \--- org.springframework:spring-beans:4.1.8.RELEASE
+--- org.grails:grails-plugin-i18n:2.5.4
|    \--- commons-lang:commons-lang:2.6
+--- org.grails:grails-plugin-filters:2.5.4
+--- org.grails:grails-plugin-gsp:2.5.4
|    \--- org.grails:grails-plugin-codecs:2.5.4
|         \--- org.grails:grails-encoder:2.5.4
|              \--- org.springframework:spring-web:4.1.8.RELEASE
|         \--- commons-codec:commons-codec:1.6
|    \--- org.grails:grails-logging:2.5.4
|    \--- org.grails:grails-web-gsp-taglib:2.5.4
+--- org.grails:grails-plugin-log4j:2.5.4
|    \--- org.slf4j:jul-to-slf4j:1.7.5
+--- org.grails:grails-plugin-services:2.5.4
|    \--- org.springframework:spring-tx:4.1.8.RELEASE
+--- org.grails:grails-plugin-servlets:2.5.4
+--- org.grails:grails-plugin-url-mappings:2.5.4
|    \--- com.googlecode.concurrentlinkedhashmap:concurrentlinkedhashmap-lru:1.4
|    \--- org.grails:grails-validation:2.5.4
|         \--- commons-validator:commons-validator:1.4.0
+--- org.grails:grails-plugin-async:2.5.4
|    \--- org.grails:grails-async:2.5.4
|         \--- org.codehaus.gpars:gpars:1.2.1
|              \--- org.codehaus.jsr166-mirror:jsr166y:1.7.0
+--- org.grails:grails-plugin-testing:2.5.4
|    \--- org.grails:grails-plugin-converters:2.5.4
|    \--- cglib:cglib:2.2.2
|         \--- asm:asm:3.3.1
|    \--- org.grails:grails-plugin-mimetypes:2.5.4
|    \--- org.grails:grails-plugin-domain-class:2.5.4
|    \--- org.grails:grails-test:2.5.4
|         \--- org.grails:grails-project-api:2.5.4
|              \--- jline:jline:2.12
|              \--- org.fusesource.jansi:jansi:1.11
|              \--- org.codehaus.gant:gant_groovy1.8:1.9.6
|              \--- org.apache.ant:ant:1.9.4
|                   \--- org.apache.ant:ant-launcher:1.9.4
|         \--- org.objenesis:objenesis:1.4
|    \--- org.springframework:spring-test:4.1.8.RELEASE
+--- org.spockframework:spock-core:1.0-groovy-2.4
+--- cglib:cglib-nodep:2.2.2
+--- junit:junit:4.12
|    \--- org.hamcrest:hamcrest-core:1.3
+--- com.h2database:h2:1.3.176
+--- log4j:log4j:1.2.17
+--- org.grails:grails-resources:2.5.4
+--- org.grails:grails-datastore-test-support:1.0.2-grails-2.4
+--- org.grails.plugins:scaffolding:2.1.2
+--- org.grails.plugins:cache:1.1.8
|    \--- org.javassist:javassist:3.17.1-GA
|    \--- org.grails.plugins:webxml:1.4.1
+--- org.grails.plugins:asset-pipeline:2.5.7
|    \--- org.mozilla:rhino:1.7R4
|    \--- com.bertramlabs.plugins:asset-pipeline-core:2.5.5
|         \--- com.google.javascript:closure-compiler:v20141023
|              \--- com.google.javascript:closure-compiler-externs:v20141023
|              \--- args4j:args4j:2.0.26
|              \--- com.google.guava:guava:18.0
|              \--- com.google.protobuf:protobuf-java:2.5.0
|              \--- com.google.code.findbugs:jsr305:1.3.9
|         \--- commons-logging:commons-logging:1.1.1
+--- org.grails.plugins:hibernate4:4.3.10
|    \--- org.hibernate:hibernate-validator:5.1.3.Final
|         \--- javax.validation:validation-api:1.1.0.Final
|         \--- com.fasterxml:classmate:1.0.0
|    \--- org.hibernate:hibernate-ehcache:4.3.10.Final
|         \--- org.hibernate:hibernate-core:4.3.10.Final
|              \--- org.jboss.spec.javax.transaction:jboss-transaction-api_1.2_spec:1.0.0.Final
|              \--- antlr:antlr:2.7.7
|              \--- org.jboss:jandex:1.1.0.Final
|    \--- net.sf.ehcache:ehcache:2.9.0
|    \--- org.jboss.logging:jboss-logging:3.1.0.GA
|    \--- org.grails:grails-datastore-core:3.1.5.RELEASE
|    \--- org.grails:grails-datastore-gorm:3.1.5.RELEASE
|    \--- org.grails:grails-datastore-gorm-hibernate4:3.1.5.RELEASE
|         \--- org.grails:grails-datastore-gorm-hibernate-core:3.1.5.RELEASE
|              \--- org.grails:grails-datastore-gorm-plugin-support:3.1.5.RELEASE
|              \--- org.springframework:spring-orm:4.1.8.RELEASE
|         \--- org.hibernate.common:hibernate-commons-annotations:4.0.4.Final
|              \--- org.jboss.logging:jboss-logging-annotations:1.2.0.Beta1
|         \--- dom4j:dom4j:1.6.1
|    \--- org.grails:grails-datastore-simple:3.1.5.RELEASE
+--- org.grails.plugins:database-migration:1.4.0
|    \--- org.liquibase:liquibase-core:2.0.5
+--- org.grails.plugins:jquery:1.11.1

ashburndave@dphnuc4:~/g2projects/g254app$ 
```

```
ashburndave@dphnuc4:~/g2projects/g254app$ 
ashburndave@dphnuc4:~/g2projects/g254app$ date
Sat Aug 18 09:57:22 EDT 2018
ashburndave@dphnuc4:~/g2projects/g254app$ pwd
/home/ashburndave/g2projects/g254app
ashburndave@dphnuc4:~/g2projects/g254app$ ls -latr
total 104
drwxr-xr-x  4 ashburndave ashburndave  4096 Aug 18 08:06 src
drwxr-xr-x  4 ashburndave ashburndave  4096 Aug 18 08:06 test
drwxr-xr-x  2 ashburndave ashburndave  4096 Aug 18 08:06 scripts
drwxr-xr-x  2 ashburndave ashburndave  4096 Aug 18 08:06 lib
drwxr-xr-x  7 ashburndave ashburndave  4096 Aug 18 08:06 web-app
drwxr-xr-x 11 ashburndave ashburndave  4096 Aug 18 08:06 grails-app
-rw-r--r--  1 ashburndave ashburndave  1003 Aug 18 08:06 .classpath
-rw-r--r--  1 ashburndave ashburndave   480 Aug 18 08:06 .project
-rw-r--r--  1 ashburndave ashburndave   110 Aug 18 08:06 application.properties
drwxr-xr-x  2 ashburndave ashburndave  4096 Aug 18 08:06 wrapper
-rwxr--r--  1 ashburndave ashburndave  9604 Aug 18 08:06 grailsw
-rw-r--r--  1 ashburndave ashburndave  5972 Aug 18 08:06 grailsw.bat
drwxr-xr-x  9 ashburndave ashburndave  4096 Aug 18 08:06 ..
drwxr-xr-x  3 ashburndave ashburndave  4096 Aug 18 08:08 target
-rw-r--r--  1 ashburndave ashburndave   215 Aug 18 08:10 .gitignore
-rw-r--r--  1 ashburndave ashburndave 22594 Aug 18 09:49 README.md
drwxr-xr-x 11 ashburndave ashburndave  4096 Aug 18 09:49 .
drwxr-xr-x  8 ashburndave ashburndave  4096 Aug 18 09:50 .git
ashburndave@dphnuc4:~/g2projects/g254app$ 
ashburndave@dphnuc4:~/g2projects/g254app$ cat application.properties 
#Grails Metadata file
#Sat Aug 18 08:06:07 EDT 2018
app.grails.version=2.5.4
app.name=g254app
app.version=0.1
ashburndave@dphnuc4:~/g2projects/g254app$ 
```

