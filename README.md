### Reference

[LINK](https://developer.confluent.io/get-started/go)

## config.properties example

```properties
bootstrap.servers=< BOOTSTRAP SERVERS >
security.protocol=SASL_SSL
sasl.mechanisms=PLAIN
sasl.username=< CLUSTER API KEY >
sasl.password=< CLUSTER API SECRET >
```

## Build Producer

```bash
go build -o out/producer util.go producer.go
go build -tags dynamic -o out/producer util.go producer.go  # m1
```

## Build Consumer

```bash
go build -o out/consumer util.go consumer.go
go build -tags dynamic -o out/consumer util.go consumer.go  # m1
```

## M1 Mac Error Solution

```bash
brew install openssl zstd pkg-config
```
