## <a name="env_variables"></a> Environment Variables

Alternatively, each variable of the .yml file can be set with an environment variable.
For example, if you want to use an environment variable to set the `name` parameter, you can write it like this: `KAFKA_CLUSTERS_2_NAME`

|Name               	|Description
|-----------------------|-------------------------------
|`SERVER_SERVLET_CONTEXT_PATH` | URI basePath
|`LOGGING_LEVEL_ROOT`        	| Setting log level (trace, debug, info, warn, error). Default: info
|`LOGGING_LEVEL_COM_PROVECTUS` |Setting log level (trace, debug, info, warn, error). Default: debug
|`SERVER_PORT` |Port for the embedded server. Default: `8080`
|`KAFKA_ADMIN-CLIENT-TIMEOUT` | Kafka API timeout in ms. Default: `30000`
|`KAFKA_CLUSTERS_0_NAME` | Cluster name
|`KAFKA_CLUSTERS_0_BOOTSTRAPSERVERS` 	|Address where to connect
|`KAFKA_CLUSTERS_0_KSQLDBSERVER` 	| KSQL DB server address
|`KAFKA_CLUSTERS_0_KSQLDBSERVERAUTH_USERNAME` 	| KSQL DB server's basic authentication username
|`KAFKA_CLUSTERS_0_KSQLDBSERVERAUTH_PASSWORD` 	| KSQL DB server's basic authentication password
|`KAFKA_CLUSTERS_0_PROPERTIES_SECURITY_PROTOCOL` 	|Security protocol to connect to the brokers. For SSL connection use "SSL", for plaintext connection don't set this environment variable
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRY`   	|SchemaRegistry's address
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYAUTH_USERNAME`   	|SchemaRegistry's basic authentication username
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYAUTH_PASSWORD`   	|SchemaRegistry's basic authentication password
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYSSL_KEYSTORELOCATION`   	|Path to the JKS keystore to communicate to SchemaRegistry
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYSSL_KEYSTOREPASSWORD`   	|Password of the JKS keystore for SchemaRegistry
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYSSL_TRUSTSTORELOCATION`   	|Path to the JKS truststore to communicate to SchemaRegistry
|`KAFKA_CLUSTERS_0_SCHEMAREGISTRYSSL_TRUSTSTOREPASSWORD`   	|Password of the JKS truststore for SchemaRegistry
|`KAFKA_CLUSTERS_0_SCHEMANAMETEMPLATE` |How keys are saved to schemaRegistry
|`KAFKA_CLUSTERS_0_METRICS_PORT`        	 |Open metrics port of a broker
|`KAFKA_CLUSTERS_0_METRICS_TYPE`        	 |Type of metrics retriever to use. Valid values are JMX (default) or PROMETHEUS. If Prometheus, then metrics are read from prometheus-jmx-exporter instead of jmx
|`KAFKA_CLUSTERS_0_READONLY`        	|Enable read-only mode. Default: false
|`KAFKA_CLUSTERS_0_DISABLELOGDIRSCOLLECTION`        	|Disable collecting segments information. It should be true for confluent cloud. Default: false
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_NAME` |Given name for the Kafka Connect cluster
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_ADDRESS` |Address of the Kafka Connect service endpoint
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_USERNAME`| Kafka Connect cluster's basic authentication username
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_PASSWORD`| Kafka Connect cluster's basic authentication password
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_KEYSTORELOCATION`| Path to the JKS keystore to communicate to Kafka Connect
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_KEYSTOREPASSWORD`| Password of the JKS keystore for Kafka Connect
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_TRUSTSTORELOCATION`| Path to the JKS truststore to communicate to Kafka Connect
|`KAFKA_CLUSTERS_0_KAFKACONNECT_0_TRUSTSTOREPASSWORD`| Password of the JKS truststore for Kafka Connect
|`KAFKA_CLUSTERS_0_METRICS_SSL`          |Enable SSL for Metrics? `true` or `false`. For advanced setup, see `kafka-ui-jmx-secured.yml`
|`KAFKA_CLUSTERS_0_METRICS_USERNAME` |Username for Metrics authentication
|`KAFKA_CLUSTERS_0_METRICS_PASSWORD` |Password for Metrics authentication
|`TOPIC_RECREATE_DELAY_SECONDS` |Time delay between topic deletion and topic creation attempts for topic recreate functionality. Default: 1
|`TOPIC_RECREATE_MAXRETRIES`  |Number of attempts of topic creation after topic deletion for topic recreate functionality. Default: 15