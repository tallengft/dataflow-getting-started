# Dataflow Getting Started

* Created using the following command from this [guide](https://beam.apache.org/get-started/quickstart-java/)
* sample.txt created from [https://www.lipsum.com/](https://www.lipsum.com/)

```bash
mvn archetype:generate \
      -DarchetypeGroupId=org.apache.beam \
      -DarchetypeArtifactId=beam-sdks-java-maven-archetypes-examples \
      -DarchetypeVersion=2.30.0 \
      -DgroupId=org.example \
      -DartifactId=word-count-beam \
      -Dversion="0.1" \
      -Dpackage=org.apache.beam.examples \
      -DinteractiveMode=false
```

# Run Word Count With
Word count is directly from the example found [here](https://beam.apache.org/get-started/quickstart-java/)

```bash
mvn compile exec:java -Dexec.mainClass=org.apache.beam.examples.WordCount \
     -Dexec.args="--inputFile=sample.txt --output=counts" -Pdirect-runner
```

# Run Hello World With
This is a simple pipeline that prints hello world to a file

```bash
mvn compile exec:java -Dexec.mainClass=org.apache.beam.examples.HelloWorld \
     -Dexec.args="" -Pdirect-runner
```