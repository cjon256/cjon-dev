+++
date = '2024-12-06T11:26:44-05:00'
title = 'Proof of Concept'
expriryDate = '2024-12-11T10:03:19-05:00'
+++

Quote of the day: "In this day and age, the most significant competitive threats (if competitors pursue them) and opportunities (if your company goes after them first) come from new capabilities provided or enabled by information technology innovations."

source: https://www.cio.com/article/191822/the-hard-truth-about-business-it-alignment.html

```go
package reverse_test

import (
  "fmt"
  "golang.org/x/example/hello/reverse"
)

func ExampleString() {
  fmt.Println(reverse.String("hello"))
  // Output: olleh
}
```

javascript

```js
// Zero Dependencies Node.js HTTP Server for running static on localhost
var http = require("http");
var fs = require("fs");
var path = require("path");
console.log("cwd", __dirname);
var index = fs.readFileSync(path.resolve(__dirname + "/../index.html"), "utf8");
var favicon = fs.readFileSync(__dirname + "/favicon.ico");
var app = fs.readFileSync(__dirname + "/todo-app.js");
var elmish = fs.readFileSync(__dirname + "/elmish.js");
var appcss = fs.readFileSync(__dirname + "/todomvc-app.css");
var basecss = fs.readFileSync(__dirname + "/todomvc-common-base.css");

http
  .createServer(function (req, res) {
    console.log("URL:", req.url);
    if (req.url.indexOf("favicon") > -1) {
      res.writeHead(200, { "Content-Type": "image/x-icon" });
      res.end(favicon);
    }
    if (req.url.indexOf(".js") > -1) {
      res.writeHead(200, { "Content-Type": "application/javascript" });
      if (req.url.indexOf("elmish") > -1) {
        res.end(elmish);
      } else {
        res.end(app);
      }
    }
    if (req.url.indexOf(".css") > -1) {
      res.writeHead(200, { "Content-Type": "text/css" });
      if (req.url.indexOf("base") > -1) {
        res.end(basecss);
      } else {
        res.end(appcss);
      }
    } else {
      res.writeHead(200, { "Content-Type": "text/html" });
      res.end(index);
    }
  })
  .listen(process.env.PORT || 8000);
```

```elixir
// ...

let channel = socket.channel("lobby", {});
let list    = $('#message-list');
let message = $('#message');
let name    = $('#name');

message.on('keypress', event => {
  if (event.keyCode == 13) {
    channel.push('new_message', { name: name.val(), message: message.val() });
    message.val('');
  }
});

channel.on('new_message', payload => {
  list.append(`<b>${payload.name || 'Anonymous'}:</b> ${payload.message}<br>`);
  list.prop({scrollTop: list.prop("scrollHeight")});
});

channel.join()
  .receive("ok", resp => { console.log("Joined successfully", resp) })
  .receive("error", resp => { console.log("Unable to join", resp) })

// ...
```
