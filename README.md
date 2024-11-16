<p align="center">
	<img width=256px src="GitHub/logo.png" />
</p>
<p align="center">
	<a href="https://modrinth.com/mod/resolutioncontrol4plus" target="_blank">
		<img alt="Modrinth Version" src="https://img.shields.io/modrinth/v/wHm7Bneo?style=flat&logo=modrinth">
	</a>
</p>

# Resolution Control ++++

Resolution Control ++++ is a fork of [ResolutionControl3](https://github.com/BGP0/ResolutionControl-3?ysclid=m3ipus1vtl365115032) (fork of [ResolutionControl+](https://github.com/UltimateBoomer/Resolution-Control?ysclid=m3ipwlewqb6737760))

This mod is typically used to increase your framerate as much as you want, and is especially useful on high resolution monitors.
For example I have a 4k monitor and used this mod to render in 1080p, quadrupling my framerate. This mod does not affect the HUD/GUI so your inventory and menus will still look just as good!

Join our discord at Coming soon for support.

## Features

### Version Support

This new version of the mod is to support new versions in the form of a port and it will work until Java update (if it affects a code change).
So we need people who know how to port the mod to a new version of the game with support for the new Java!

---

### Resolution Scaling

All versions of Resolution Control allows you to change Minecraft's render resolution separately from the HUD elements.
You can lower the games resolution to improve performance or give Minecraft a retro style. You can also set a custom multiplier value by pressing the `S` button.

Additionally, you can set the upscale/downscale algorithm used to scale the render to the viewport.
Linear is useful as an anti-aliasing filter,
and nearest neighbor generally looks better for lower than native resolutions.
![main](https://i.imgur.com/41EAyJn.png)

---

### Screenshots

All versions of Resolution Control can be used to take larger than native resolution screenshots.
To do this, use the `Screenshot Framebuffer` keybind which is unbound by default.

Compared to *Fabrishot*, this implementation does not lock up the game until the screenshot is saved.
This makes taking large screenshots much faster.
And while a screenshot is being processed, you can take another one without any problems.

Here is the time it takes to take a 16k screenshot, on an i7 4770 and GTX 1060:

```
Fabrishot: 12 seconds (pause)
ResolutionControl3: <1 second (initial pause) + 13 seconds (background processing)
```
[Video](https://www.youtube-nocookie.com/embed/Dghj0Ldeu0Q)

---

## Settings

**Resolution Scaling**

- Render scale
    - 0.0 - 8.0x (can be exceeded by manually setting the value)
    - An estimate VRAM usage is displayed
- Upscale/downscale algorithm  
    - Linear, nearest

**Screenshots**

- Use set size
    - Enabled: render screenshots at the specified resolution

        - Note: can produce artifacts if the screenshot aspect ratio is significantly different 
          from the aspect ratio of the viewport
    - Disabled: render at the scaled render resolution
- Always allocated
    - Enabled: screenshot framebuffer is always allocated in memory
        - May reduce screenshot pause times, at the cost of more VRAM usage during normal gameplay
    - Disabled: screenshot framebuffer is allocated on-demand and freed immediately after
- Screenshot size
    - Screenshot size if `use set size` is enabled
