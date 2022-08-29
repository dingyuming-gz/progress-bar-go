# progress-bar-go
GO写的进度条

## 概述

最终呈现的效果 `[█████████████████████████]100/100 [eta]16:33:39 [qps]9`

当然，为了更酷炫一点，同时还引入了emoji字符，能够根据字符自适应地调整显示效果。

## 安装

```shell
go get -u github.com/Tinyming-GO/progress-bar-go
```
## 如何使用
```go
package main

import (
	"time"

	progress "github.com/Tinyming-GO/progress-bar-go"
)

func main() {
	bar := progress.New(100)
	for i := 0; i < 100; i++ {
		time.Sleep(time.Second / 10)
		bar.Done(1)
	}
	bar.Finish()
}
```