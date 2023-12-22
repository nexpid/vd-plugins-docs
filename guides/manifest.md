---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📜 Manifest

The `manifest.json` file in your plugin contains information about how your plugin will appear in the Plugins tab, and where the entrypoint for the plugin is. Here's a basic example:

{% code title="manifest.json" overflow="wrap" lineNumbers="true" %}
```json
{
  "name": "Example Plugin"
  "description": "An example plugin for the plugin docs GitBook",
  "authors": [
    {
      "name": "You!",
      "id": "123456789123456789"
    }
  ],
  "main": "src/index.ts",
  "vendetta": {
    "icon": "ic_badge_staff"
  }
}
```
{% endcode %}

* **Name** and **description** are the name and description for the plugin, respectively
* The **authors** field is an array of objects. At least one author is required. The **id** field is a [discord user ID snowflake](https://discord.com/developers/docs/reference#snowflakes) and is currently unused (only used in Plugin Browser)
* The **main** field tells the plugin bundler where the entrypoint for your plugin is.
* The **icon** property in the **vendetta** field refers to an asset in Discord's asset library. Asset strings can be found in the Asset Browser, under Vendetta's developer settings. _(optional)_

