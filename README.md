# nextjs-getting-started-2
API Routesから
https://nextjs.org/learn/basics/api-routes/setup

https://nextjs.org/learn/basics/getting-started

https://github.com/zeit/next-learn-demo


## memo

### API Routes
- 同じNext.jsアプリでAPIを作成して使用する方法
- `pages/api` -> API Route
- [swr](https://swr.now.sh/)
    - React Hooks library for remote data fetching

- Middlewares
    - [API Middlewares](https://nextjs.org/docs/api-routes/api-middlewares)


backendとUIを同じappで作れる

### Deploying a Next.js App
`npm run build` -> production build 

PORTを指定して start を実行したいとき

`"start": "next start -p $PORT"`

```sh
PORT=8000 npm start
PORT=9000 npm start
```

buildを一度すれば、複数PORTで立ち上げることができる

[Deployment](https://nextjs.org/docs/deployment)


## Export into a Static HTML App
https://nextjs.org/learn/excel/static-html-export

> If your app needs to generate dynamic pages at the runtime, you can't deploy it as a static app.


`serve`: simple static web server --> generateしたディレクトリに移動して、 `serve -p 8080` とすると確認できる

`next.config.js` の `exportPathMap` を指定するときに、fetch等を行ってpathを追加することができる

`next export` コマンドでは buildしない