# MCEntity

## 导入相关包

It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import at the very top of the file.
```zenscript
import crafttweaker.api.entity.MCEntity;
```


## 方法

:::group{name=addTag}

Adds a new tag to the Entity.

 There is a limit of 1024 tags per Entity.

 These are **not** tags like MCTag<EntityType>, these are tags that are added by the /tag command.

 You can read more about how they can be used here: https://minecraft.fandom.com/wiki/Commands/tag

Return Type: boolean

```zenscript
// MCEntity.addTag(tag as string) as boolean

myMCEntity.addTag("foundMesa");
```

| 参数  | 类型     | 描述                          |
| --- | ------ | --------------------------- |
| tag | string | The name of the tag to add. |


:::

:::group{name=addVelocity}

Adds velocity to this Entity.

Return Type: void

```zenscript
// MCEntity.addVelocity(x as double, y as double, z as double) as void

myMCEntity.addVelocity(5, 9, -1);
```

| 参数 | 类型     | 描述                               |
| -- | ------ | -------------------------------- |
| x  | double | The amount of X velocity to add. |
| y  | double | The amount of Y velocity to add. |
| z  | double | The amount of Z velocity to add. |


:::

:::group{name=applyEntityCollision}

Applies entity collision between this Entity and the other Entity, pushing them away from each other.

Return Type: void

```zenscript
// MCEntity.applyEntityCollision(other as MCEntity) as void

myMCEntity.applyEntityCollision(entity);
```

| 参数    | 类型                                       | 描述                          |
| ----- | ---------------------------------------- | --------------------------- |
| other | [MCEntity](/vanilla/api/entity/MCEntity) | The Entity to collide with. |


:::

:::group{name=canSwim}

Checks if this Entity can swim.

Return Type: boolean

```zenscript
// MCEntity.canSwim() as boolean

myMCEntity.canSwim();
```

:::

:::group{name=changeDimension}

Teleports this Entity to the given world.

Return Type: void

```zenscript
// MCEntity.changeDimension(world as MCServerWorld) as void

myMCEntity.changeDimension(world);
```

| 参数    | 类型                                                | 描述                            |
| ----- | ------------------------------------------------- | ----------------------------- |
| world | [MCServerWorld](/vanilla/api/world/MCServerWorld) | The new world for the Entity. |


:::

:::group{name=extinguish}

Extinguishes the Entity if it is on fire.

Return Type: void

```zenscript
// MCEntity.extinguish() as void

myMCEntity.extinguish();
```

:::

:::group{name=forceFireTicks}

Sets the Entity on fire for the given amount of **ticks**.

 This method can be used to override how long the Entity is on fire for.

Return Type: void

```zenscript
// MCEntity.forceFireTicks(ticks as int) as void

myMCEntity.forceFireTicks(25);
```

| 参数    | 类型  | 描述                                              |
| ----- | --- | ----------------------------------------------- |
| ticks | int | The amount of ticks the Entity should burn for. |


:::

:::group{name=forceSetPosition}

Forcefully sets this Entity to the new position.

Return Type: void

```zenscript
// MCEntity.forceSetPosition(x as double, y as double, z as double) as void

myMCEntity.forceSetPosition(5, 2, 9);
```

| 参数 | 类型     | 描述               |
| -- | ------ | ---------------- |
| x  | double | The new X value. |
| y  | double | The new Y value. |
| z  | double | The new Z value. |


:::

:::group{name=getAir}

Gets the air value for the Entity. The air value is used to determine when the Entity will start drowning when swimming.

Return Type: int

```zenscript
// MCEntity.getAir() as int

myMCEntity.getAir();
```

:::

:::group{name=getBrightness}

Gets how bright this Entity is.

Return Type: float

```zenscript
// MCEntity.getBrightness() as float

myMCEntity.getBrightness();
```

:::

:::group{name=getData}

Gets the NBT data of this Entity.

