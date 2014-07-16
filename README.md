A Knockout.js binding for keeping an element bound to an observable array scrolled to the bottom.

[Click here to see an example](http://one-com.github.io/knockout-bottomsup/examples/)

Usage:

```html
<ul style="overflow: auto; height: 100px;"
    data-bind="foreach: myObservableArray, bottomsUp: true">
  <li>...</li>
</ul>
```

Whenever `myObservableArray` changes, the `<ul>` will be scrolled to the bottom if it was at the bottom before the change. Thus the user can turn off the behavior by scrolling the element up.

If you want to prune the array while the element is scrolled to the bottom, use the `trim` option to specify the maximum number of items to retain:

```html
<ul style="overflow: auto; height: 100px;"
    data-bind="foreach: myObservableArray, bottomsUp: {trim: 25}">
  <li>...</li>
</ul>
```

This is useful for logs that you don't want to grow infinitely.

## License

Knockout.dragdrop is licensed under a standard 3-clause BSD license -- see the `LICENSE` file for details.
