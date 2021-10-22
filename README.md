# go-services-kodo

[qiniu kodo](https://www.qiniu.com/products/kodo) service support for [go-storage](https://github.com/beyondstorage/go-storage).

## Notes

**This package has been moved to [go-storage](https://github.com/beyondstorage/go-storage/tree/master/services/kodo).**

```shell
go get go.beyondstorage.io/services/kodo/v3
```

## Install

```go
go get github.com/beyondstorage/go-service-kodo/v2
```

## Usage

```go
import (
	"log"

	_ "github.com/beyondstorage/go-service-kodo/v2"
	"github.com/beyondstorage/go-storage/v4/services"
)

func main() {
	store, err := services.NewStoragerFromString("kodo://bucket_name/path/to/workdir?credential=hmac:<access_key>:<secret_key>&endpoint=http:<domain>")
	if err != nil {
		log.Fatal(err)
	}
	
	// Write data from io.Reader into hello.txt
	n, err := store.Write("hello.txt", r, length)
}
```

- See more examples in [go-storage-example](https://github.com/beyondstorage/go-storage-example).
- Read [more docs](https://beyondstorage.io/docs/go-storage/services/kodo) about go-service-kodo.
