# Flink Tangle source

*_Note:_* This project is just a proof of concept and necessary for the Flink Tangle streaming examples. 
I do not recommend to use it in production environments. Feel free to contribute to make this production ready.

This library contains some helpful resources to use the tangle streaming data as flink source.

## Usage

### 1. Publish the library to your local repository
Since this library is not available in a maven repository at the moment, you need to publish it locally.

```bash
sbt
sbt:iri-stream-provider> clean
sbt:iri-stream-provider> compile
sbt:iri-stream-provider> publishLocal
```

### 2. Add library as