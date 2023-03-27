To begin with, you'll need to make a new `Bitmap` in the `class Main extends hxd.App`, between the brackets

```haxe
var bmp = new h2d.Bitmap();
```

Next, just like the previous chapter, we'll need to make a `tile` variablein the `init` function. And then reference our image

```haxe
var tile = hxd.Res.imageHere.toTile();
```

`Res` is assuming that you have a folder in your project called `res` which is your resource/asset folder
`toTile();` is changing the image to a tile.

now after, it's just simple as rendering the `tile` to the `s2d`

```haxe
bmp = new Bitmap(tile, s2d);
```

