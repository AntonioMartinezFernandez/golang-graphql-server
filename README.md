# golang-graphql-server

This is a simple GraphQL server written in Go.

## Resources

- [GraphQL](https://graphql.org/)
- [gqlgen getting started](https://gqlgen.com/getting-started/)
- [Building a GraphQL Server with Go](https://www.howtographql.com/graphql-go/0-introduction/)

## Getting started

1. Install [Go](https://golang.org/doc/install)
2. Install [gqlgen](https://github.com/99designs/gqlgen)
3. Run `go run cmd/main.go` to start the server
4. Open the GraphQL Playground at `http://localhost:8080/`
5. Create a new Todo with the following query:
   ```graphql
   mutation createTodo {
     createTodo(input: { text: "Buy milk", userId: "1" }) {
       user {
         id
       }
       text
       done
     }
   }
   ```
6. Request todos with the following query:
   ```graphql
   query Todos {
     todos {
       id
       text
       done
       user {
         id
         name
       }
     }
   }
   ```
