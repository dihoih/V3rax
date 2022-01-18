[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/dihoih/herokaka.git)部署按钮，
下面是反代代码
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
