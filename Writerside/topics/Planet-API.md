# Planet API

A planet is an encompassing term for any celestial body in the game, including planets and moons.
Any dimension can be turned into a planet by creating a datapack and giving the dimension the required attributes.
See [Custom Planets](Custom-Planets.md) for more information on how to create a datapack.

The Planet API allows you to safely retrieve the `Planet` object and interact with the planet data for any given dimension.
Planet data is also synced to the client so this API can be used on both the server and the client.

### Planet Structure
- `dimension`: The dimension of the planet.
- `oxygen`: The default oxygen state of the planet.
- `temperature`: The default temperature of the planet.
- `gravity`: The default gravity of the planet.
- `solarPower`: The amount of energy that solar panels can generate on the planet.
- `solarSystem`: The ID of the solar system the planet is in.
- `orbit`: The planet's corresponding orbit dimension.
- `tier`: the required rocket tier to land on the planet.
- `additionalLaunchDimensions`: a list of additional dimensions that the player can launch from.

### Methods

#### `getPlanet(Level level)`

Gets the planet data for the given level, or null if the level is not a planet.

- **Parameters**: `level` - The level to get the planet data for.
- **Returns**: The planet data for the given level, or null if the level is not a planet.

#### `getPlanet(ResourceKey<Level> level)`

Gets the planet data for the given level, or null if the level is not a planet.

- **Parameters**: `level` - The level to get the planet data for.
- **Returns**: The planet data for the given level, or null if the level is not a planet.

#### `isPlanet(Level level)`

Returns true if the given level is a planet.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is a planet.

#### `isPlanet(ResourceKey<Level> level)`

Returns true if the given level is a planet.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is a planet.

#### `isSpace(Level level)`

Returns true if the given level is orbit.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is orbit.

#### `isSpace(ResourceKey<Level> level)`

Returns true if the given level is orbit.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is orbit.

#### `isExtraterrestrial(Level level)`

Returns true if the given level is a planet or orbit.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is a planet or orbit.

#### `isExtraterrestrial(ResourceKey<Level> level)`

Returns true if the given level is a planet or orbit.

- **Parameters**: `level` - The level to check.
- **Returns**: True if the level is a planet or orbit.

#### `getSolarPower(Level level)`

Returns the solar power energy result of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The solar power energy result of the given level.

#### `getSolarPower(ResourceKey<Level> level)`

Returns the solar power energy result of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The solar power energy result of the given level.