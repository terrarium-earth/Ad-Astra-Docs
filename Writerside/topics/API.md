# API

Ad Astra features a lightweight API for developers to safely interact with the various
systems and features of the mod.

<warning>
    <p>
        Ad Astra is made with Mojang mappings. Other mappings such as Yarn are not supported.
        Unless otherwise stated, all code in this wiki uses Mojang mappings.
    </p>
</warning>

## Definitions
- `Planet`: an encompassing term for any celestial body in the game, including planets and moons.
- `System`: A special effect that is applied per BlockPos.

## System APIs

Ad Astra has three main systems that can be interacted with: `Oxygen`, `Temperature`, and `Gravity`.
A "system" in Ad Astra is an special effect that is applied to blocks and entities.
All dimensions have a default system. For example, the Overworld has a default oxygen state of `true`,
a default temperature of `15`, and a default gravity of `9.807`. Systems are then overridden per-BlockPos,
meaning that you can have different oxygen, temperature, and gravity values in different parts of the same dimension.
Behind the scenes, systems are packed into a single `int` value, with 1 bit for oxygen, 16 bits for temperature, 
and 15 bits for gravity, equating to a total of 32 bits or exactly one `int`. These are then mapped to a packed BlockPos and 
saved to the world nbt in an int array.

Ad Astra has corresponding APIs for interacting with each system. These APIs allow you
to check the current state of a system for the given entity or BlockPos, and to modify the state of a system for the given BlockPos.

- [Oxygen API](Oxygen-API.md)
- [Temperature API](Temperature-API.md)
- [Gravity API](Gravity-API.md)

## Planet API

Ad Astra has an API for interacting with planets. The data for planets is defined in
a data pack, and can be accessed through this API.

- [Planet API](Planet-API.md)

## Events

Ad Astra has multiple events that can be hooked into. Note that Ad Astra does not use platform-specific events,
instead opting for a simple lambda-based event system.

- [Events](Events.md)