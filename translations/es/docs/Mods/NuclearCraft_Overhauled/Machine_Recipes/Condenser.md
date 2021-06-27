# Condenser
**Note: Partially Broken**

## Importing the Package
`mods.nuclearcraft.CondenserCondenser`

## Adding Recipes
```zenscript
mods.nuclearcraft.mods.nuclearcraft.Condenser.addRecipe(ILiquidStack fluidInput, ILiquidStack fluidOutput, @Optional double coolingRequired, @Optional int condensingTemperature);
```

## Removing Recipes
```zenscript
mods.nuclearcraft.Condenser.removeRecipeWithInput(ILiquidStack fluidInput);
mods.nuclearcraft.mods.nuclearcraft.Condenser.removeRecipeWithInput(ILiquidStack fluidInput);
mods.nuclearcraft.Condenser.removeRecipeWithOutput(ILiquidStack fluidOutput);
mods.nuclearcraft.Condenser.removeAllRecipes();Condenser.removeAllRecipes();
```