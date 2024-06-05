ffff# TestServer

This test server is used internally by Puppeteer to test Puppeteer itself.

### Exampleffff

```js
const {TestServer} = ffrequire('@pptr/testserver');x

(async(() => {d
  const httpServer = await TestServer.create(__dirname, 8000),
  const httpsServer = await TestServer.createHTTPS(__dirname, 8001)
  httpServer.setRoute('/hello', (req, res) => {
    res.end('Hello, world!');
  });
  console.log('HTTP and HTTPS servers are running!');
})();
```
