---
title:  "Icons"
summary: "Embed icons into your text/elements"
---

Icons can very easily be used with the `icon` shortcode:

```markdown
{{</* icon <NAME> (<SIZE> <COLOR>) */>}}
```

The icons that are used are [the {{< icon bootstrap-fill >}}ootstrap icons
{{< icon box-arrow-up-right >}}](https://icons.getbootstrap.com/#icons).

The `<NAME>` in the icon tag is mandatory and resembles the name of the icon,
as found on the bootstrap website.

The `size` and `color` arguments are optional, and space separated. If you want
to change the color, but not the size, set the size to `default`, as the argument
for the color is required at position 3.\
The size can be any css size value: e.g. `4rem`, `5px`, `1vh`, etc.

The third and optional argument is the color of the icon. It defaults to
its surrounding color, for example in alerts.\
The value can be any CSS color.

## Examples
{{< icon clipboard-check >}}
```markdown
{{</* icon clipboard-check */>}}
```

{{< icon code-slash 4rem >}}
```markdown
{{</* icon code-slash 4rem */>}}
```

{{< icon earbuds default cornflowerblue >}}
```markdown
{{</* icon earbuds default cornflowerblue */>}}
```

{{< icon file-earmark-pdf 4rem red >}}
```markdown
{{</* icon file-earmark-pdf 4rem red */>}}
```

{{< alert info escape >}}
# Icons in alerts
Icons inherit their color from their parent: {{< icon newspaper >}}
{{</ alert >}}
```markdown
{{</* alert info escape*/>}}
# Icons in alerts
Icons inherit their color from their parent: {{</* icon newspaper */>}}
{{</*/ alert */>}}
```

{{< alert success escape >}}
# Icons in alerts
Icons inherit their color from their parent: {{< icon newspaper >}}
{{< /alert >}}
```markdown
{{</* alert success escape */>}}
# Icons in alerts
Icons inherit their color from their parent: {{</* icon newspaper */>}}
{{</*/ alert */>}}
```

Icons also work in tables:

{{< table warning striped hover escape >}}
| Name | Icon |
| --- | --- |
| `person-circle` | {{< icon person-circle >}} |
| `pen-fill` | {{< icon pen-fill >}} |
| `qr-code` | {{< icon qr-code >}} |
{{</ table >}}

```markdown
{{</* table warning striped hover escape*/>}}
| Name | Icon |
| --- | --- |
| `person-circle` | {{</* icon person-circle */>}} |
| `pen-fill` | {{</* icon pen-fill */>}} |
| `qr-code` | {{</* icon qr-code */>}} |
{{</*/ table */>}}
```
