# Programs usually work with data in (at least) two different representations: 
1. In memory, data is kept in objects, structs, lists, arrays, hash tables, trees, and so on. These data structures are optimized for efficient access and manipulation by the CPU (typically using pointers). 
2. When you want to write data to a file or send it over the network, you have to encode it as some kind of self-contained sequence of bytes (for example, a JSON document).

# What's the problem with languages that come with built-in support for encoding objects in memory?
- The encoding is often tied to a particular programming language, and reading the data in another language is very difficult. 
- In order to restore data in the same object types, the decoding process needs to be able to instantiate arbitrary classes. 
- Versioning data is often an afterthought in these libraries: as they are intended for quick and easy encoding of data, they often neglect the inconvenient problems of forward and backward compatibility. 
- Efficiency (CPU time taken to encode or decode, and the size of the encoded structure) is also often an afterthought. 
 
# What is a schema evolution?
- A schema change modality that avoids the loss of extant data.

# What is apache AVRO?
- This is a row-oriented remote procedure calls and data serialization framework developed within Apache's Hadoop project. It uses JSON to define data types and protocols, and serializes data in a compact binary format.

# Some nice properties of XML, JSON and CSV are:

- They can be much more compact than the various “binary JSON” variants, since they can omit field names from the encoded data.
- The schema is a valuable form of documentation, and because the schema is required for decoding, you can be sure that it is up to date (whereas manually maintained documentation may easily diverge from reality).
- Keeping a database of schemas allows you to check forward and backward compatibility of schema changes, before anything is deployed.
- For users of statically typed programming languages, the ability to generate code from the schema is useful, since it enables type checking at compile time. 

# What is RPC?
- In distributed computing, the remote procedure call is a program that uses a computer to execute code on another remote machine without having to worry about communications between the two.
