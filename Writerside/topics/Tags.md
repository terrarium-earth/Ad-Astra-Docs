# Tags

A list of Ad Astra's important tags.

### Items

- `#ad_astra:space_suit_items`: Armor items that will protect the user from cold temperature and oxygen damage.
Note that the space suit chestplate is still required.
- `#ad_astra:nether_space_suit_items`: Armor items that will protect the user from any temperature and oxygen damage.
Note that the netherite space suit chestplate is still required.
- `#ad_astra:jet_suit_items`: Armor items that allow the user to fly. Note that the jet suit chestplate is still required.
- `#ad_astra:freeze_resistant_armor`: Armor items that will protect the user from cold temperature damage.
- `#ad_astra:heat_resistant_armor`: Armor items that will protect the user from hot temperature damage.

### Blocks

- `#ad_astra:passes_flood_fill`: Blocks that allow the flood fill algorithm, which is used for machines like the oxygen distributor, to pass through them.
- `#ad_astra:blocks_flood_fill`: Blocks that the flood fill algorithm, which is used for machines like the oxygen distributor, will not be able to pass through.
- `#ad_astra:destroyed_in_space`: Blocks, such as torches that will randomly break in space.

### Fluids

- `#ad_astra:oxygen`: Fluids that can be used as oxygen.
- `#ad_astra:oil`: Fluids that can be turned into fuel in a fuel refinery.
- `#ad_astra:fuel`: Fluids that can be used as rocket fuel and to power rovers.
- `#ad_astra:efficient_fuel`: Fluids that only require one bucket to launch a rocket.
- `#ad_astra:tier_1_rocket_fuel`: Fuel that can be used to launch a tier 1 rocket.
- `#ad_astra:tier_2_rocket_fuel`: Fuel that can be used to launch a tier 2 rocket.
- `#ad_astra:tier_3_rocket_fuel`: Fuel that can be used to launch a tier 3 rocket.
- `#ad_astra:tier_4_rocket_fuel`: Fuel that can be used to launch a tier 4 rocket.
- `#ad_astra:tier_1_rover_fuel`: Fuel that can be used to power a tier 1 rover.
- `#ad_astra:zip_gun_propellants`: Fluids that can be used as propellants for the zip gun.
- `#ad_astra:freezes_in_space`: Fluids that will turn into ice in freezing temperatures.
- `#ad_astra:"evaporates_in_space"`: Fluids that will evaporate in extremely hot temperatures.

### Entities

- `#ad_astra:lives_without_oxygen`: Entities that can survive without oxygen.
- `#ad_astra:can_survive_extreme_cold`: Entities that can survive in freezing temperatures.
- `#ad_astra:can_survive_extreme_heat`: Entities that can survive in extremely hot temperatures.
- `#ad_astra:can_survive_in_space`: A general tag for entities that can survive any temperature and oxygen state.
- `#ad_astra:can_survive_in_acid_rain`: Entities that can survive in acid rain.
- `#ad_astra:ignores_air_vortex`: Entities that won't be sucked into air vortexes.

### Biomes

- `#ad_astra:has_structure/oil_well`: Biomes that can spawn oil wells. If you want to disable oil wells, create a new tag in a datapack
with the same name and set the `replace` field to `true` and the `values` field to an empty list.