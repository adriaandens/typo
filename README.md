# Typo, a Hugo theme. (modified)

This is a customized version of typo to add support for features that I need or to tweak the css for my own use-cases

## Modifications

### Lightbox support

I needed support for thumbnails in a blogpost with a click on a thumbnail giving the full resolution picture. Since I'm oldskool, I used lightbox for this.

In your markdown file, use:

```
{{ <gallery title="some title" subtitle="some subtitle" folder="gallery1" > }}
```

This will add a lightbox with all images in the `gallery1/` folder as thumbnails. The `title` and `subtitle` are optional and allow for adding some text above or below the lightbox.
