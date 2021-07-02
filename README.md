# gqlgen-mongo

go generate based graphql server library with mongo plugin

## What is gqlgen-mongo?

**gqlgen-mongo** is a [gqlgen](https://github.com/99designs/gqlgen) generator adding a simple plugin that append bson tags for every property in a graphql struct.

## Getting Started

Setup your project as described on [gqlgen](https://gqlgen.com/getting-started/) and then run the following command to generate the graphql server schema

```
go run github.com/timokoenig/gqlgen-mongo
```

## Example

```go
type User struct {
	ID          string        `json:"id" bson:"_id,omitempty"`
	CreatedAt   time.Time     `json:"createdAt" bson:"createdAt,omitempty"`
	Email       string        `json:"email" bson:"email,omitempty"`
}
```