Return Type: [MapData](/vanilla/api/data/MapData)

```zenscript
// MCEntity.getData() as MapData

myMCEntity.getData();
```

:::

:::group{name=getDistance}

Gets the distance between this Entity and the given Entity.

Return Type: float

```zenscript
// MCEntity.getDistance(other as MCEntity) as float

myMCEntity.getDistance(entity);
```

| 参数    | 类型                                       | 描述                                 |
| ----- | ---------------------------------------- | ---------------------------------- |
| other | [MCEntity](/vanilla/api/entity/MCEntity) | The Entity to get the distance to. |


:::

:::group{name=getDistanceSq}

Gets the squared distance from this Entity to the given Entity.

Return Type: double

```zenscript
// MCEntity.getDistanceSq(other as MCEntity) as double

myMCEntity.getDistanceSq(entity);
```

| 参数    | 类型                                       | 描述                                                 |
| ----- | ---------------------------------------- | -------------------------------------------------- |
| other | [MCEntity](/vanilla/api/entity/MCEntity) | The other Entity to check the squared distance to. |


:::

:::group{name=getDistanceSq}

Gets the squared distance from this Entity's position to the given position.

Return Type: double

```zenscript
// MCEntity.getDistanceSq(x as double, y as double, z as double) as double

myMCEntity.getDistanceSq(5, 6, 3);
```

| 参数 | 类型     | 描述                                            |
| -- | ------ | --------------------------------------------- |
| x  | double | The X value of the position to check against. |
| y  | double | The Y value of the position to check against. |
| z  | double | The Z value of the position to check against. |


:::

:::group{name=getEntityId}

Gets this Entity's id that can be used to reference this Entity.

Return Type: int

```zenscript
// MCEntity.getEntityId() as int

myMCEntity.getEntityId();
```

:::

:::group{name=getFacingDirections}

Gets which directions the Entity is currently facing.

Return Type: [Direction](/vanilla/api/util/Direction)[]

```zenscript
// MCEntity.getFacingDirections() as Direction[]

myMCEntity.getFacingDirections();
```

:::

:::group{name=getFireTimer}

Gets the amount of ticks the Entity will be on fire for.

Return Type: int

```zenscript
// MCEntity.getFireTimer() as int

myMCEntity.getFireTimer();
```

:::

:::group{name=getMaxInPortalTime}

Gets the maximum amount of time the Entity needs to be in the portal before they are teleported.

Return Type: int

```zenscript
// MCEntity.getMaxInPortalTime() as int

myMCEntity.getMaxInPortalTime();
```

:::

:::group{name=getName}

Gets the name of the Entity.

Return Type: string

```zenscript
// MCEntity.getName() as string

myMCEntity.getName();
```

:::

:::group{name=getPosition}

Gets this Entity's position in the world.

Return Type: [BlockPos](/vanilla/api/util/BlockPos)

```zenscript
// MCEntity.getPosition() as BlockPos

myMCEntity.getPosition();
```

:::

:::group{name=getTags}

Gets all the tags that are attached to the entity.

 These are **not** tags like MCTag<EntityType>, these are tags that are added by the /tag command.

 You can read more about how they can be used here: https://minecraft.fandom.com/wiki/Commands/tag

Return Type: Set&lt;string&gt;

```zenscript
// MCEntity.getTags() as Set<string>

myMCEntity.getTags();
```

:::

:::group{name=getType}

Gets this Entity's type.

Return Type: [MCEntityType](/vanilla/api/entities/MCEntityType)

```zenscript
// MCEntity.getType() as MCEntityType

myMCEntity.getType();
```

:::

:::group{name=getUUID}

Gets the UUID of this Entity.

Return Type: string

```zenscript
// MCEntity.getUUID() as string

myMCEntity.getUUID();
```

:::

:::group{name=getWorld}

Gets the World that this Entity is in.

Return Type: [MCWorld](/vanilla/api/world/MCWorld)

