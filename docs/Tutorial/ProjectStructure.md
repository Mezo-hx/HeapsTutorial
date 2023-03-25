# Project Structure

To begin with, you'll need to download my Pre-made [Template](https://github.com/FacilitatedIsTaken/heapsGameTemplate/archive/refs/heads/main.zip)

once downloaded, you can extract the ZIP file and rename it to whatever you want and open it in your preferred IDE/Code Editor (I personally use VSCode)

And now run either one of the commands below

Use *SDL* through *HLSDL*

- `haxelib install hlsdl 1.13.0`

Use DirectX through *HLDX*:

- `haxelib install hldx 1.13.0`

You may be wondering, "What's the difference between the two?" Well;

*HLSDL* is more focused on Cross-Platform development

While *HLDX* is more focused on Windows-specific development, or in other words, *HLDX* is limited to only the Windows Operating System.

I am using *HLSDL* for this tutorial, but feel free to use *HLDX* instead.

once you have either one installed, we can move on.

In the *.hxml* file, `client.hl` can be renamed to whatever you want, but it must have the `.hl` extension (this goes for HLDX also)

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