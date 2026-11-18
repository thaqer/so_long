# so_long

A small 2D game made with MiniLibX for 42 Amman. Collect every item on the map, then reach the exit.

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` or arrow keys | move |
| `Esc` or closing the window | quit |

The move count is printed in the terminal.

## Maps

Maps are `.ber` text files built from these characters:

| Char | Meaning |
| --- | --- |
| `1` | wall |
| `0` | floor |
| `P` | player start (exactly one) |
| `C` | collectible (at least one) |
| `E` | exit (exactly one) |

A map must be rectangular and surrounded by walls, and every collectible and the exit must be reachable (checked with flood fill). See `maps/map.ber`.

## Build and run

Needs the X11 development libraries (`sudo apt install libx11-dev libxext-dev` on Ubuntu). `make` downloads [minilibx-linux](https://github.com/42Paris/minilibx-linux) into `minilibx/` the first time.

```sh
make
./so_long maps/map.ber
```

## Author

[thaqer](https://github.com/thaqer), 42 Amman.
