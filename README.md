run java -jar java-cup-11b.jar -dump_tables <filename>.cup to create parser.java, sym.java and dump LALR tables

how to:
1) create grammar1.cup
2) run `java -jar java-cup-11b.jar -interface -parser Parser grammar1.cup`. It will generate sym.java and parser.java
3) edit your scanner.java based on your grammar.java. scanner.java taken from http://www2.cs.tum.edu/projects/cup/examples.php 
4) compile all .java. `javac -cp java-cup-11b-runtime.jar:. *.java`. validate your scanner.java with your grammar.cup if encountered some errors.
5) run. `java -cp java-cup-11b-runtime.jar:. Main`