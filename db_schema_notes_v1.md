# DB Schema Notes

Tables:
+ Components:
  + Name.
  + Brand data.
  + General Class: Spirit, Liqueur, Potable Bitters (including Amari), Non-Potable Bitters, Aromatized Wine/Fortified Wine, Other.
  + General Type: Rum, Rhum Agricole, Whisk(e)y, Bourbon/Rye/American Whisk(e)y, Gin/Genever, Vodka, Amaro, Bitters, Tequila, Mezcal, Other.
  + Source region.
  + ABV.
+ Specs:
  + Cocktail Name.
  + Cocktail Creator (if known).
  + Original source of spec.
  + URL.
  + Recipe, didactic.
  + Recipe, standardized.
  + Generic cocktail class. (Type of cocktail, generally, following Cocktail Codex: Old Fashioned, Martini, Daiquiri, Sidecar, Highball, Flip. Allow `None` or `Nil`.)
  + Generic process class. (Process class: built, stirred (built), stirred (mixing glass), shaken, blended, flash blended.)
  + Generic component list (serialized).
  + Preferred component list, when relevant, allow `None` or `Nil`.
  + Component amounts, in millitres. (Per IBA.)
  + Glassware.
  + Author (local authority for spec).
