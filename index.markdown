---
layout: default
title: Home
---

# AppSec Payloads Web

A collection of web application security testing payloads for penetration testing and security research.

## 🎯 Payload Categories

<div class="payload-grid">
  <a href="{{ site.baseurl }}/sqli-payloads" class="payload-card">
    <h3>🗃️ SQL Injection</h3>
    <p>Basic, time-based, error-based, and boolean-based SQLi payloads</p>
  </a>
  
  <a href="{{ site.baseurl }}/xss-payloads" class="payload-card">
    <h3>⚡ Cross-Site Scripting</h3>
    <p>XSS payloads, filter bypasses, and DOM-based attacks</p>
  </a>
  
  <a href="{{ site.baseurl }}/csrf-payloads" class="payload-card">
    <h3>🔄 Cross-Site Request Forgery</h3>
    <p>CSRF forms, auto-submit, and AJAX attack vectors</p>
  </a>
  
  <a href="{{ site.baseurl }}/ssrf-payloads" class="payload-card">
    <h3>🌐 Server-Side Request Forgery</h3>
    <p>SSRF payloads for internal networks and cloud metadata</p>
  </a>
  
  <a href="{{ site.baseurl }}/template-injection-payloads" class="payload-card">
    <h3>📝 Template Injection</h3>
    <p>SSTI payloads for Jinja2, Twig, Smarty, and more</p>
  </a>
</div>

## ⚠️ Usage Warning

**These payloads are for authorized security testing only.** Use responsibly and only on systems you own or have explicit permission to test.

<style>
.payload-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.payload-card {
  background: #0d1117;
  border: 1px solid #30363d;
  border-radius: 8px;
  padding: 20px;
  text-decoration: none;
  color: #c9d1d9;
  transition: all 0.3s ease;
}

.payload-card:hover {
  border-color: #58a6ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(88, 166, 255, 0.15);
}

.payload-card h3 {
  margin: 0 0 10px 0;
  color: #58a6ff;
}

.payload-card p {
  margin: 0;
  font-size: 14px;
  opacity: 0.8;
}
</style>
