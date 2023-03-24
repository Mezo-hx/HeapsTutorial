# Project Structure

# As a Web Game
Your project structure should look similar to this if you managed to set it up by following the [Heaps Documentation](https://heaps.io/documentation/hello-world.html)

![ProjectStructure](../Images/ProjectStructure.png)

```json
{
	"version": "0.2.0",
	"configurations": [
		{
			"name": "HashLink (launch)",
			"request": "launch",
			"type": "hl",
			"cwd": "${workspaceFolder}",
			"preLaunchTask": {
			  "type": "haxe",
			  "args": "active configuration"
			}
		  },
		  {
			"name": "HashLink (attach)",
			"request": "attach",
			"port": 6112,
			"type": "hl",
			"cwd": "${workspaceFolder}",
			"preLaunchTask": {
			  "type": "haxe",
			  "args": "active configuration"
			}
		  }
	]
}
```

Now, There's two ways of doing this, One is by using SDL through *HLSDL*:

- `haxelib install hlsdl 1.13.0`

And the other way is by using DirectX through *HLDX*:

- `haxelib install hldx 1.13.0`

You may be wondering, "What's the difference between the two?" Well;

*HLSDL* is more focused on Cross-Platform development

While *HLDX* is more focused on Windows-specific development, or in other words, *HLDX* is limited to only the Windows Operating System.

I am using *HLSDL* for this tutorial, but feel free to use *HLDX* instead.

once you have either one installed, we can move on. The only thing you'll need to do is edit your `.hxml` file, and add 4 new lines:

![Exe](../Images/CodeGraphic.png)

For information about `-D dce=full`, check out [Docs For It](https://haxe.org/manual/cr-dce.html)

`client.hl` can be renamed to whatever you want, but it must have the `.hl` extension (this goes for HLDX also)

If you're using *HLDX*, just replace `-lib hlsdl` with `-lib hldx`

Upon running (by pressing F5), a window should show up, but some may encounter an error like:

`src\module.c(506) : FATAL ERROR : Failed to load function sdl@get_window_grab`

this can be fixed by running the following commands one by one in Visual Studio Code's terminal:

`haxelib git heaps https://github.com/HeapsIO/heaps`

`haxelib set heaps git`

`haxelib git hlsdl https://github.com/HaxeFoundation/hashlink master libs/sdl`

`haxelib git hldx` (for HLDX users)

If the issue still persists, you can also try installing the [nightly build](https://github.com/HaxeFoundation/hashlink/releases) for Hashlink, once you have installed it, you can follow these steps:

Locate and Open the ZIP file you downloaded and open the Folder that is inside of it

![Step1](../Images/Screenshot_3.png)

Once the folder is open, copy all the contents by CTRL + A and CTRL + B

![Step2](../Images/Screenshot_4.png)

Next, find a folder called **HaxeToolkit**, for me, it's in my *C:* drive. And then open another folder called *hl*

![Step3](../Images/Screenshot_5.png)

Once your inside that folder, press *CTRL + A* and then *CTRL + V*, and replace all files.

#### ~Don't forget to add the HL folder to your PATH~

And now simply Re-open visual studio code and run it again.

If you're on a Linux Distribution, you'll need to download one of the assets of the Nightly Build (for hashlink) based on your system

there's two versions

the AMD64 version and the i386 version

AMD64 is for x64 bit computers, while i386 are for x86 or x36 bit computers