# Flink Tangle source

**_Note:_** This project is just a proof of concept and necessary for the Flink Tangle streaming examples. 
I do not recommend to use it in production environments. Feel free to contribute to make this production ready.

This library contains some helpful resources to use the tangle streaming data as flink source.

## Usage

### 1. Publish the library to your local repository

Since this library is not available in a maven repository at the moment, you need to publish it locally.

```bash
sbt
```

You are now in the sbt repl. You are not able to compile & publish the code to your local maven repository.

```bash
clean
compile
publishLocal
```

### 2. Add library as dependency

Just add the following to your build.sbt

```scala
libraryDependencies += "org.iota" %% "tangle-stream-provider" % "0.0.1"
```

### 3. Use it

**_Note:_** [This repository](https://github.com/Citrullin/flink-tangle-examples) contains a few examples.

You can also filter with the topic parameter, if you are not interested in all ZMQ topics.

```scala
    val env: StreamExecutionEnvironment = StreamExecutionEnvironment.getExecutionEnvironment
    val stream = env.addSource(new TangleSource(zeroMQHost, zeroMQPort, ""))
```