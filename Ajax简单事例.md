```javascript
$.ajax({
    async : false,    //表示请求是否异步处理
    type : "post",    //请求类型
    url : url,//请求的 URL地址
    dataType : "json",//返回的数据类型
    success: function (data) {
        console.log(data);  //在控制台打印服务器端返回的数据
        alert(data)
    },
    error:function (data) {
        alert(data.result);
    }
});
```

