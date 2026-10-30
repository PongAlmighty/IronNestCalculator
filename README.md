# Iron Nest Gun Laying

A fire-direction card for [IRON NEST: Heavy Turret Simulator](https://store.steampowered.com/app/2950790/). Enter the
turret-to-target range and powder charges, and it gives you the gun elevation. A firing log keeps a running list of
lined-up shots: shot number, shell type, bearing, charges, range and elevation.

It runs entirely in the browser: one HTML file, no build step and no dependencies. Open `index.html` to use it.

## The math

It uses the community firing rule players worked out from the game:

> elevation (°) = range (km) × 12 ÷ charges

Each charge adds 5 km of range and the gun tops out at 60°, so 1 charge reaches 5 km and 6 charges reach 30 km.
**Auto** picks the fewest charges that can reach the target. The game's developer has said on the Steam forums that
the ballistics are deliberately this simple, and players report every shell type uses the same elevation.

If an update changes the ballistics, open **Calibration** at the bottom of the page and adjust km per charge and
maximum elevation.

## Saved data

The firing log, the last shell type, units and calibration are saved in your browser's local storage. Nothing is
sent anywhere, and the log stays on the browser and device you used.

## Sources

- [Steam: Gun elevation confusion](https://steamcommunity.com/app/2950790/discussions/0/567037624436458799/) (developer-marked answer)
- [Steam: Quick Elevation Guide](https://steamcommunity.com/app/2950790/discussions/0/588434434320191280/)
- Shell list from [ironnest.buzz](https://ironnest.buzz/guides/shell-types/), which cites Destructoid's shell table

This is a fan-made tool and is not affiliated with the game's developers.
