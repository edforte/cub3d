# cub3D

A Wolfenstein 3D–style first-person raycasting engine written from scratch in C with the [MiniLibX](https://github.com/42Paris/minilibx-linux) graphics library. Project of the 42 Common Core, built in a team of two: [SimoneFelici](https://github.com/SimoneFelici) and [EdoardoForte](https://github.com/edforte).

https://github.com/user-attachments/assets/0e87dd7f-8e9d-4b9c-9183-9d1d16273648

## Features

- Raycasting renderer based on the DDA algorithm, with textured walls and floor/ceiling colors
- Robust `.cub` parser: textures, RGB colors, map validation (closed walls, single player, valid characters)
- Smooth movement and rotation, wall collisions
- **Bonus:** interactive doors, minimap, HUD and mouse look
- No memory leaks: every resource is freed on exit or error

## Build & run

Requires Linux with X11 development libraries (`libx11-dev`, `libxext-dev`, `zlib1g-dev`).

```bash
make            # mandatory part
make bonus      # doors, minimap, HUD, mouse
./cub3D maps/good/dungeon.cub
```

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` | Move |
| `←` `→` / mouse | Rotate the camera |
| `E` | Open / close a door (bonus) |
| `ESC` | Quit |

## What I learned

Raycasting math, fixed-step DDA traversal, texture mapping, event-driven rendering loops, and splitting a large C codebase into a clean parser / engine architecture with a teammate.

Game assets by [Hajer](https://github.com/HajerZam).