```zenscript
// MCEntity.getWorld() as MCWorld

myMCEntity.getWorld();
```

:::

:::group{name=hasNoGravity}

Checks if this Entity has no gravity.

Return Type: boolean

```zenscript
// MCEntity.hasNoGravity() as boolean

myMCEntity.hasNoGravity();
```

:::

:::group{name=isEntityInRange}

Checks if this Entity is in the given range (distance) of the other Entity.

Return Type: boolean

```zenscript
// MCEntity.isEntityInRange(entity as MCEntity, distance as double) as boolean

myMCEntity.isEntityInRange(entity, 2.5);
```

| 参数       | 类型                                       | 描述                                     |
| -------- | ---------------------------------------- | -------------------------------------- |
| entity   | [MCEntity](/vanilla/api/entity/MCEntity) | The Entity to check if it is in range. |
| distance | double                                   | The distance to check for.             |


:::

:::group{name=isImmuneToFire}

Checks if this Entity is immune to fire.

Return Type: boolean

```zenscript
// MCEntity.isImmuneToFire() as boolean

myMCEntity.isImmuneToFire();
```

:::

:::group{name=isInLava}

Checks if this Entity is in lava or not.

Return Type: boolean

```zenscript
// MCEntity.isInLava() as boolean

myMCEntity.isInLava();
```

:::

:::group{name=isInWater}

Checks if this Entity is in water.

Return Type: boolean

```zenscript
// MCEntity.isInWater() as boolean

myMCEntity.isInWater();
```

:::

:::group{name=isInWaterOrBubbleColumn}

Checks if this Entity is in water or a bubble column.

Return Type: boolean

```zenscript
// MCEntity.isInWaterOrBubbleColumn() as boolean

myMCEntity.isInWaterOrBubbleColumn();
```

:::

:::group{name=isInWaterRainOrBubbleColumn}

Checks if this Entity is in rain or a bubble column.

Return Type: boolean

```zenscript
// MCEntity.isInWaterRainOrBubbleColumn() as boolean

myMCEntity.isInWaterRainOrBubbleColumn();
```

:::

:::group{name=isOffsetPositionInLiquid}

Checks if the offset position from the Entity's current position is inside of a liquid.

Return Type: boolean

```zenscript
// MCEntity.isOffsetPositionInLiquid(x as double, y as double, z as double) as boolean

myMCEntity.isOffsetPositionInLiquid(5, 4, 5);
```

| 参数 | 类型     | 描述            |
| -- | ------ | ------------- |
| x  | double | The X offset. |
| y  | double | The Y offset. |
| z  | double | The Z offset. |


:::

:::group{name=isOnGround}

Checks whether the Entity is on the ground or not.

Return Type: boolean

```zenscript
// MCEntity.isOnGround() as boolean

myMCEntity.isOnGround();
```

:::

:::group{name=isSilent}

Checks if this Entity is silent.

 Silent Entities do not play sounds.

Return Type: boolean

```zenscript
// MCEntity.isSilent() as boolean

myMCEntity.isSilent();
```

:::

:::group{name=isSpectator}

Checks if this Entity is in spectator mode.

Return Type: boolean

```zenscript
// MCEntity.isSpectator() as boolean

myMCEntity.isSpectator();
```

:::

:::group{name=isWet}

Checks if this Entity is wet.

Return Type: boolean

```zenscript
// MCEntity.isWet() as boolean

myMCEntity.isWet();
```

:::

:::group{name=moveForced}

Forcefully moves this Entity to the new position.

Return Type: void

```zenscript
// MCEntity.moveForced(x as double, y as double, z as double) as void

myMCEntity.moveForced(5, 2, 9);
```

| 参数 | 类型     | 描述               |
| -- | ------ | ---------------- |
| x  | double | The new X value. |
| y  | double | The new Y value. |
| z  | double | The new Z value. |


:::

