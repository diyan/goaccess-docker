# goaccess-docker
GoAccess in a tiny Docker image powered by Alpine Linux.

GoAccess is an open source real-time web log analyzer and interactive viewer that runs in a terminal in Unix systems. It provides fast and valuable HTTP statistics for system administrators that require a visual server report on the fly. More info at: http://goaccess.io.

# How to use this image

Print help:
```bash
docker run --rm diyan/goaccess --help
```

The most simple usage:
```bash
TODO
```

To generate an HTML report:
```bash
cat access.log | docker run --rm -i diyan/goaccess \
  --time-format='%H:%M:%S' \
  --date-format='%d/%b/%Y' \
  --log-format='%h %^[%d:%t %^] "%r" %s %b "%R" "%u"' > access.html
```
