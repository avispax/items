```go
package main

import "fmt"

type Data struct {
    id    string
    datas []string
}

func findDataById(dataSlice []Data, targetId string) {
    for _, data := range dataSlice {
        if data.id == targetId {
            fmt.Printf("ID: %s, Data: %v\n", data.id, data.datas)
            return
        }
    }
    fmt.Printf("ID %s not found\n", targetId)
}

func main() {
    var aaa []Data = []Data{
        {id: "aaa1", datas: []string{"data1", "data2"}},
        {id: "aaa2", datas: []string{"data3", "data4"}},
    }

    findDataById(aaa, "aaa1")
}
```
