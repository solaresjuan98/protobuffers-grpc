# protobuffers-grpc

- [protobuffers-grpc](#protobuffers-grpc)
  - [Protocol buffers (protobuffers)](#protocol-buffers-protobuffers)
  - [What Are Protocol Buffers?](#what-are-protocol-buffers)
  - [Creating and compiling our first proto](#creating-and-compiling-our-first-proto)
  - [Architectonic styles](#architectonic-styles)



## Protocol buffers (protobuffers)

Protocol Buffers (abreviado como Protobuf) es un formato de intercambio de datos. Este formato binario permite a las aplicaciones almacenare intercambiardatos estructurados fácilmente, incluso si los programas están compilados en diferentes lenguajes.

Protobuf se utiliza en combinación con, entre otros, HTTP y RPC (Remote Procedure Call o llamada a procedimiento remoto) para llevar a cabo el proceso de comunicación cliente-servidor local y remota, en particular para describir las interfaces necesarias para ello. La estructura del protocolo también se denomina gRPC.

---

## What Are Protocol Buffers?

Protocol buffers are Google’s language-neutral, platform-neutral, extensible mechanism for serializing structured data – think XML, but smaller, faster, and simpler. You define how you want your data to be structured once, then you can use special generated source code to easily write and read your structured data to and from a variety of data streams and using a variety of languages.


---

## Creating and compiling our first proto


1. Init a go module
```go
go mod init github.com/<username>/<modulename>
```

2. Install the following go packages
```sh

sudo apt install -y protobuf-compiler
# verify 
protoc --version
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest

```

3. Generate profobuffer file
```
protoc --go_out=. --go_opt=paths=source_relative --plugin=<GOPATH>/bin/protoc-gen-go-grpc --go-grpc_out=. --go-grpc_opt=paths=source_relative proto/student.proto
```

---

## Architectonic styles

* Monolitic
* Microservices
* Service oriented architecture (SOA)
* Event driven architecture
* Representational State Transfer Rest