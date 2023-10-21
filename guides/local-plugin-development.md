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

# 〽 Local plugin development

{% hint style="info" %}
This guide is PC only

If you're using [vscode.dev](https://vscode.dev/), you may skip this guide
{% endhint %}

Clone your repo using [**git**](https://github.com/git-guides/install-git)

{% code overflow="wrap" %}
```bash
git clone https://github.com/GITHUB_USERNAME/GITHUB_REPO.git
cd GITHUB_REPO
```
{% endcode %}

Install the `http-server` package:

```bash
npm i http-server -g
```

Then, open two terminal windows and run:

{% tabs %}
{% tab title="Terminal 1" %}
Pick the IP address that starts with `192.168...`

{% code fullWidth="true" %}
```bash
> http-server dist --port XXXX

Starting up http-server, serving dist

...

Available on:
  http://**.**.***.***:XXXX
  http://192.168.**.**:XXXX
  http://***.*.*.*:XXX
```
{% endcode %}
{% endtab %}

{% tab title="Terminal 2" %}
This command should be ran every time you make a change to one of your plugins:

```bash
> pnpm build

Successfully built Template Plugin!
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Make sure your phone is connected to the same network as your PC
{% endhint %}

Depending on which template you chose, the plugin's local IP will be different:

* If you chose the monorepo template:
  * `http://192.168.**.**:XXXX/PLUGIN_NAME`
* If you chose the seperate repo template:
  * `http://192.168.**.**:XXXX`

