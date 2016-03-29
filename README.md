# apostrophe-browser-requirements

Display a polite message telling users with browsers that are too old that they must upgrade or switch browsers to view the site. Use only when necessary.

```
npm install --save apostrophe-browser-requirements
```

In app.js:

```
modules: {
  apostrophe-browser-requirements: {
    minimums: {
      // currently only supports IE detection
      ie: 9
    },
    // optional, should be something simple, not SVG
    logo: '/images/my-custom-logo.png'
  }
}
```

And optionally, in your CSS:

```
#apos-browser-requirements {
  background-color: #somethingthatmatchesyourlogonicely
}
```

If you don't configure a logo, it looks a little "unofficial," so we recommend providing one.

You can override `views/content.html` at project level if you need to change the text or don't want to link to `browsehappy.com`.

## Limitations

This module can't help IE6 and IE7 users because their JavaScript and CSS support is too weak to cope. If you need to display messages to those, use IE conditional comments.