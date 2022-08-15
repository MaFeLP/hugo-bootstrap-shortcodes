---
title: "Inject the bootstrap styles"
---

## Injection

To import the stylesheets, javascript and fonts (used for the bootstrap icons), just include the partial
`bootstrap.html` into your header:

```html
<head>
...
  {{- partial "bootstrap.html" }}
...
</head>
```

It is important, that the partial `bootstrap.html` is **always** included on all pages that either rely
on bootstrap's CSS, JavaScript or the bootstrap icons.

To minimize bundle size, optional parameters can be passed to the bootstrap partial.\
If only the icons are needed, the JavaScript and CSS can be disabled as follows:

```html
<head>
...
  {{- partial "bootstrap.html" (dict "js" false "css" false)}}
...
</head>
```

If on the other hands the icons are not needed, only they can be disabled as well:

```html
<head>
...
  {{- partial "bootstrap.html" (dict "icons" false)}}
...
</head>
```

---

If not all CSS variables and functions are needed, please look into
[Customization]({{< relref "customize.md" >}}) to reduce the CSS bundle size.

The JavaScript bundle can not be minified further by hugo, as it would require
running another script (e.g. npm) before being able to build the site.\
hugo-bootstrap-shortcodes therefore relies on the prebuilt and minified
JavaScript bundles provided by bootstrap.
