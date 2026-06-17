# MySQL [![GoDoc](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat-square)](https://godoc.org/github.com/conex/mysql)  [![Build Status](https://travis-ci.org/conex/mysql.svg?branch=master)](https://travis-ci.org/conex/mysql) [![Go Report Card](https://goreportcard.com/badge/github.com/conex/mysql)](https://goreportcard.com/report/github.com/conex/mysql)

This package provides a MySQL Box using Conex.

## Usage

```go
package example_test

import (
  "testing"

  "github.com/omeid/conex"
  "github.com/conex/mysql"
  _ "github.com/go-sql-driver/mysql" // Bring your own driver!
)

func TestMain(m *testing.M) {
  conex.Main(m)
}

func TestMySQL(t *testing.T) {
  db, container := mysql.Box(t, nil)
  defer container.Drop()

  // use db to interact with the database
}
```

*Note: You must import your preferred sql driver (e.g., `_ "github.com/go-sql-driver/mysql"`) in your tests, as the plugin does not register one automatically.*
