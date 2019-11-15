## Modelling the Word Ladder Game in a Neo4j Graph Database

#### The Game
Word ladder (also known as Doublets, word-links, change-the-word puzzles, paragrams, laddergrams, or Word golf) is a word game invented by Lewis Carroll. A word ladder puzzle begins with two words, and to solve the puzzle one must find a chain of other words to link the two, in which two adjacent words (that is, words in successive steps) differ by one letter.

#### Credit Sources
Words text file: https://github.com/dwyl/english-words <br>
Logic: https://supercompiler.wordpress.com/2014/05/28/implementing-word-ladder-game-using-neo4j/

#### NOTE: At the moment, this code only works for 3-letter words


#### Steps
1) Start a local Neo4j database.
2) Run the Python file to create all the nodes and relationships.
2) To find and visualise the shortest chain, run the below query in the Neo4j browser using the below Cypher query - replace start_word and end_word with your words of choice.
```cypher
MATCH (a:Word3 {word:'start_word'}),(b:Word3 {word:'end_word'}), path = shortestPath((a)-[*..50]-(b)) RETURN path
```



