# Toolkit

## Overview

Download opencars toolkit with following command

```sh
go get -u github.com/opencars/toolkit
```

## Example

Simple example of toolkit usage

```go
package main

import (
  "fmt"
  "log"
  "os"

  "github.com/opencars/toolkit"
)

func main() {
  client := toolkit.New("https://api.opencars.app", os.Getenv("OPENCARS_API_KEY"))
  operation, err := client.Operation().FindByNumber("АА9359РС")
  if err != nil {
    log.Fatal(err)
  }

  fmt.Println(operation)
}
```

## License

Project released under the terms of the MIT [license](./LICENSE).
