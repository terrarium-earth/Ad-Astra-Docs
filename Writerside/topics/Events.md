# Events

## Oxygen Tick Event

This event is fired serverside by every entity every 20 ticks (1 second) for each entity in the world.
Return false to cancel the ticking of oxygen for the entity.

### Example Usage {id="oxygen-tick-event-example-usage"}

```java
AdAstraEvents.OxygenTickEvent.register((level, entity) -> {
    // Code
});
```

## Entity Oxygen Event

This event is fired every time an entity checks for oxygen. Return a value not equal to 
the entity's current oxygen state to change the oxygen state of the entity.

### Example Usage {id="entity-oxygen-event-example-usage"}

```java
AdAstraEvents.EntityOxygenEvent.register((entity, hasOxygen) -> {
    // Code
});
```

## Temperature Tick Event

This event is fired serverside by every entity every 20 ticks (1 second) for each entity in the world.
Return false to cancel the ticking of temperature for the entity.

### Example Usage {id="temperature-tick-event-example-usage"}

```java
AdAstraEvents.TemperatureTickEvent.register((level, entity) -> {
    // Code
});
```

## Hot Temperature Tick Event

This event is fired serverside when an entity is taking damage from a hot temperature.
Return false to cancel the damage.

### Example Usage {id="hot-temperature-tick-event-example-usage"}

```java
AdAstraEvents.HotTemperatureTickEvent.register((level, entity) -> {
    // Code
});
```

## Cold Temperature Tick Event

This event is fired serverside when an entity is taking damage from a cold temperature.
Return false to cancel the damage.

### Example Usage {id="cold-temperature-tick-event-example-usage"}

```java
AdAstraEvents.ColdTemperatureTickEvent.register((level, entity) -> {
    // Code
});
```

## Gravity Tick Event

This event is fired every tick for every entity in the world. Return false to cancel 
the ticking of gravity for the entity and use normal gravity.

### Example Usage {id="gravity-tick-event-example-usage"}

```java
AdAstraEvents.GravityTickEvent.register((level, entity, travelVector, movementAffectingPos) -> {
    // Code
});
```

## Entity Gravity Event

This event is fired every time an entity checks for gravity. Return a value not equal to
the entity's current gravity state to change the gravity state of the entity.

### Example Usage {id="entity-gravity-event-example-usage"}

```java
AdAstraEvents.EntityGravityEvent.register((entity, gravity) -> {
    // Code
});
```

## Zero Gravity Event

This event is fired when an entity is in zero gravity. Return false to cancel the zero gravity movement.

### Example Usage {id="zero-gravity-event-example-usage"}

```java
AdAstraEvents.ZeroGravityEvent.register((level, entity, travelVector, movementAffectingPos) -> {
    // Code
});
```

## Acid Rain Tick Event

This event is fired serverside every 10 ticks (0.5 seconds) for each entity under acid rain.
Return false to cancel the damage from acid rain.

### Example Usage {id="acid-rain-tick-event-example-usage"}

```java
AdAstraEvents.AcidRainTickEvent.register((level, entity) -> {
    // Code
});
```

## Environment Tick Event

All planets tick blocks randomly in order to apply effects, such as freezing water, breaking blocks, etc.
This event is fired serverside every time a planet BlockState is randomly ticked. Return false to cancel
any effects to the BlockState.

### Example Usage {id="environment-tick-event-example-usage"}

```java
AdAstraEvents.EnvironmentTickEvent.register((level, pos, state, temperature) -> {
    // Code
});
```