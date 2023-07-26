FROM apache/hive:3.1.2

ENV MYSQL_CONNECTOR_VERSION 8.0.26

# Download MySQL JDBC connector
RUN wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}.tar.gz -O /opt/hive/lib/mysql-connector-java.tar.gz

# Unpack MySQL JDBC connector and remove archive file
RUN tar -xzvf /opt/hive/lib/mysql-connector-java.tar.gz -C /opt/hive/lib/ && rm /opt/hive/lib/mysql-connector-java.tar.gz

# Move MySQL JDBC connector to Hive lib directory
RUN mv /opt/hive/lib/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}/mysql-connector-java-${MYSQL_CONNECTOR_VERSION}.jar /opt/hive/lib/
