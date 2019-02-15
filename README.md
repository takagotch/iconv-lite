### iconv-lite
---
https://github.com/ashtuchkin/iconv-lite

```js
var iconv = require('iconv-lite');

str = iconv.decode(Buffer.from([0x68, 0x65, 0x6c, 0x6c, 0x6f]), 'win1251');

buf = iconv.encode("Sample input string", 'win1251');

iconv.encodingExists("us-ascii")


http.createServer(function(req, res) {
  var converterStream = iconv.decodeStream('win1251');
  req.pipe(converterStream);
  
  converterStream.on('data', function(str) {
    console.log(str);
  });
});

fs.createReadStream('file-in-win1251.txt')
  .pipe(iconv.decodeStream('win1251'))
  .pipe(iconv.encodeStream('ucs2'))
  .pipe(fs.createWriteStream('file-in-ucs2.txt'));
  
http.createServer(funciton(req, res){
  req.pipe(iconv.decodeStream).collect(function(err, body) {
    assert(typeof body == 'string');
    console.log(body);
  });
});

iconv.extendNodeEncodings();

buf = new Buffer(str, 'win1251');
buf.write(str, 'gbk');
str = buf.toString('latin1');
assert(Buffer.isEncoding('iso-8859-15'));
Buffer.byteLength(str, 'us-ascii');

http.createServer(function(req, res) {
  req.setEncoding('big5');
  req.collect(function(err, body) {
    console.log(body);
  });
});

fs.createReadStream("file.txt", "shift_jis");

request = require('request');
request({
  url: "http://github.com/",
  encoding: "cp932"
});

iconv.undoExtendNodeEncodings();
```

```
npm install
npm test

node tst/performance.js
npm run coverage
open coverage/lcov-report/index.html
```

```
```


