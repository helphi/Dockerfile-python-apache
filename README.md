# Python + Apache Docker Image

Run python [CGI](https://docs.python.org/3.10/library/cgi.html) scripts in [apache](https://httpd.apache.org/docs/2.4/) HTTP server.

## Tags

- [3.8.2](https://gitee.com/docker8/python-apache/tree/master/3.8.2)
- [3.10.0](https://gitee.com/docker8/python-apache/tree/master/3.10.0)

## Usage

```bash
docker run -d -p 80:80 helphi/python-apache:3.10.0
curl http://localhost/cgi-bin/hello.py
```
