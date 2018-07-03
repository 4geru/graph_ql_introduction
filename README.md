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