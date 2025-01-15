# EntityEvents.checkSpawn

## Basic info

- Valid script types: [SERVER, CLIENT]

- Has result? ✔

- Event class: [CheckLivingEntitySpawnEventJS](https://github.com/KubeJS-Mods/KubeJS/tree/2001/common/src/main/java/dev/latvian/mods/kubejs/entity/CheckLivingEntitySpawnEventJS.java)

```
Invoked before an entity is spawned into the world.

Only entities from a `BaseSpawner` or world generation will trigger this event.
```

### Available fields:

| Name | Type | Static? |
| ---- | ---- | ------- |
| x | double | ✘ |
| y | double | ✘ |
| z | double | ✘ |
| type | MobSpawnType | ✘ |
| spawner | BaseSpawner | ✘ |

Note: Even if no fields are listed above, some methods are still available as fields through *beans*.

### Available methods:

| Name | Parameters | Return type | Static? |
| ---- | ---------- | ----------- | ------- |
| getSpawner |  |  | BaseSpawner | ✘ |
| getEntity |  |  | LivingEntity | ✘ |
| getBlock |  |  | BlockContainerJS | ✘ |
| getLevel |  |  | Level | ✘ |
| getType |  |  | MobSpawnType | ✘ |
| getPlayer |  |  | Player | ✘ |
| getServer |  |  | MinecraftServer | ✘ |
| success |  |  | Object | ✘ |
| success | Object |  | Object | ✘ |
| cancel | Object |  | Object | ✘ |
| cancel |  |  | Object | ✘ |
| exit | Object |  | Object | ✘ |
| exit |  |  | Object | ✘ |


### Documented members:

- `BaseSpawner getSpawner()`
```
The spawner that spawned the entity. Can be null if the entity was spawned by worldgen.
```

- `LivingEntity getEntity()`
```
The entity being spawned.
```

- `BlockContainerJS getBlock()`
```
The block the entity is being spawned on.
```

- `Level getLevel()`
```
The level the entity is being spawned into.
```

- `MobSpawnType getType()`
```
The type of spawn.
```

- `Object success()`
```
Stops the event with default exit value. Execution will be stopped **immediately**.

`success` denotes a `true` outcome.
```

- `Object success(Object var0)`

  Parameters:
  - var0: Object

```
Stops the event with the given exit value. Execution will be stopped **immediately**.

`success` denotes a `true` outcome.
```

- `Object cancel(Object var0)`

  Parameters:
  - var0: Object

```
Cancels the event with the given exit value. Execution will be stopped **immediately**.

`cancel` denotes a `false` outcome.
```

- `Object cancel()`
```
Cancels the event with default exit value. Execution will be stopped **immediately**.

`cancel` denotes a `false` outcome.
```

- `Object exit(Object var0)`

  Parameters:
  - var0: Object

```
Stops the event with the given exit value. Execution will be stopped **immediately**.

`exit` denotes a `default` outcome.
```

- `Object exit()`
```
Stops the event with default exit value. Execution will be stopped **immediately**.

`exit` denotes a `default` outcome.
```



### Example script:

```js
EntityEvents.checkSpawn(/* extra_id (optional), */ (event) => {
	// This space (un)intentionally left blank
});
```
