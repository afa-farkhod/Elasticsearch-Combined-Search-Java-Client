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

## [Background](https://www.elastic.co/guide/en/elasticsearch/reference/current/search-your-data.html)

- [k-nearest neighbor (kNN) search](https://www.elastic.co/guide/en/elasticsearch/reference/current/knn-search.html) - A k-nearest neighbor (kNN) search finds the k nearest vectors to a query vector, as measured by a similarity metric. Common use cases for kNN include:
  - Relevance ranking based on natural language processing (NLP) algorithms
  - Product recommendations and recommendation engines
  - Similarity search for images or videos
- [Vector Search](https://www.elastic.co/what-is/vector-search) - Vector search engines — known as vector databases, semantic, or cosine search — find the nearest neighbors to a given (vectorized) query. Where traditional search relies on mentions of keywords, lexical similarity, and the frequency of word occurrences, vector search engines use distances in the embedding space to represent similarity. Finding related data becomes searching for nearest neighbors of your query.

<p align="center">
  <img src="https://github.com/af4092/Elasticsearch-JavaAPI-connection/assets/24220136/5a2b5c51-142c-4a75-a980-ce914dc46325" alt="Image">
</p>

- [Vector Search usage](https://www.datasciencebyexample.com/2023/03/18/elasticsearch-dense-vector-search/) - vector search using Elastic Search, index and search example using python requests library
