# README

- get all links

```
{
  allLinks {
    id
    url
    description
  }
}
```


- create mutation

```
mutation{
  createLink(
    url:"http://yahoo.co.jp",
    description:"hoge"
  ) {
    id
    url
    description
  }
}
```

- run test

```
./bin/rspec test test/graphql/resolvers/create_link_test.rb

```

- create_user

```
mutation{
  createUser(
    name: "Test User",
      authProvider: {
        email: {
          email: "hoge@example.com",
          password: "123456"
        }
      }
  ) {
    id
    email
    name
  }
}
```

- sign_in

```
mutation {
  signinUser(email: {email: "hoge@example.com", password: "123456"}) {
    token
    user {
      id
      email
      name
    }
  }
}
```

- allLinks

```
query{
  allLinks {
    id
    url
    description
    postedBy {
      id
      name
      votes {
        link {
          description
        }
      }
    }
  }
}
```