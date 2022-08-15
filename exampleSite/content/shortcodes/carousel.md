---
title: "Carousel"
---

Carousels are `slideshows` which can display multiple images
in a self-looping loop.

Here is an example with the CSS applied from below:

```markdown
{{</* carousel */>}}
- This is the first slide
  With an image: ![Image description](https://cc0.photo/download/5715/)
- And the second slide also has an image: ![Image description](https://cc0.photo/download/5710/)
- Only a description
{{</*/ carousel */>}}
```

{{< carousel >}}
- This is the first slide
  With an image: ![Image description](https://cc0.photo/download/5715/)
- And the second slide also has an image: ![Image description](https://cc0.photo/download/5710/)
- Only a description
{{</ carousel >}}

---

## Options
### `dark`
Uses the dark variant of the carousel.

### `fade`
Uses a fade animation to switch between the different slides instead of swiping.

### `no_indicators`
Disables the 'bars' on the bottom.

### `no_controls`
Disables the arrows on the right and left.

### `escape`
Escapes and unescapes the HTML when converting to markdown.\
Useful when using [icons]({{< relref "icon.md" >}}) in the description.

---

## Styling
You can modify the styles of the classes directly:

```scss
.carousel-placeholder {
    height: 50vh;
}

.carousel-img {
    max-height: 90vh;
}

.carousel-caption-heading {
    color: red;
}

.carousel-caption-description {
    color: greenyellow;
}
```

or you can target the elements of the the carousel independently:

```scss
.carousel-item {
    img {
        max-height: 90vh;
    }

    .placeholder {
        height: 50vh;
    }

    .carousel-caption {
        h5 {
            color: red;
        }

        p {
            color: greenyellow;
        }
    }
}
```

---

More information about carousels can be found at [bootstrap's official
documentation](https://getbootstrap.com/docs/5.2/components/carousel/)
