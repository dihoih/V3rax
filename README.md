###H_eroku部署V_2ray

###提醒：刚申请不要大流量使用，
[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/dihoih/V3rax.git)  部署按钮<p>下面是反代代码:</p>
```js
addEventListener(
    "fetch",event => {
        let url=new URL(event.request.url);
        url.hostname="appname.herokuapp.com";
        let request=new Request(url,event.request);
        event. respondWith(
            fetch(request)
        )
    }
)
```
