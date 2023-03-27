To begin with, you'll need to make a new `Bitmap` in the `class Main extends hxd.App` between the brackets, I won't help you out in this one, but I'm assuming you know how to do it.

Next, just like the previous chapter, we'll need to make a `tile` variable. And then reference our image like so:

```haxe
var tile = hxd.Res.imageHere.toTile();
```

now after, it's just simple as rendering the `tile` to the `s2d`

```haxe
bmp = new Bitmap(tile, s2d);
```