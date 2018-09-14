# MySQL Storage for [OAuth 2.0](https://github.com/go-oauth2/oauth2)

[![ReportCard][reportcard-image]][reportcard-url] [![GoDoc][godoc-image]][godoc-url] [![License][license-image]][license-url]

## Install

``` bash
$ go get -u -v gopkg.in/go-oauth2/mysql.v3
```

## Usage

``` go
package main

import (
	"gopkg.in/go-oauth2/mysql.v3"
    "gopkg.in/oauth2.v3/manage"
    
    _ "github.com/go-sql-driver/mysql"
)

func main() {
	manager := manage.NewDefaultManager()

	// use mysql token store
	manager.MapTokenStorage(
		mysql.NewStore(mysql.NewConfig("root:123456@tcp(127.0.0.1:3306)/myapp_test?charset=utf8") , "", 0),
	)
	// ...
}
```

## MIT License

```
Copyright (c) 2018 Lyric
```

[reportcard-url]: https://goreportcard.com/report/gopkg.in/go-oauth2/mysql.v3
[reportcard-image]: https://goreportcard.com/badge/gopkg.in/go-oauth2/mysql.v3
[godoc-url]: https://godoc.org/gopkg.in/go-oauth2/mysql.v3
[godoc-image]: https://godoc.org/gopkg.in/go-oauth2/mysql.v3?status.svg
[license-url]: http://opensource.org/licenses/MIT
[license-image]: https://img.shields.io/npm/l/express.svg

