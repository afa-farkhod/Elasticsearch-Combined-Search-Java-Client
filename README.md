# Elasticsearch-Combined-Search-Java-Client
Elasticsearch Combined Search (Vector + Text) Java Client

## [Implementation](https://github.com/af4092/Elasticsearch-Combined-Search-Java-Client/tree/main/src/ElasticHighLevelVectorTextCombinedSearchAPI/src/main/java/org/example)

- Java client `ElasticsearchConnectionCheckHTTP` that establishes a connection to an Elasticsearch cluster and checks if the connection is successful using HTTP.
- Variables:
  - The code declares and initializes several variables:
  - host: Represents the IP address or hostname of the Elasticsearch cluster.
  - port: Represents the port number on which the Elasticsearch cluster is running.
  - username: Represents the username for authentication with the Elasticsearch cluster.
  - password: Represents the password for authentication with the Elasticsearch cluster.
- Building the Elasticsearch Client:
  - The code creates a RestClientBuilder object to configure the Elasticsearch client.
  - It uses the RestClient.builder() method and specifies the host, port, and "http" scheme to build an HTTP host.
  - The setHttpClientConfigCallback method is used to configure the HTTP client with authentication credentials.
  - It creates a CredentialsProvider object, sets the AuthScope to ANY, and provides the UsernamePasswordCredentials.
  - The httpClientBuilder is then configured with the setDefaultCredentialsProvider method.
  - Finally, the RestHighLevelClient is created using the configured RestClientBuilder.
- Checking the Connection:
  - The code attempts to ping the Elasticsearch cluster using the client.ping method and passing RequestOptions.DEFAULT.
  - If the ping is successful, it prints "Connection is SUCCESSFUL."
  - If an IOException occurs during the ping, it prints "Connection is FAILED" along with the exception message.
- Closing the Client:
  - The client.close() method is called in a finally block to ensure the client resources are released.
