# Demo for GraphQL in Go

Deploy with `gcloud app deploy`.

Browse with `gcloud app browse`.

Here are some example queries:

```graphql

query findTodos {
  todos {
    id  
    text
    done
  }
}

query findTodo {
  todo(id: "T5577006791947779410") {
    id
    text
    user {
      id
      name
    }
  }
}

mutation createTodo {
  createTodo(input: { text: "todo2", userId: "2" }) {
    user {
      id
      name
    }
    text
    done
  }
}

```
