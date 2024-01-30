# Gravity API

Gravity is saved as a float per BlockPos. Entities will be affected by gravity if they are in a position with gravity.
Note that the gravity float is compacted to 15 bits rather than 32 bits, so it won't be as precise as a normal float.
Gravity is also unsigned, so negative values are not supported.

### Methods

#### `getGravity(Level level)`

Returns the gravity of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The gravity of the level.

#### `getGravity(ResourceKey<Level> level)`

Returns the gravity of the given level.

- **Parameters**: `level` - The level to check.
- **Returns**: The gravity of the level.

#### `getGravity(Level level, BlockPos pos)`

Returns the gravity of the given position.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
- **Returns**: The gravity of the position.

#### `getGravity(Entity entity)`

Returns the gravity of the given entity.

- **Parameters**: `entity` - The entity to check.
- **Returns**: The gravity of the entity.

#### `setGravity(Level level, BlockPos pos, float gravity)`

Sets the position's gravity to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.
    - `gravity` - The gravity to set.

#### `setGravity(Level level, Collection<BlockPos> positions, float gravity)`

Sets the gravity of the given positions to the given value.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The positions to check.
    - `gravity` - The gravity to set.

#### `removeGravity(Level level, BlockPos pos)`

Sets the gravity of the given position to the dimension's default gravity.

- **Parameters**:
    - `level` - The level to check.
    - `pos` - The position to check.

#### `removeGravity(Level level, Collection<BlockPos> positions)`

Sets the gravity of the given positions to the dimension's default gravity.

- **Parameters**:
    - `level` - The level to check.
    - `positions` - The positions to check.

#### `entityTick(Level level, LivingEntity entity, Vec3 travelVector, BlockPos movementAffectingPos)`

This method is called every tick for each living entity in the level.

- **Parameters**:
    - `level` - The level.
    - `entity` - The living entity to tick.
    - `travelVector` - The travel vector of the entity.
    - `movementAffectingPos` - The position affecting the entity's movement.