# ✂️ Snippets

Save these snippets for quick and easy model creation.

### Start of each document

```yaml
name: $name$
description: $description$
locations:
- $location$
  fields:
  $END$
```

### Each field

```yaml
$name$:
  type: $type$
  required: $required$
  description: $description$
  example: $examples$
  ref: $nameDTO$$DTO$
$END$
```
