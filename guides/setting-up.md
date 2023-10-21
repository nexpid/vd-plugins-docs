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

# 📃 Setting up

Start off by using a Vendetta plugin template from GitHub:

* If you want all your plugins to be in the same repository (a monorepo), use [**this**](https://github.com/vendetta-mod/plugin-template) template
* If you want a seperate repo for each of your plugins, use [**this**](https://github.com/fierdetta/plugin-template) template

{% hint style="info" %}
If you want to use [vscode.dev](https://vscode.dev/), choose the **Open in a codespace** option when using a template from the list
{% endhint %}

Next, go to your repo's ![](../.gitbook/assets/github-cog.svg) **Settings** ▸ ![](../.gitbook/assets/github-pages.svg) **Pages** and select **gh-pages** as the Branch

Depending on which template you chose, your plugin's URL will appear differently:

* If you chose the monorepo template:
  * `https://GITHUB_USERNAME.github.io/GITHUB_REPO/PLUGIN_NAME`
* If you chose the seperate repo template:
  * `https://GITHUB_USERNAME.github.io/GITHUB_REPO`

:tada: You're done! Try installing the template plugin in Vendetta.
