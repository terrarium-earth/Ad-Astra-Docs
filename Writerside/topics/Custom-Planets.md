# Custom Planets

<note>
    This wiki assumes that you have a basic understanding of how to create data packs 
    and resource packs. If you do not, check out the <a href="https://minecraft.wiki/w/Data_pack">Datapack Guide</a> and
    the <a href="https://minecraft.wiki/w/Tutorials/Creating_a_resource_pack">Resource Pack Guide</a> on the
    <a href="https://minecraft.wiki">Minecraft Wiki</a>.
</note>

Ad Astra allows you to turn any dimension into a planet. A planet is composed of two main parts:

- A data pack that defines the planet's properties. This is required for the planet to be recognized by Ad Astra.
- A resource pack for rendering the dimension. This is only needed if the dimension does not have a custom sky renderer.

Here's a basic overview of how to set these up:
- [Datapack Guide](Datapack.md)
- [Resourcepack Guide](Resourcepack.md)

## Definitions

- `Planet`: an encompassing term for any celestial body in the game, including planets and moons.

## Examples

### Ad Astra's built-in planets
All of Ad Astra's built-in planets are created using a data pack and a resource pack. Feel free to use them as a reference.
- [Ad Astra's built-in planets](https://github.com/terrarium-earth/Ad-Astra/tree/1.20.1/common/src/main/generated/resources/data/ad_astra/planets)
- [Ad Astra's built-in planet renderers](https://github.com/terrarium-earth/Ad-Astra/tree/1.20.1/common/src/main/generated/resources/assets/ad_astra/planet_renderers)

### Example planet datapack
A datapack that contains a custom cheese dimension and is set up as a planet.
[Cheese Dimension Data Pack](https://github.com/terrarium-earth/Ad-Astra-Docs/blob/main/Writerside/examples/cheese-datapack.zip)

### Example planet resourcepack
A resource pack that contains a custom sky renderer for the cheese dimension.
[Cheese Dimension Resource Pack](https://github.com/terrarium-earth/Ad-Astra-Docs/blob/main/Writerside/examples/cheese-resourcepack.zip)