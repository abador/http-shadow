# http-shadow
Compares HTTP responses from two different backends

### How to run

1. Set up virtualenv
2. Install dependencies by running `python setup.py develop`
3. Run the following (preferrably in `screen`):

```
get_urls | check_urls
```

This will pipe URLs found in Apache access log to the process that will perform two requests: to Apache and to Kubernetes. Response code and headers will be compared and results logged via syslog with `http-shadow` ident. 
