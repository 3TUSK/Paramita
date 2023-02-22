# Pāramitā

> When you still can't decide which loader and which version to develop with... why not choose *ALL OF THEM*?

This is a multi-project template for those who wish to develop a single Minecraft mod on multiple Minecraft versions and 
multiple loaders, altogether in a single place. 

As you can see, this template is definitely NOT for newcomers. 
Users of this template are expected to have experiences on modding two or more Minecraft versions, as well as 
experiences with different modding frameworks (Fabric, Forge, Quilt, ...)

If you want something much simpler, [jaredlll08/MultiLoader-Template][ref-jared-template] is also a good start. 
That template focuses on one specific Minecraft version, which is much more conventional.

[ref-jared-template]: https://github.com/jaredlll08/MultiLoader-Template

The name of this template `Pāramitā` is [IAST][ref-IAST] of Sanskrit पारमिता, usually translated as "perfection", or 
less commonly interpreted as "that which goes beyond". 

[ref-IAST]: https://en.wikipedia.org/wiki/International_Alphabet_of_Sanskrit_Transliteration

## Usage

Simply clone the repository and start adding/removing subprojects based on your need. After that, you can start coding. 
Remember, 

  - Change the mod name from `ExampleMod` to something else.
  - All shared code goes to `-base` projects.
  - Loader-specific code goes to loader-specific projects. 
  - Access Wideners used in `-base` projects must be duplicated in all loader-specific projects, unless some APIs you 
    depend on have done so already. This will get more significant when you encounter a method/field that Forge's AT 
    has exposed for you.
  - Purge the entire `.git` directory and then `git init` if you need a fresh start of your `git` history.

All `build.gradle` files should give you enough hint about what do they do.

*More coming soon*

### How to know which projects do I need?

Depends on your actual need. You probably want the latest version (as of today, it is 1.19.3) first. 
Nevertheless, here are a few things to consider: 

  - Maintaining too many loader+version combinations can make you burn out *very fast*. You have been warned.
  - If you are on/want 1.19.*, you will need both `1.19.2` and `1.19.3` subprojects if:
    - You have new items
    - You have anything to do with `BakedModel`
  - If you are on/want 1.18.*, you will need both `1.18.1` and `1.18.2` subprojects if:
    - You have anything to do with world generation
  - *To be continued*

## How to contribute

*Coming soon*

## Credits

Special thanks to williewillus, Hurby, Alwinfy, et al. for their multi-loader project architecture used in Botania;
without their pioneering work, this gigantic project layout will not be possible. 

Special thanks to Architectury team for their work on Architectury Loom, which enables the usage of full 
Official Mapping on Forge with Minecraft 1.14 - 1.16.5. 

Special thanks to all developers behind these projects:

  - Architectury Loom
  - Fabric Loom
  - ForgeGradle
  - Librarian (by ParchmentMC)
  - MixinGradle
  - Quilt Loom
  - VanillaGradle

## Further Reading

- [Williewillus, Hubry, Alwinfy. "Maintaining Botania for Forge and Fabric — Multiloader Experience Report", BlanketCon 22.][ref-1]
- [Darkhax, Jared. "MultiLoader Madness", BlanketCon 22.][ref-2]

[ref-1]: https://www.youtube.com/watch?v=EZ-Lvtx6Wyk&list=PLC1qq1Hb0u1GI8919iCClzb_Bku-DrL4L&index=11
[ref-2]: https://www.youtube.com/watch?v=Ec8AoD29lrw&list=PLC1qq1Hb0u1GI8919iCClzb_Bku-DrL4L&index=17
