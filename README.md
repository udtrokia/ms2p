# ms2p

Migrate data from sqlite3 to postgreSQL with xorm

### Install

```
go get -u https://github.com/udtrokia/ms2p

```

### Methods



+ Generate -- Generate database structs

```go

type Generate func() 
// output `the.db`

```
  


+ Read -- Read data from sqlite3

```go

type Read func() ([]Block, []Tx)
// import `the.db`

```



+ Write -- Write data into PostgreSQL

```go

type Write func(blocks []Block, txs []Tx) 

```


#### Usage

```Golang
import "ms2p"

func main() {
    Generate();
    Write(Read());
}

```

#### TODO

+ [ ] Struct Separate


#### LICENSE

GPLv3.0
