# Python + Apache Docker Image

Run python [CGI](https://docs.python.org/3.8/library/cgi.html) scripts in [apache](https://httpd.apache.org/docs/2.4/) HTTP server.

## Tags

- `3.8.2`

## Usage

```bash
docker run -d -p 80:80 helphi/python-apache:3.8.2
curl http://localhost/cgi-bin/hello.py
```
