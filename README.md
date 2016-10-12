# statistics

[使用示例](http://orionwei.github.io/homework/statistics/docs/demo.html)

1. 获取 statistics

  下载statistics文件

2. 引入 statistics 插件（`dist` 目录下的 JS）：

  ```html
  <script src="statistics.js"></script>
  ```

3. 初始化 autocomplete:

  ```js
  var a = statistics({
        obj:document.getElementById("a"), //must
        filterType:"length",
        length:20,
        callback:function(){   //超出长度后的回调函数
            this.value = this.value.slice(0,20);
        }
    });
    var b = statistics({
        obj:document.getElementById("b"), //must
        filterType:"RegExp",  //正则
        reg:"a",
        callback:function(){  //匹配成功后的回调函数
            console.log(1);
        }
    })
  ```
