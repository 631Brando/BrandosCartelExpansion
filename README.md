# Brando's Cartel Expansion

A work-in-progress cartel questline with custom cartel safehouses, 15+ new drugs with complex recipes, new clothing and new lab equipment. Currently in alpha, with plenty more to come.

**Download:** [Releases](https://github.com/631Brando/BrandosCartelExpansion/releases/latest) · [Nexus Mods](https://www.nexusmods.com/drugdealersimulator2/mods/28)

---

## Installing

### With DDS2 Mod Manager (recommended)

Drag the release archive onto the manager window, or use **Install Mod...**. It reads what is
actually inside the pak, works out that this is a LogicMod, and puts the files where they
belong — and it will tell you if this mod conflicts with anything else you have installed.

The manager: <https://github.com/631Brando/DDS2ModManager>

### By hand

A packaged mod is three files that always travel together:

```
BrandosCartelExpansion_P.pak
BrandosCartelExpansion_P.ucas
BrandosCartelExpansion_P.utoc
```

Put all three into:

```
<game folder>\DrugDealerSimulator2\Content\Paks\LogicMods\
```

All three are required. A `.pak` on its own will not load: the asset data lives in the `.ucas`
and the index that finds it lives in the `.utoc`.

## Requirements

- Drug Dealer Simulator 2
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) — DDS2 Mod Manager can install it for you

## Updates

This mod carries its own update address, so DDS2 Mod Manager can tell players when a new
version is published here. The `ModActor` Blueprint sets:

| Variable | Value |
|---|---|
| `ModUpdateUrl` | `https://github.com/631Brando/BrandosCartelExpansion` |
| `ModVersion` | the version of that build — currently `0.4.1` |

The manager checks this repository's releases and offers the update. **Nothing installs without
the player agreeing to it**, whether or not they have trusted the author.

> The address is pinned on each player's machine the first time it is seen, and compared
> afterwards as the exact string above. Reformatting it in a later release — a trailing slash,
> a `.git`, a dropped `https://` — reads as *the update address has moved* and warns every
> player. It has to stay byte-for-byte identical.

## Reporting a problem

Open an issue here. If it misbehaves in game, DDS2 Mod Manager's **Save Log** button (or the
**Diagnostics** bundle) collects everything worth attaching.

## Source

Built with the [DDS2 Cooked Editor SDK](https://github.com/631Brando/DrugDealerSimulator2_CookedEditor).
This repository distributes the packaged mod; it does not host the Unreal source assets.

