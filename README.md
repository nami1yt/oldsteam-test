# OldSteam-Reborn

This is a receration of the [OldSteam theme](https://github.com/MapleAtMorning/OldSteam-Theme/) made by [MapleAtMorning](https://github.com/MapleAtMorning), which hasn't updated in over half a year.

This theme uses Ricewind012's Advanced [Theme Template](https://github.com/ricewind012/more-advanced-theme-template)

### Known Issues

If you know how to fix. please make a PR.

- Steam Store + Community Pages are not finished, therefore looking weird
- Downloads Page is 50% Complete
- Some Variable Colors don't work

## Examples

This uses **your own** class map - more info on how it works [here][steam-theming-utils].

Let's say you have a file called `src/desktop/titlebarcontrols.css`:

```css
/* Remove useless shit */
#AnnouncementsButton,
#GamepadUIToggle {
  display: none;
}
```

It will be compiled to the following code residing in `dist/desktop/titlebarcontrols.css`:

```css
/* Remove useless shit */
._5wILZhsLODVwGfcJ0hKmJ /* AnnouncementsButton */,
._3LKQ3S_yqrebeNLF6aeiog /* GamepadUIToggle */ {
  display: none;
}
```

This example resides in the `src` directory. The files whose class names will be replaced will reside in the `dist` directory.

## How to Build

```sh
# Install dependencies
$ npm i

# See the readable versions of classes
$ npx steam-theming-utils make_readable_classes

# ...and build!
$ npm run build
```

## Adding Files

If you making a new file for the theme, create the file in `src` as in `.scss` file, then add the file's directory in index.css.

#### Example

```
@import "filename.css";
```

The directory of the file depends on where you place it!

---

[Prettier][prettier], a CSS/JS formatter, is also included as a dependency of [steam-theming-utils][steam-theming-utils].

[prettier]: https://prettier.io
[steam-theming-utils]: https://github.com/ricewind012/steam-theming-utils
