---
title:  "Alerts"
---

An alert can be embedded as follows:

```markdown
{{</* alert <NAME> (icon) (dismiss) (escape) */>}}
# Heading
I'm a `primary` **Alert** [with hyperlinks]({{< relref "/" >}}).
{{</*/ alert */>}}
```

`<NAME>` can be exchanged with one of the following values:

- `primary`
- `secondary`
- `success`
- `warning`
- `danger`
- `info`
- `light`
- `dark`

`icon` is an optional argument, a small icon appears on the left side of the alert (see [examples](#examples) below).

If the user should be able to dismiss the alert by clicking on a `X` in the top
right corner, the optional argument `dismiss` needs to be given.

If you use custom HTML inside of the alert, such as other Bootstrap shortcodes (e.g. [icons]({{< relref "icon" >}}),
you need to specify the `escape` parameter so that the HTML will be escaped and unescaped.

### Examples
{{< alert primary icon dismiss >}}
# Primary
I'm a dismissable `primary` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert secondary icon >}}
# Secondary
I'm a `secondary` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert success icon dismiss >}}
# Success
I'm a dismissable `success` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert danger icon >}}
# Danger
I'm a `danger` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert warning icon dismiss >}}
# Warning
I'm a dismissable `warning` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert info icon >}}
# Info
I'm a `info` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert light icon dismiss >}}
# Light
I'm a dismissable `light` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

{{< alert dark icon >}}
# Dark
I'm a dark `light` **Alert** [with hyperlinks]({{< relref "/" >}}) and icon.
{{</ alert >}}

