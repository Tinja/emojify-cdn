# emojify-cdn.js

A Javascript module to convert emoji keywords to images via a CDN

The emoji keywords are as described by [emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com).

The majority of this project's code is taken from [emojify.js](http://hassankhan.github.com/emojify.js).

This library has no dependencies to work with whatever javascript framework you use (jquery, prototype, etc).

## Rationale

I wanted [my blog](http://hassankhan.me) to display smileys nicely, decided to use Emojis because they look nice.


## Usage
Add the required lines to the ``<head>`` part of your HTML code:

```
  <script src="emojify-cdn.js"></script>
```

Now type in an emoji keyword in your HTML, for example ``:smile:``
Now run emojify using ``emojify.run()``.
To exclude tags from being emojified, add ``no-emojify`` to their ``class`` attributes.

You can optionally pass an object to ``emojify.run()`` to restrict the **emojification** to that object only: ``emojify.run(document.getElementById('my-element'))``

### Configuration
To set configuration options, use `emojify.setConfig()` and a JSON object as a parameter with the following attributes:
* ``emojify_tag_type``: Set to `<div>` by default. Sets the element the emojify.js uses to replace emoji keywords

### Code Example

    emojify.setConfig({
      emojify_tag_type: 'img'
    });
    emojify.run();

## License

Copyright 2013 Austen Ito

Licensed under the MIT License
