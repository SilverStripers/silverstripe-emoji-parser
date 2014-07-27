# :star::star::star: Emoji Parser for SilverStripe :star::star::star:

Render Emojis in your template, so that a `:smile:` becomes a real :smile:

# Usage

Copy or clone the project to your SilverStripe instance folder or using composer:

```sh
  composer require pstaender/silverstripe-emoji-parser dev-master
```

Wheny you're done flush SilverStripe cache with `?flush=1`.

In your templates you can now parse Emojis with:

```html
  <h1>$Title</h1>
  $Content.Parse(Emoji)
```

Of course also in combination with other parsers:

```html
  <h1>$Title</h1>
  $Content.Parse(BBCodeParser).Parse(Emoji)
```

All rendered icon-image-tags contain the class `emoji` so that you can easily define a style, for instance:

```css
   img.emoji {
     height: 1em;
     margin: 0 1em 0 1em;
   }
```

# Optional configuration

You can optionally configure these values in your `config.yml`:

```yaml
  Emojis:
    basePath: pathToGraphics
    cssClass: classNameForCSS
```

# Original Project and License

The images are taken from [Emoji-Cheat-Sheet.com](https://github.com/arvida/emoji-cheat-sheet.com) and are under different [Licenses](https://github.com/arvida/emoji-cheat-sheet.com/blob/master/LICENSE).

This module is under **The MIT License (MIT)**.
