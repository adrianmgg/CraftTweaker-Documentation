# Soils

Class path: `mods.botanypots.Soil`

## Use

To use, import the class with `import mods.botanypots.Soil;` at the beginning of your script.

## Creating New Soils

`Soil.create(id, ingredient, displayState, tickRate, categories);`

- `id` &lt;string> The id of the new soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `ingredient` <[IIngredient](/vanilla/api/items/IIngredient)> The ingredient used to determine which items/blocks are used to put the soil in a pot.
- `displayState` <[MCBlockState](/vanilla/api/blocks/MCBlockState)> The block state to display for the soil in the pot.
- `tickRate` &lt;int> The tick rate for the soil.
- `categories` &lt;string[]> An array of categories associated with the new soil.

Creates a new soil entry that players can use in the botany pot.

```zenscript
Soil.create("examplepack:rock", <item:minecraft:stone>, <blockstate:minecraft:stone>, 100, ["rocky"]);
```

## Removing A Soil

`Soil.remove(id);`

- `id` &lt;string> The id of the soil to remove. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.

Removes a soil from the game's data.

```zenscript
Soil.remove("botanypots:soil/podzol");
```

## Changing Soil Tick Rate

`Soil.setTicks(id, tickRate);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `tickRate` &lt;int> The new tick rate for the soil.

Changes the tick rate of a given soil.

```zenscript
Soil.setTicks("botanypots:soil/grass", 1300);
```

## Changing Soil Ingredient

`Soil.setIngredient(id, ingredient);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `ingredient` <[IIngredient](/vanilla/api/items/IIngredient)> The ingredient used to determine which items/blocks are used to put the soil in a pot.

Changes the items used to put the soil into the botany pot.

```zenscript
Soil.setIngredient("botanypots:soil/soul_sand", <item:minecraft:sand>);
```

## Changing Soil Display

`Soil.setDisplayState(id, displayState);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `displayState` <[MCBlockState](/vanilla/api/blocks/MCBlockState)> The block state to display for the soil in the pot.

Changes the block displayed for the soil.

```zenscript
Soil.setDisplayState("botanypots:soil/dirt", <blockstate:minecraft:snow>);
```

## Changing Soil Categories

Changes the categories associated with the soil. These are used to match crops to valid soils.

### Add a Category to a Soil

`Soil.addCategory(id, categoriesToAdd);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `categoriesToAdd` &lt;string[]> An array of categories to associate with the soil.

```zenscript
Soil.addCategory("botanypots:soil/soul_sand", ["nether"]);
```

### Remove a Category From a Soil

`Soil.removeCategory(id, categoriesToRemove);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.
- `categoriesToRemove` &lt;string[]> An array of categories to dissociate with the soil.

```zenscript
Soil.removeCategory("botanypots:soil/soul_sand", ["soul_sand"]);
```

### Clear All Categories From a Soil

`Soil.clearCategories(id);`

- `id` &lt;string> The id of the soil. 유효한 `namespace:path` 형식의 이름공간이 붙은 ID여야 합니다.

```zenscript
Soil.clearCategories("botanypots:soil/farmland");
```

## 모든 ID 보기

`Soil.getAllIds();`

- Returns: &lt;string[]> An array of all known soil ids at the time this is ran.

This will give you an array of all the known soil ids at the time.

```zenscript
// Log all ids to the crafttweaker.log file
for soilId in Soil.getAllIds() {
    println(soilId);
}
```

## Removing All Soil

This will completely remove all the soils currently registered. 스크립트를 통해 모든 데이터를 다시 만들고자 하는 경우 유용합니다.

```zenscript
Soil.removeAll();
```