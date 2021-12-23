# Commands and Syntax for Nihilego

# Unimplemented

## `Meta`
`Meta` commands are ones that don't show up as items/Pokemon, along with various constants

### `Meta.SetMode`
Sets mode to one of the following:

`item`

`pkmn`

`raw`

### `Meta.ShinySpread`
Constant which holds the max Shiny Spread IVs

### `Meta.Assert`
Makes an assertion

## `Spc`
`Spc` commands are misc. commands

### `Spc.RawOut`
Allows for raw data:
```
Spc.RawOut(01)
```
would turn into a Master Ball (0x01)

### `Spc.RoundAbout`
Uses a roundabout technique to create a number, helpful for box Pokemon:
```
Spc.RoundAbout(01)
```
would become
```
LD E, $00
LD A, $01
ADD E
LD E, A
```

## `Poke`
`Poke` commands hold various helpful things for dealing with Pokemon:
### `Poke.SetPokeSpecies`
Sets a Pokemon species (**does not update count**)
```
Poke.SetPokeSpecies(21, 0)
```
would modify ($D164 + 0) to become 0x21

### `Poke.AddPoke`
Appends a Pokemon to the end of the party:
```
Poke.AddPoke(21)
```
would modify ($D164 + $D163) to become 0x21



