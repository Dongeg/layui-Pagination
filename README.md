# layui-Pagination
kayui-分页

```js
    layui.use(['laypage', 'layer'], function () {
        var laypage = layui.laypage
            , layer = layui.layer;
        laypage.render({
            elem: 'pagination ',  //分页标签容器id
            limit: 5,   //每页显示多少条
            count: 100,  //数据总数
            first: '<<',
            last: '>>',
            prev: '<em><</em>',
            next: '<em>></em>',
            theme: '#1E9FFF',
            curr: 1,  //当前active页
            jump: function (obj, first) {//点击页码出发的事件
                if (first != true) {//是否首次进入页面
                    var currentPage = obj.curr;//获取点击的页码
                    window.location.href = "../invest/toLoanBot.htm?page=" + currentPage; //点击跳转链接
                }
            }
        });
    });
```
