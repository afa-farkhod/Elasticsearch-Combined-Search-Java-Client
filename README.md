# Elasticsearch-Combined-Search-Java-Client
Elasticsearch Combined Search (Vector + Text) Java Client

## [Implementation](https://github.com/af4092/Elasticsearch-Combined-Search-Java-Client/tree/main/src/ElasticHighLevelVectorTextCombinedSearchAPI/src/main/java/org/example)

1. `ElasticHighLevelVectorTextCombinedSearchApiHTTP` Java client that demonstrates how to use the Elasticsearch Java High-Level REST Client to perform various search operations on an Elasticsearch index. Here's a general explanation of the code:
- Import Statements:
  - The code imports various classes from the org.apache.http and org.elasticsearch packages for making HTTP requests and interacting with Elasticsearch.
- Main Method:
  - The code contains a main method that serves as the entry point of the program.
  - It prompts the user to input the index name, vector field name, vector value, text field name, and text value.
- Creating the Elasticsearch Client:
  - The code calls the `createClient()` method to create an instance of the `RestHighLevelClient` using the provided Elasticsearch IP address, port, username, and password.
  - The IP address, port, username, and password are specified as constants or placeholders (ELASTIC-IP-ADDRESS, ELASTIC-PORT, USERNAME, PASSWORD) and should be replaced with actual values.
- Vector Search:
  - The code calls the `performVectorSearch()` method to perform a vector search.
  - It constructs a `SearchRequest and `SearchSourceBuilder` to define the search request and query.
  - The `MoreLikeThisQueryBuilder` is used to create a vector query based on the vector field and value provided.
  - The search request is executed using the `client.search()` method.
- Text Search:
  - The code calls the `performTextSearch()` method to perform a text search.
  - It constructs a `SearchRequest` and `SearchSourceBuilder` to define the search request and query.
  - The `MatchQueryBuilder` is used to create a text query based on the text field and value provided.
  - The search request is executed using the `client.search()` method.
- Combined Search:
  - The code calls the `performCombinedSearch()` method to perform a combined search.
  - It constructs a `SearchRequest` and `SearchSourceBuilder` to define the search request and query.
  - The `BoolQueryBuilder` is used to create a boolean query that combines the vector query and text query.
  - The search request is executed using the `client.search()` method.
- Printing Search Results:
  - The code calls the `printSearchResults()` method to print the search results for each type of search (vector, text, combined).
  - The method prints the total hits, as well as the ID, score, and source of each search hit.
