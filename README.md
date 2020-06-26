# thingproxy-docker
Docker Container for [thingproxy](https://github.com/zinthose/thingproxy)

## Why?
Because Deno's fetch is broken *(as of 2020-06-25)* and can't reliably establish SSL sessions to some remote REST servers.

## About
Uses the latest `node:lts-alpine` container and git clones from [https://github.com/zinthose/thingproxy](https://github.com/zinthose/thingproxy) 

Port 3000 is exposed by default.

## Example
URL = `http://localhost:3000/fetch/https://postman-echo.com/get?foo1=bar1&foo2=bar2`

Result:
```json
{"args":{"foo1":"bar1","foo2":"bar2"},"headers":{"x-forwarded-proto":"https","x-forwarded-port":"443","host":"postman-echo.com","upgrade-insecure-requests":"1","user-agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.116 Safari/537.36","accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","sec-fetch-site":"none","sec-fetch-mode":"navigate","sec-fetch-user":"?1","sec-fetch-dest":"document","accept-encoding":"gzip, deflate, br","accept-language":"en-US,en;q=0.9","url":"https://postman-echo.com/get?foo1=bar1&foo2=bar2"}
