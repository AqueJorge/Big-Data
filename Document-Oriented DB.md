# Database oriented to documents
A document database is a type of non-relational database that has been designed to store and query data as JSON type documents. Document databases make it easy for developers to store and query data in a database using the same document model format that they use in application code. The flexible, semi-structured and hierarchical nature of documents and document databases allows them to evolve according to the needs of the applications. The document model works well with use cases such as catalogs, user profiles, and content management systems where each document is unique and evolves over time. Document databases allow easy indexing, powerful ad hoc queries, and analysis of document collections. Documentary databases are fundamental allies that we can trust for the handling of voluminous amounts of information.

## Example:
[
    {
        "year" : 2013,
        "title" : "Turn It Down, Or Else!",
        "info" : {
            "directors" : [ "Alice Smith", "Bob Jones"],
            "release_date" : "2013-01-18T00:00:00Z",
            "rating" : 6.2,
            "genres" : ["Comedy", "Drama"],
            "image_url" : "http://ia.media-imdb.com/images/N/O9ERWAU7FS797AJ7LU8HN09AMUP908RLlo5JF90EWR7LJKQ7@@._V1_SX400_.jpg",
            "plot" : "A rock band plays their music at high volumes, annoying the neighbors.",
            "actors" : ["David Matthewman", "Jonathan G. Neff"]
        }
    },
    {
        "year": 2015,
        "title": "The Big New Movie",
        "info": {
            "plot": "Nothing happens at all.",
            "rating": 0
        }
    }
]

Thanks to their flexible schema, they've found regular use in e-commerce, blogging, and analytics platforms, as well as content management systems. Document stores are considered highly scalable, with sharding being a common horizontal scaling strategy. They are also excellent for keeping large amounts of unrelated, complex information that varies in structure.



