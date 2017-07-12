Rune
====

Rune is a tool to post-process Haiku raw ARM images for various target devices.

Features
---------

  * Coordinates with a [remote manifest](https://github.com/haiku/firmware/blob/master/manifest.json) at Github of known target boards.
  * Injects any needed vendor specific boot binaries from remote sources.
  * Writes directly to an SD card, or to a new image file.


Why is this needed?
----

The ARM ecosystem contains a wide range of technology and boot processes. While
this variability has been great for innovation, it also means operating systems
need to be custom tailored per device.

Specific boot files on SD cards, secondary loaders at specific offsets,
binary vendor blobs tailored just right per SOC specifications and GPL licensed
u-boot binaries make the ARM ecosystem a tricky beast to conquer.

Why Rust?
---------

  * Low level enough to directly write to files and make modifications without relying on external tools.
  * Cross-platform. Rune is designed to be used by end-users across multiple operating systems.
  * Easy json parsing and HTTP GET's without requiring a large number of libraries.

Credit
------
Thanks to Fedora for creating fedora-arm-installer which was the inspiration for this tool.