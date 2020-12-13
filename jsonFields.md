# JSON Prototype

Fields:

+ `nameS` - Cocktail name.
+ `defaultGlassS` - Default type of glassware (picklist?).
+ `instructionS` - Narrative instructions for making the cocktail.
+ `genericProcessClassS` - Process class: built, stirred (built), stirred (mixing glass), shaken.
+ `genericCocktailClassS` - Type of cocktail (generally) following _Cocktail Codex_: Old Fashioned, Martini, Daiquiri, Sidecar, Highball, Flip. Allow Python `None`.
+ `genericIngredientsL` - Python list (serialized as string) of ingredient classes.
+ `preferredIngredientsL` - List of preferred brands when relevant; allow `None`.
+ `mlMeasuresL` - List of amounts in millilitres (ml). All other conversions done via interfaces. There need to be rules for rounding appropriately; both on input and output. IBA uses ml.
+ `sourceS` - Source of data; usually a URL?

Several of the items in the list above are **synchronized** lists and need error checking/validation at input.

Test, using Python and `dataset` library to connect to `sqlite`.

```python
 OrderedDict([('id', 2),
              ('name', 'Green Goblin'),
              ('glass', 'pint glass'),
              ('instructions',
               'Add cider first, then layer in cider followed by curacao.'),
              ('genericCocktailClass', None),
              ('genericIngredients',
               "['hard cider', 'lager beer', 'blue curacao']"),
              ('mlMeasures', '[473, 473, 30]'),
              ('source', 'thecocktaildb.com'),
              ('genericProcessClass', 'built')])]
```

Serialized as JSON:

```json
{
    "genericCocktailClass": null,
    "genericIngredients": "['hard cider', 'lager beer', 'blue curacao']",
    "genericProcessClass": "built",
    "glass": "pint glass",
    "id": 2,
    "instructions": "Add cider first, then layer in cider followed by curacao.",
    "mlMeasures": "[473, 473, 30]",
    "name": "Green Goblin",
    "source": "thecocktaildb.com"
}
```
