---
description: Coded by @nexpid
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Self destruct plugin

{% tabs %}
{% tab title="manifest.json" %}
```json
{
  "name": "Self Destruct",
  "description": "A plugin that deletes itself when installed",
  "authors": [
    {
      "name": "nexpid",
      "id": "853550207039832084"
    }
  ],
  "main": "src/index.ts",
  "vendetta": {
    "icon": "placeholder"
  }
}

```
{% endtab %}

{% tab title="src/index.ts" %}
```typescript
import { id } from "@vendetta/plugin";
import { removePlugin } from "@vendetta/plugins";

export const onUnload = () => removePlugin(id);
```
{% endtab %}
{% endtabs %}
