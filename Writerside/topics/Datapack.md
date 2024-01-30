# Datapack

<note>
    This wiki assumes that you have a basic understanding of how to create custom dimensions.
    If you do not, check out the <a href="https://minecraft.wiki/w/Custom_dimension">Custom Dimension Guide</a> on the
    <a href="https://minecraft.wiki">Minecraft Wiki</a>.
</note>

To set up a dimension as a planet, the minimum you'll need is a planet file. This file
contains the properties of the planet, such as its dimension, temperature, gravity, and so on.
The file needs to be created at:

```
pack_name
└── data
    └── pack_id
        └── planets
            └── planet_id.json
```

Here's an example of a planet file:

```json
{
  "dimension": "pack_id:planet_id",
  "gravity": 9.807,
  "orbit": "pack_id:orbit_id",
  "oxygen": true,
  "solar_power": 16,
  "solar_system": "ad_astra:solar_system",
  "temperature": 15,
  "tier": 1,
  "additional_launch_dimensions": []
}
```

- `dimension`: The dimension ID of the planet. Make sure the ID is the same as the 
dimension's ID. If you're turning an existing dimension into a planet, 
you can find the dimension ID by typing the `/execute in` command and finding the dimension ID in the list.
If you're creating a new dimension, set this ID to whatever you named the dimension in the `dimension` folder.
- `gravity`: The gravity of the planet. Keep in mind that due to optimizations and floating point precision,
the actual gravity may be slightly different from the value you set here. It's not noticeable, but if you check
the Ti-69 in-game, you'll see that the gravity is slightly off.
- `orbit`: The orbit dimension ID. This dimension must be created in a datapack. See [Orbit](#orbit) for more information.
- `oxygen`: The default oxygen state of the planet.
- `solar_power`: The amount of energy that Ad Astra's solar panels can generate in this planet.
- `solar_system`: The solar system ID of the planet. This is purely cosmetic and just controls where the planet
will be in the planet screen.
- `temperature`: The default temperature of the planet. Setting this to below `-50` will freeze entities and
and blocks while setting it to above `70` will burn entities and blocks.
- `tier`: The minimum rocket tier required to visit this planet.
- `additional_launch_dimensions`: a list of additional dimensions that the player can launch from.

Once this is set up, you'll be able to visit the planet in-game. However, if this is a newly created dimesion,
it wont have a custom sky. See [Resourcepack](Resourcepack.md) for more information on how to set up custom planet rendering.

### Orbit

All planets have a corresponding orbit dimension. An orbit dimension is set up the same way as a planet but with
the `orbit` field absent. Here's an example of an orbit dimension:

```json
{
  "dimension": "pack_id:orbit_id",
  "gravity": 0.0,
  "oxygen": false,
  "solar_power": 32,
  "solar_system": "ad_astra:solar_system",
  "temperature": -270,
  "tier": 1
}
```

You'll need to create the dimension and dimension type files in your datapack as well for your orbit dimension
to work.

### Examples

### Ad Astra's built-in planet datapack
- [Ad Astra's built-in planets](https://github.com/terrarium-earth/Ad-Astra/tree/1.20.1/common/src/main/generated/resources/data/ad_astra/planets)

### Example planet datapack
A datapack that contains a custom cheese dimension and is set up as a planet.
[Cheese Dimension Data Pack](https://github.com/terrarium-earth/Ad-Astra-Docs/blob/main/Writerside/examples/cheese-datapack.zip)