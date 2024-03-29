# Moved to [https://github.com/goreq/goreq](https://github.com/goreq/goreq)

# GoRe (Go Requester)
Simple HTTP client for Go

# Example

```go
resp, err := gore.Get("https://api.products.com/entities", nil)
if err != nil {
  panic(err)
}

defer resp.Body.Close()

// do anything with the resp object
```

or, using base URL like this

```go
g := gore.New(
  gore.WithBaseURL("https://api.products.com"),
)

resp, err := g.Get("/entities", nil)
if err != nil {
  panic(err)
}

defer resp.Body.Close()

// do anything with the resp object
```

# Features
* Reusable, prevent options rewrite using single object for multiple request
* Flexible, because it use raw response object

# Todos
* [x] Global error handler
* [x] Global request and response hooks
* [x] Use custom request object


## Stargazers over time

[![Stargazers over time](https://starchart.cc/hadihammurabi/gore.svg)](https://starchart.cc/hadihammurabi/gore)

