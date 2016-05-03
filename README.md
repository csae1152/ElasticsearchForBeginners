# ElasticsearchForBeginners
This is a tutorial for beginning to have fun with Elasticsearch.

Doing some elasticsearch magic with Java and Spring Boot.
=========================================================

Let's create our first elasticsearch "entity" and start playing around with some annotations.

Elasticsearch and Spring Boot:

1. Create "entitiy" class for our elasticsearch document
2. Implement spring repository
3. Create service
4. Implement serviceImpl


Allowed attributes for type String:

index_name
store
index
doc_values
term_vector
boost - you can modifie this "screw" due to the importance of your docments.
null_value
norms: {enabled: <value>}
norms: {loading: <value>}
index_options
analyzer
index_analyzer
search_analyzer
include_in_all
ignore_above
position_offset_gap

Multiple Query Strings
======================

The simplest multifield query to deal with is the one where we can map search terms to specific fields. If we know that War and Peace is the title, and Leo Tolstoy is the author, it is easy to write each of these conditions as a match clause and to combine them with a bool query:

GET /_search
{
  "query": {
    "bool": {
      "should": [
        { "match": { "title":  "ReleaseIT" }},
        { "match": { "author": "Michael Nygard"   }}
      ]
    }
  }
}






