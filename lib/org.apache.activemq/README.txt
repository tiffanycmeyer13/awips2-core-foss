Between versions 5.3 and 5.9, activemq split the core jar into broker, client and openwire-legacy jars. 
These require geronimo for the JMS API and hawtbuf for buffer IO utilities. AlertViz requires stomp at runtime.

Dependency tree from Maven:
org.apache.activemq:activemq-broker:jar:6.1.3
+- org.apache.activemq:activemq-client:jar:6.1.3
|  +- org.slf4j:slf4j-api:jar:2.0.13
|  +- jakarta.jms:jakarta.jms-api:jar:3.1.0
|  \- org.fusesource.hawtbuf:hawtbuf:jar:1.11
+- org.apache.activemq:activemq-openwire-legacy:jar:6.1.3
+- jakarta.annotation:jakarta.annotation-api:jar:2.1.1
\- com.fasterxml.jackson.core:jackson-databind:jar:2.17.2
   +- com.fasterxml.jackson.core:jackson-annotations:jar:2.17.2
   \- com.fasterxml.jackson.core:jackson-core:jar:2.17.2
