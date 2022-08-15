---
title:  "Tables"
summary: "Beautify markdown tables"
---

Normal markdown tables look a bit boring:

```markdown
| Id  | Name    | Age |
| --- | ---     | --- |
| 1   | Alice   | 42  |
| 2   | Bob     | 69  |
| 3   | Charlie | 1   |
```

Resulting in:

| Id | Name | Age |
| --- | --- | --- |
| 1 | Alice | 42 |
| 2 | Bob | 69 |
| 3 | Charlie | 1 |

---

## Bootstrap tables
Bootstrap tables are embedded inside a shortcode: `{{</* table */>}}` and `{{</*/ table */>}}`.

Here is an example with the corresponding output:

```markdown
{{</* table striped hover */>}}
| Id  | Name    | Age |
| --- | ---     | --- |
| 1   | Alice   | 42  |
| 2   | Bob     | 69  |
| 3   | Charlie | 1   |
{{</*/ table */>}}
```

{{< table primary striped hover >}}
| Id | Name | Age |
| --- | --- | --- |
| 1 | Alice | 42 |
| 2 | Bob | 69 |
| 3 | Charlie | 1 |
{{</ table >}}

As you can see, the table block can take additional arguments.
The following optional arguments are supported:

- colorscheme:
  - `primary`
  - `secondary`
  - `success`
  - `danger`
  - `warning`
  - `info`
  - `light`
  - `dark`
- `hover`: highlights the rows when hovering over them
- stripes:
  - `striped`: horizontal stripes (rows)
  - `striped_columns` vertical stripes (columns)
- `small`: Make the table smaller
- `divider`: the divider between the title bar and the body
- `responsive`: If the table should be scrollable vertically
- borders
  - `bordered`: Adds outline borders to the table
  - `borderless`: Removes all cell borders

For more information about bootstrap tables,
please visit [their documentation](https://getbootstrap.com/docs/5.2/content/tables/)
