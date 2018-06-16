
*reap-cloud-runtime* 是 REAP 平台的共享库（Shared Library）旨在减少 REAP 应用发布包的大小。

## 构建 

执行此命令在工程的 *target/dependency* 包下获取完整依赖的 jar 包。

```bash
mvn dependency:copy-dependencies

```

## 依赖清单

- *org.springframework.cloud/spring-cloud-starter-netflix-eureka-client* 
- *org.springframework.cloud/spring-cloud-starter-config* 
- *org.springframework.cloud/spring-cloud-starter-zipkin*
- *org.springframework.boot/spring-boot-starter-web*
- *org.springframework.boot/spring-boot-starter-data-jpa*
- *org.springframework.boot/spring-boot-starter-actuator*
- *org.springframework.boot/spring-boot-configuration-processor*

完整的依赖树如下：

```bash
[INFO] org.reap:reap-cloud-runtime:pom:0.0.1-SNAPSHOT
[INFO] +- org.springframework.cloud:spring-cloud-starter-netflix-eureka-client:jar:2.0.0.M8:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-starter:jar:2.0.0.M9:compile
[INFO] |  |  +- org.springframework.cloud:spring-cloud-context:jar:2.0.0.M9:compile
[INFO] |  |  |  \- org.springframework.security:spring-security-crypto:jar:5.0.4.RELEASE:compile
[INFO] |  |  +- org.springframework.cloud:spring-cloud-commons:jar:2.0.0.M9:compile
[INFO] |  |  \- org.springframework.security:spring-security-rsa:jar:1.0.5.RELEASE:compile
[INFO] |  |     \- org.bouncycastle:bcpkix-jdk15on:jar:1.56:compile
[INFO] |  |        \- org.bouncycastle:bcprov-jdk15on:jar:1.56:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-netflix-core:jar:2.0.0.M8:compile
[INFO] |  |  \- org.springframework.boot:spring-boot-autoconfigure:jar:2.0.1.RELEASE:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-netflix-eureka-client:jar:2.0.0.M8:compile
[INFO] |  +- com.netflix.eureka:eureka-client:jar:1.8.7:compile
[INFO] |  |  +- org.codehaus.jettison:jettison:jar:1.3.7:runtime
[INFO] |  |  |  \- stax:stax-api:jar:1.0.1:runtime
[INFO] |  |  +- com.netflix.netflix-commons:netflix-eventbus:jar:0.3.0:runtime
[INFO] |  |  |  +- com.netflix.netflix-commons:netflix-infix:jar:0.3.0:runtime
[INFO] |  |  |  |  +- commons-jxpath:commons-jxpath:jar:1.3:runtime
[INFO] |  |  |  |  +- joda-time:joda-time:jar:2.9.9:runtime
[INFO] |  |  |  |  +- org.antlr:antlr-runtime:jar:3.4:runtime
[INFO] |  |  |  |  |  \- org.antlr:stringtemplate:jar:3.2.1:runtime
[INFO] |  |  |  |  \- com.google.code.gson:gson:jar:2.8.2:runtime
[INFO] |  |  |  \- org.apache.commons:commons-math:jar:2.2:runtime
[INFO] |  |  +- com.netflix.archaius:archaius-core:jar:0.7.5:compile
[INFO] |  |  +- javax.ws.rs:jsr311-api:jar:1.1.1:runtime
[INFO] |  |  +- com.netflix.servo:servo-core:jar:0.10.1:runtime
[INFO] |  |  |  \- com.netflix.servo:servo-internal:jar:0.10.1:runtime
[INFO] |  |  +- com.sun.jersey:jersey-core:jar:1.19.1:runtime
[INFO] |  |  +- com.sun.jersey:jersey-client:jar:1.19.1:runtime
[INFO] |  |  +- com.sun.jersey.contribs:jersey-apache-client4:jar:1.19.1:runtime
[INFO] |  |  +- org.apache.httpcomponents:httpclient:jar:4.5.5:compile
[INFO] |  |  |  +- org.apache.httpcomponents:httpcore:jar:4.4.9:compile
[INFO] |  |  |  \- commons-codec:commons-codec:jar:1.11:compile
[INFO] |  |  +- com.google.inject:guice:jar:4.1.0:runtime
[INFO] |  |  |  +- javax.inject:javax.inject:jar:1:runtime
[INFO] |  |  |  \- aopalliance:aopalliance:jar:1.0:runtime
[INFO] |  |  +- com.github.vlsi.compactmap:compactmap:jar:1.2.1:runtime
[INFO] |  |  |  \- com.github.andrewoma.dexx:dexx-collections:jar:0.2:runtime
[INFO] |  |  +- com.fasterxml.jackson.core:jackson-annotations:jar:2.9.0:compile
[INFO] |  |  \- com.fasterxml.jackson.core:jackson-core:jar:2.9.3:compile
[INFO] |  +- com.netflix.eureka:eureka-core:jar:1.8.7:compile
[INFO] |  |  \- org.codehaus.woodstox:woodstox-core-asl:jar:4.4.1:runtime
[INFO] |  |     +- javax.xml.stream:stax-api:jar:1.0-2:runtime
[INFO] |  |     \- org.codehaus.woodstox:stax2-api:jar:3.1.4:runtime
[INFO] |  +- org.springframework.cloud:spring-cloud-starter-netflix-archaius:jar:2.0.0.M8:compile
[INFO] |  |  +- org.springframework.cloud:spring-cloud-netflix-ribbon:jar:2.0.0.M8:compile
[INFO] |  |  +- org.springframework.cloud:spring-cloud-netflix-archaius:jar:2.0.0.M8:compile
[INFO] |  |  +- commons-configuration:commons-configuration:jar:1.8:compile
[INFO] |  |  |  \- commons-lang:commons-lang:jar:2.6:compile
[INFO] |  |  \- com.google.guava:guava:jar:18.0:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-starter-netflix-ribbon:jar:2.0.0.M8:compile
[INFO] |  |  +- com.netflix.ribbon:ribbon:jar:2.2.5:compile
[INFO] |  |  |  +- com.netflix.ribbon:ribbon-transport:jar:2.2.5:runtime
[INFO] |  |  |  |  +- io.reactivex:rxnetty-contexts:jar:0.4.9:runtime
[INFO] |  |  |  |  \- io.reactivex:rxnetty-servo:jar:0.4.9:runtime
[INFO] |  |  |  +- com.netflix.hystrix:hystrix-core:jar:1.5.12:runtime
[INFO] |  |  |  \- io.reactivex:rxnetty:jar:0.4.9:runtime
[INFO] |  |  |     +- io.netty:netty-codec-http:jar:4.1.23.Final:runtime
[INFO] |  |  |     |  \- io.netty:netty-codec:jar:4.1.23.Final:runtime
[INFO] |  |  |     \- io.netty:netty-transport-native-epoll:jar:4.1.23.Final:runtime
[INFO] |  |  |        +- io.netty:netty-common:jar:4.1.23.Final:runtime
[INFO] |  |  |        +- io.netty:netty-buffer:jar:4.1.23.Final:runtime
[INFO] |  |  |        +- io.netty:netty-transport-native-unix-common:jar:4.1.23.Final:runtime
[INFO] |  |  |        \- io.netty:netty-transport:jar:4.1.23.Final:runtime
[INFO] |  |  |           \- io.netty:netty-resolver:jar:4.1.23.Final:runtime
[INFO] |  |  +- com.netflix.ribbon:ribbon-core:jar:2.2.5:compile
[INFO] |  |  +- com.netflix.ribbon:ribbon-httpclient:jar:2.2.5:compile
[INFO] |  |  |  +- commons-collections:commons-collections:jar:3.2.2:runtime
[INFO] |  |  |  \- com.netflix.netflix-commons:netflix-commons-util:jar:0.1.1:runtime
[INFO] |  |  +- com.netflix.ribbon:ribbon-loadbalancer:jar:2.2.5:compile
[INFO] |  |  |  \- com.netflix.netflix-commons:netflix-statistics:jar:0.1.1:runtime
[INFO] |  |  \- io.reactivex:rxjava:jar:1.3.8:compile
[INFO] |  +- com.netflix.ribbon:ribbon-eureka:jar:2.2.5:compile
[INFO] |  |  \- org.slf4j:slf4j-api:jar:1.7.25:compile
[INFO] |  \- com.thoughtworks.xstream:xstream:jar:1.4.10:compile
[INFO] |     +- xmlpull:xmlpull:jar:1.1.3.1:compile
[INFO] |     \- xpp3:xpp3_min:jar:1.1.4c:compile
[INFO] +- org.springframework.boot:spring-boot-starter-actuator:jar:2.0.1.RELEASE:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- org.springframework.boot:spring-boot:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- org.springframework.boot:spring-boot-starter-logging:jar:2.0.1.RELEASE:compile
[INFO] |  |  |  +- ch.qos.logback:logback-classic:jar:1.2.3:compile
[INFO] |  |  |  +- org.apache.logging.log4j:log4j-to-slf4j:jar:2.10.0:compile
[INFO] |  |  |  |  \- org.apache.logging.log4j:log4j-api:jar:2.10.0:compile
[INFO] |  |  |  \- org.slf4j:jul-to-slf4j:jar:1.7.25:compile
[INFO] |  |  +- javax.annotation:javax.annotation-api:jar:1.3.2:compile
[INFO] |  |  +- org.springframework:spring-core:jar:5.0.5.RELEASE:compile
[INFO] |  |  |  \- org.springframework:spring-jcl:jar:5.0.5.RELEASE:compile
[INFO] |  |  \- org.yaml:snakeyaml:jar:1.19:runtime
[INFO] |  +- org.springframework.boot:spring-boot-actuator-autoconfigure:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- org.springframework.boot:spring-boot-actuator:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- org.springframework:spring-context:jar:5.0.5.RELEASE:compile
[INFO] |  |  \- com.fasterxml.jackson.datatype:jackson-datatype-jsr310:jar:2.9.3:compile
[INFO] |  \- io.micrometer:micrometer-core:jar:1.0.3:compile
[INFO] |     +- org.hdrhistogram:HdrHistogram:jar:2.1.10:compile
[INFO] |     \- org.latencyutils:LatencyUtils:jar:2.0.3:compile
[INFO] +- org.springframework.cloud:spring-cloud-starter-config:jar:2.0.0.M9:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-config-client:jar:2.0.0.M9:compile
[INFO] |  \- com.fasterxml.jackson.core:jackson-databind:jar:2.9.3:compile
[INFO] +- org.springframework.boot:spring-boot-starter-web:jar:2.0.1.RELEASE:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter-json:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- com.fasterxml.jackson.datatype:jackson-datatype-jdk8:jar:2.9.3:compile
[INFO] |  |  \- com.fasterxml.jackson.module:jackson-module-parameter-names:jar:2.9.3:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter-tomcat:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- org.apache.tomcat.embed:tomcat-embed-core:jar:8.5.29:compile
[INFO] |  |  +- org.apache.tomcat.embed:tomcat-embed-el:jar:8.5.29:compile
[INFO] |  |  \- org.apache.tomcat.embed:tomcat-embed-websocket:jar:8.5.29:compile
[INFO] |  +- org.hibernate.validator:hibernate-validator:jar:6.0.9.Final:compile
[INFO] |  |  +- javax.validation:validation-api:jar:2.0.1.Final:compile
[INFO] |  |  +- org.jboss.logging:jboss-logging:jar:3.3.2.Final:compile
[INFO] |  |  \- com.fasterxml:classmate:jar:1.3.4:compile
[INFO] |  +- org.springframework:spring-web:jar:5.0.5.RELEASE:compile
[INFO] |  |  \- org.springframework:spring-beans:jar:5.0.5.RELEASE:compile
[INFO] |  \- org.springframework:spring-webmvc:jar:5.0.5.RELEASE:compile
[INFO] |     +- org.springframework:spring-aop:jar:5.0.5.RELEASE:compile
[INFO] |     \- org.springframework:spring-expression:jar:5.0.5.RELEASE:compile
[INFO] +- org.springframework.boot:spring-boot-starter-data-jpa:jar:2.0.1.RELEASE:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter-aop:jar:2.0.1.RELEASE:compile
[INFO] |  |  \- org.aspectj:aspectjweaver:jar:1.8.13:compile
[INFO] |  +- org.springframework.boot:spring-boot-starter-jdbc:jar:2.0.1.RELEASE:compile
[INFO] |  |  +- com.zaxxer:HikariCP:jar:2.7.8:compile
[INFO] |  |  \- org.springframework:spring-jdbc:jar:5.0.5.RELEASE:compile
[INFO] |  +- org.hibernate:hibernate-core:jar:5.2.16.Final:compile
[INFO] |  |  +- org.hibernate.javax.persistence:hibernate-jpa-2.1-api:jar:1.0.0.Final:compile
[INFO] |  |  +- org.javassist:javassist:jar:3.22.0-GA:compile
[INFO] |  |  +- antlr:antlr:jar:2.7.7:compile
[INFO] |  |  +- org.jboss:jandex:jar:2.0.3.Final:compile
[INFO] |  |  +- dom4j:dom4j:jar:1.6.1:compile
[INFO] |  |  \- org.hibernate.common:hibernate-commons-annotations:jar:5.0.1.Final:compile
[INFO] |  +- javax.transaction:javax.transaction-api:jar:1.2:compile
[INFO] |  +- org.springframework.data:spring-data-jpa:jar:2.0.6.RELEASE:compile
[INFO] |  |  +- org.springframework.data:spring-data-commons:jar:2.0.6.RELEASE:compile
[INFO] |  |  +- org.springframework:spring-orm:jar:5.0.5.RELEASE:compile
[INFO] |  |  \- org.springframework:spring-tx:jar:5.0.5.RELEASE:compile
[INFO] |  \- org.springframework:spring-aspects:jar:5.0.5.RELEASE:compile
[INFO] +- org.springframework.cloud:spring-cloud-starter-zipkin:jar:2.0.0.M9:compile
[INFO] |  +- org.springframework.cloud:spring-cloud-starter-sleuth:jar:2.0.0.M9:compile
[INFO] |  |  \- org.springframework.cloud:spring-cloud-sleuth-core:jar:2.0.0.M9:compile
[INFO] |  |     +- org.aspectj:aspectjrt:jar:1.8.13:compile
[INFO] |  |     +- io.zipkin.brave:brave:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-context-log4j2:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-instrumentation-spring-web:jar:4.18.2:compile
[INFO] |  |     |  \- io.zipkin.brave:brave-instrumentation-http:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-instrumentation-spring-rabbit:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-instrumentation-kafka-clients:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-instrumentation-httpclient:jar:4.18.2:compile
[INFO] |  |     +- io.zipkin.brave:brave-instrumentation-httpasyncclient:jar:4.18.2:compile
[INFO] |  |     \- io.zipkin.brave:brave-instrumentation-spring-webmvc:jar:4.18.2:compile
[INFO] |  |        \- io.zipkin.brave:brave-instrumentation-servlet:jar:4.18.2:compile
[INFO] |  \- org.springframework.cloud:spring-cloud-sleuth-zipkin:jar:2.0.0.M9:compile
[INFO] |     +- io.zipkin.reporter2:zipkin-reporter:jar:2.5.0:compile
[INFO] |     +- io.zipkin.reporter2:zipkin-sender-kafka11:jar:2.5.0:compile
[INFO] |     \- io.zipkin.reporter2:zipkin-sender-amqp-client:jar:2.5.0:compile
[INFO] +- io.zipkin.zipkin2:zipkin:jar:2.9.3:compile
[INFO] +- net.logstash.logback:logstash-logback-encoder:jar:4.6:compile
[INFO] |  \- ch.qos.logback:logback-core:jar:1.2.3:compile
[INFO] \- org.springframework.boot:spring-boot-configuration-processor:jar:2.0.1.RELEASE:compile (optional) 
```
