# Oxygen API

Oxygen is saved as a boolean per BlockPos. Entities will take oxygen damage if they are in a position without oxygen.

### Methods

#### `hasOxygen(Level level)`

Returns whether the given level has oxygen.

- **Parameters**: `level` - The level to check.
- **Returns**: Whether the level has oxygen.

#### `hasOxygen(ResourceKey<Level> level)`

Returns whether the given level has oxygen.

- **Parameters**: `level` - The level to check.
- **Returns**: Whether the level has oxygen.

#### `hasOxygen(Level level, BlockPos pos)`

Returns whether the given position has oxygen.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: Whether the position has oxygen.

#### `hasOxygen(Entity entity)`

Returns whether the given entity has oxygen.

- **Parameters**: `entity` - The entity to check.
- **Returns**: Whether the entity has oxygen.

#### `setOxygen(Level level, BlockPos pos, boolean oxygen)`

Sets the position's oxygen presence to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to add oxygen to.
    - `oxygen` - The oxygen to set.

#### `setOxygen(Level level, Collection<BlockPos> positions, boolean oxygen)`

Sets the oxygen presence of the given positions to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The position to add oxygen to.
    - `oxygen` - The oxygen to set.

#### `removeOxygen(Level level, BlockPos pos)`

Sets the oxygen of the given position to the dimension's default oxygen.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to remove oxygen from.

#### `removeOxygen(Level level, Collection<BlockPos> positions)`

Sets the oxygen of the given position to the dimension's default oxygen.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The positions to remove oxygen from.

#### `entityTick(ServerLevel level, LivingEntity entity)`

This method is called every tick for each living entity in the server level.

- **Parameters**:
    - `level` - The server level.
    - `entity` - The living entity to tick.