:::group{name=onCollideWithPlayer}

Triggers the collide effect between this Entity and the player.

 Some examples of collide effects are: Puffer fish damaging and applying poison. Experience orbs being collected.

Return Type: void

```zenscript
// MCEntity.onCollideWithPlayer(playerEntity as MCPlayerEntity) as void

myMCEntity.onCollideWithPlayer(player);
```

| 参数           | 类型                                                           | 描述                          |
| ------------ | ------------------------------------------------------------ | --------------------------- |
| playerEntity | [MCPlayerEntity #MC玩家实体](/vanilla/api/entity/MCPlayerEntity) | The player to collide with. |


:::

:::group{name=onKillCommand}

Can be used to simulate the `/kill` command being used on the Entity.

Return Type: void

```zenscript
// MCEntity.onKillCommand() as void

myMCEntity.onKillCommand();
```

:::

:::group{name=onLivingFall}

Can be used to simulate the Entity falling the given distance with the given damage multiplier.

Return Type: boolean

```zenscript
// MCEntity.onLivingFall(distance as float, damageMultiplier as float) as boolean

myMCEntity.onLivingFall(5, 5);
```

| 参数               | 类型    | 描述                                  |
| ---------------- | ----- | ----------------------------------- |
| distance         | float | The distance the Entity has fallen. |
| damageMultiplier | float | The damage multiplier.              |


:::

:::group{name=removeTag}

Removes a tag from the Entity.

 These are **not** tags like MCTag<EntityType>, these are tags that are added by the /tag command.

 You can read more about how they can be used here: https://minecraft.fandom.com/wiki/Commands/tag

Return Type: boolean

```zenscript
// MCEntity.removeTag(tag as string) as boolean

myMCEntity.removeTag("foundMesa");
```

| 参数  | 类型     | 描述                             |
| --- | ------ | ------------------------------ |
| tag | string | The name of the tag to remove. |


:::

:::group{name=setAir}

Sets the air value for the Entity

Return Type: void

```zenscript
// MCEntity.setAir(air as int) as void

myMCEntity.setAir(20);
```

| 参数  | 类型  | 描述                 |
| --- | --- | ------------------ |
| air | int | The new air value. |


:::

:::group{name=setEntityId}

This method is marked for removal next breaking change.

 It sets the ID of the entity, which is only used in networking code and should never have to be called by mods or scripts.

Return Type: void

```zenscript
// MCEntity.setEntityId(id as int) as void

myMCEntity.setEntityId(0);
```

| 参数 | 类型  | 描述 |
| -- | --- | -- |
| id | int | 0  |


:::

:::group{name=setFire}

Sets the Entity on fire for the given amount of **seconds**.

 This does not take ticks, it only takes full seconds, and you cannot lower the amount of fire ticks the entity has.

Return Type: void

```zenscript
// MCEntity.setFire(seconds as int) as void

myMCEntity.setFire(5);
```

| 参数      | 类型  | 描述                                                      |
| ------- | --- | ------------------------------------------------------- |
| seconds | int | The amount of seconds the Entity should be on fire for. |


:::

:::group{name=setNoGravity}

Sets this Entity to have no gravity.

Return Type: void

```zenscript
// MCEntity.setNoGravity(noGravity as boolean) as void

myMCEntity.setNoGravity(true);
```

| 参数        | 类型      | 描述                     |
| --------- | ------- | ---------------------- |
| noGravity | boolean | The new gravity value. |


:::

:::group{name=setOnGround}

Sets if the Entity should be considered on the ground or not.

Return Type: void

```zenscript
MCEntity.setOnGround(grounded as boolean) as void
```

| 参数       | 类型      | 描述                                     |
| -------- | ------- | -------------------------------------- |
| grounded | boolean | If the Entity is on the ground or not. |


:::

:::group{name=setPosition}

Sets the position of this Entity.

Return Type: void

```zenscript
// MCEntity.setPosition(x as double, y as double, z as double) as void

myMCEntity.setPosition(5, 2, 59);
```

| 参数 | 类型     | 描述                                |
| -- | ------ | --------------------------------- |
| x  | double | The new X position of the Entity. |
| y  | double | The new Y position of the Entity. |
| z  | double | The new Z position of the Entity. |


:::

:::group{name=setSilent}

Sets if this Entity is silent or not.

 silent Entities do not play sounds.

Return Type: void

```zenscript
// MCEntity.setSilent(isSilent as boolean) as void

myMCEntity.setSilent(true);
```

| 参数       | 类型      | 描述                                     |
| -------- | ------- | -------------------------------------- |
| isSilent | boolean | If the Entity should be silent or not. |


:::

:::group{name=teleportKeepLoaded}

Teleports the entity, forcing the destination to stay loaded for a short time

Return Type: void

```zenscript
// MCEntity.teleportKeepLoaded(x as double, y as double, z as double) as void

myMCEntity.teleportKeepLoaded(20, 40, 60);
```

| 参数 | 类型     | 描述                      |
| -- | ------ | ----------------------- |
| x  | double | No Description Provided |
| y  | double | No Description Provided |
| z  | double | No Description Provided |


:::

:::group{name=updateData}

Updates the NBT data of this Entity.

Return Type: void

```zenscript
// MCEntity.updateData(data as MapData) as void

myMCEntity.updateData({key: "value"});
```

| 参数   | 类型                                         | 描述                           |
| ---- | ------------------------------------------ | ---------------------------- |
| data | [MapData #地图数据](/vanilla/api/data/MapData) | The new Data for this Entity |


:::


## 参数

| 名称               | 类型                                                         | 可获得  | 可设置   | 描述                                                                                                                                     |
| ---------------- | ---------------------------------------------------------- | ---- | ----- | -------------------------------------------------------------------------------------------------------------------------------------- |
| air              | int                                                        | true | true  | Gets the air value for the Entity. <br />  The air value is used to determine when the Entity will start drowning when swimming. |
| canSwim #是否可以游泳  | boolean                                                    | true | false | Checks if this Entity can swim.                                                                                                        |
| data             | [MapData #地图数据](/vanilla/api/data/MapData)                 | true | false | Gets the NBT data of this Entity.                                                                                                      |
| facingDirections | [Direction](/vanilla/api/util/Direction)[]                 | true | false | Gets which directions the Entity is currently facing.                                                                                  |
| id               | int                                                        | true | false | Gets this Entity's id that can be used to reference this Entity.                                                                       |
| inLava           | boolean                                                    | true | false | Checks if this Entity is in lava or not.                                                                                               |
| inWater          | boolean                                                    | true | false | Checks if this Entity is in water.                                                                                                     |
| isWet            | boolean                                                    | true | false | Checks if this Entity is wet.                                                                                                          |
| name             | string                                                     | true | false | Gets the name of the Entity.                                                                                                           |
| onGround         | [MCEntity](/vanilla/api/entity/MCEntity)                   | true | true  | Sets if the Entity should be considered on the ground or not.                                                                          |
| position         | [BlockPos](/vanilla/api/util/BlockPos)                     | true | false | Gets this Entity's position in the world.                                                                                              |
| silent           | boolean                                                    | true | true  | Checks if this Entity is silent. <br />  <br />  Silent Entities do not play sounds.                                       |
| spectator        | boolean                                                    | true | false | Checks if this Entity is in spectator mode.                                                                                            |
| 类型               | [MCEntityType #MC实体类型](/vanilla/api/entities/MCEntityType) | true | false | Gets this Entity's type.                                                                                                               |
| uuid             | string                                                     | true | false | Gets the UUID of this Entity.                                                                                                          |
| world            | [MCWorld](/vanilla/api/world/MCWorld)                      | true | false | Gets the World that this Entity is in.                                                                                                 |
