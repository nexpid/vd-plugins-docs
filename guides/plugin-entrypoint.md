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

# 👂 Plugin entrypoint

{% embed url="https://cdn.discordapp.com/attachments/919655852724604978/1187893096810303590/gnarpycake.mp4?ex=65988aa8&hm=6ed671a6bb371cf9f89412317dc38e1b60a33a9294422d884eba32c207eff126&is=658615a8" fullWidth="false" %}
gnarpy from regretevator cutting a xan cake
{% endembed %}

{% code title="src/index.ts" overflow="wrap" lineNumbers="true" %}
```tsx
import { General } from "@vendetta/ui/components";

const { Text } = General;

export const onLoad = () => console.log("Plugin loaded!");
export const onUnload = () => console.log("Plugin loaded!");
export const Settings = () => <Text style={{ color: "#000" }}>Hello!</Text>;
```
{% endcode %}

* **onLoad** — A function that gets called when the plugin gets enabled
* **onUnload** — A function that gets called when the plugin gets disabled
* **Settings** — A React JSX component, serves as the settings for the plugin

A plugin only gets ran when the user enables it. So this piece of code:

{% code title="src/index.ts" overflow="wrap" lineNumbers="true" fullWidth="false" %}
```typescript
console.log("Plugin loaded!");
export const onUnload = () => console.log("Plugin loaded!");
```
{% endcode %}

does the same thing as this piece of code:

{% code title="src/index.ts" overflow="wrap" lineNumbers="true" %}
```typescript
export const onLoad = () => console.log("Plugin loaded!");
export const onUnload = () => console.log("Plugin loaded!");
```
{% endcode %}

However it's recommended to keep your initial code in **onLoad**, incase this changes in the future
