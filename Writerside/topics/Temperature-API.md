# Temperature API

Temperature is saved as a short per BlockPos. Entities will take either burning damage if it's too hot, or freezing damage if it's too cold.

### Methods

#### `getTemperature(Level level)`

Returns the temperature of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The temperature of the level.

#### `getTemperature(ResourceKey<Level> level)`

Returns the temperature of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The temperature of the level.

#### `getTemperature(Level level, BlockPos pos)`

Returns the temperature of the given position.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: The temperature of the position.

#### `getTemperature(Entity entity)`

Returns the temperature of the given entity.

- **Parameters**: `entity` - The entity to check.
- **Returns**: The temperature of the entity.

#### `setTemperature(Level level, BlockPos pos, short temperature)`

Sets the position's temperature to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
    - `temperature` - The temperature to set.

#### `setTemperature(Level level, Collection<BlockPos> positions, short temperature)`

Sets the temperature of the given positions to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The positions to check.
    - `temperature` - The temperature to set.

#### `removeTemperature(Level level, BlockPos pos)`

Sets the temperature of the given position to the dimension's default temperature.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.

#### `removeTemperature(Level level, Collection<BlockPos> positions)`

Sets the temperature of the given positions to the dimension's default temperature.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The positions to check.

#### `isLiveable(Level level, BlockPos pos)`

Returns whether the temperature of the given position is within a liveable range.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: If the temperature is liveable or not.

#### `isHot(Level level, BlockPos pos)`

Returns whether the temperature of the given position is too hot to be liveable.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: If the temperature is too hot or not.

#### `isCold(Level level, BlockPos pos)`

Returns whether the temperature of the given position is too cold to be liveable.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: If the temperature is too cold or not.

#### `entityTick(ServerLevel level, LivingEntity entity)`

This method is called every tick for each living entity in the server level.

- **Parameters**:
    - `level` - The server level.
    - `entity` - The living entity to tick.