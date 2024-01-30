# Resourcepack

Ad Astra has a simple data-driven system for rendering dimensions. This allows you to create custom skyboxes with
custom stars, planets, and other celestial bodies. Ad Astra uses this system for rendering its own planets and orbits.
To add custom rendering to your planet, you'll need to create a file in your resource pack:

```
pack_name
└── assets
    └── pack_id
        └── planet_renderers
            └── planet_id.json
```

Here's an example of a planet renderer file:

```json
{
  "custom_clouds": true,
  "custom_sky": true,
  "custom_weather": false,
  "dimension": "pack_id:planet_id",
  "has_fog": true,
  "has_thick_fog": false,
  "render_in_rain": true,
  "sky_renderables": [
    {
      "back_light_color": -39,
      "back_light_scale": 27.0,
      "blend": false,
      "global_rotation": [
        0.0,
        0.0,
        0.0
      ],
      "local_rotation": [
        0.0,
        0.0,
        0.0
      ],
      "movement_type": "TIME_OF_DAY",
      "scale": 9.0,
      "texture": "ad_astra:textures/environment/sun.png"
    },
    {
      "back_light_color": -12813094,
      "back_light_scale": 42.0,
      "blend": false,
      "global_rotation": [
        80.0,
        0.0,
        30.0
      ],
      "local_rotation": [
        0.0,
        -5.0,
        0.0
      ],
      "movement_type": "STATIC",
      "scale": 14.0,
      "texture": "ad_astra:textures/environment/earth.png"
    }
  ],
  "star_brightness": 0.6,
  "star_colors": [
    {
      "data": -1447239681,
      "weight": 3
    },
    {
      "data": -1143472129,
      "weight": 5
    },
    {
      "data": -726785,
      "weight": 100
    },
    {
      "data": -3038977,
      "weight": 80
    },
    {
      "data": -7697665,
      "weight": 150
    },
    {
      "data": -12254977,
      "weight": 10
    },
    {
      "data": -2817,
      "weight": 60
    },
    {
      "data": -464897,
      "weight": 40
    },
    {
      "data": -256,
      "weight": 20
    },
    {
      "data": -65536,
      "weight": 1
    }
  ],
  "stars": 13000,
  "sunrise_angle": 0,
  "sunrise_color": 14180147
}
```

<note>
    All colors are in decimal format. You can convert hexadecimal colors to decimal colors using a converter like <a href="https://www.mathsisfun.com/hexadecimal-decimal-colors.html">this one</a>.
</note>

- `custom_clouds`: If true, removes the vanilla clouds. If you don't want clouds in your planet, set this to true.
- `custom_sky`: If true, removes the vanilla skybox. This is needed if you want a custom skybox.
- `custom_weather`: If true, removes the vanilla weather rendering. If you want rain and snow to render differently in your planet, set this to true.
- `dimension`: The dimension ID of the planet. Make sure the ID is the same as the ID of the dimension you created.
- `has_fog`: If true, renders fog in the planet.
- `has_thick_fog`: If true, renders thick fog, like the fog in the Nether and Venus.
- `render_in_rain`: If true, renders the skybox even when it's raining.
- `sky_renderables`: A list of sky renderables. These are the objects that will be rendered in the sky. Each object has the following fields:
  - `back_light_color`: The color of the light behind the object.
  - `back_light_scale`: The scale of the light behind the object.
  - `blend`: If true, blends the object with the skybox.
  - `global_rotation`: The global rotation of the object. Global rotation is the location of the object in the sky.
  - `local_rotation`: The local rotation of the object. Local rotation is the rotation of the object itself.
  - `movement_type`: The movement type of the object. This can be:
    - `TIME_OF_DAY`: The object will move with the time of day, like the sun and the moon.
    - `STATIC`: The object will never move.
  - `scale`: The scale of the object.
  - `texture`: The texture of the object.
- `star_brightness`: The brightness of the stars.
- `star_colors`: A weighted list of star colors. Each object has the following fields:
  - `data`: The color of the star.
  - `weight`: The weight of the star. The higher the weight, the more likely the star will be rendered.
- `stars`: The amount of stars in the sky.
- `sunrise_angle`: The angle of the sunrise.
- `sunrise_color`: The color of the sunrise.

Once set up, the dimension will render with the custom skybox.

### Lang
You should also add a lang file to your resource pack so that your planet has a name.
  
```json
{
  "solar_system.pack_id.solar_system_id": "Solar System Name",
  "planet.pack_id.planet_id": "Planet Name",
  "planet.pack_id.planet_orbit_id": "Orbit Name"
}
```

### Examples

### Ad Astra's built-in planet resourcepack
- [Ad Astra's built-in planet renderers](https://github.com/terrarium-earth/Ad-Astra/tree/1.20.1/common/src/main/generated/resources/assets/ad_astra/planet_renderers)

### Example planet resourcepack
A resource pack that contains a custom sky renderer for the cheese dimension.
[Cheese Dimension Resource Pack](https://github.com/terrarium-earth/Ad-Astra-Docs/blob/main/Writerside/examples/cheese-resourcepack.zip)