# Typo, a Hugo theme. (modified)

This is a customized version of typo to add support for features that I need or to tweak the css for my own use-cases

## Modifications

### Lightbox support

I needed support for thumbnails in a blogpost with a click on a thumbnail giving the full resolution picture. Since I'm oldskool, I used lightbox for this.

In your markdown file, use:

```
{{< gallery title="some title" subtitle="some subtitle" folder="gallery1" >}}
```

This will add a lightbox with all images in the `gallery1/` folder as thumbnails. The `title` and `subtitle` are optional and allow for adding some text above or below the lightbox.

### Clickable site title

The site title can be clicked and refers to the `/` page. I needed this because I have a tendency to click on titles and expect them to lead me to the homepage of a website.

### Subtitles for images

I made a special shortcode, so I can add a visible subtitle to each image:

```
{{< subtitle text="Your subtitle..." >}}
```

### Syntax highlighting

I added the lovelace theme for syntax highlighting. I still don't quite understand why it doesn't work out of the box, if i use the Hugo command to generate a `syntax.css` file with chroma, it generates all CSS selectors with `.chroma` but the entire website builds and expects `.highlight`. There's probably something trivial that I don't get...

```
hugo gen chromastyles --style=lovelace | perl -ne 's/\.chroma/\.highlight/g;print' > assets/css/syntax.css
```

And in my `hugo.toml` I added:

```
pygmentsCodefences = true
pygmentsStyle = "pygments"
```

And that improved things :)
