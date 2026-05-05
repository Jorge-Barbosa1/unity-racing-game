# Unity Racing Game

> **Suggested repo description:** *Unity 3D racing game with lap timing, single-player and 1v1 modes, and multiple track environments.*
>
> **Suggested topics:** `unity`, `unity3d`, `csharp`, `racing-game`, `game-development`, `easyroads3d`

A 3D racing game built in Unity for the **Multimedia Technologies** course in the Bachelor's Degree in Informatics Engineering at IPVC. Drive around custom-built tracks, with lap timing, configurable game modes, and audio-reactive engine sound.

![gameplay](docs/demo.gif) <!-- add a screenshot or short GIF before publishing -->

## Features

- **Vehicle physics** — `WheelColliders` driving the wheels, configurable motor power, brake power, max speed, and a steering animation curve for realistic feel (`PlayerController.cs`).
- **Lap timer** — millisecond-precise per-lap timing with multiple checkpoint triggers (`TimePerLap.cs`).
- **Game modes** — single-player and 1v1 toggle exposed via a static `GameMode` flag, switching scenes accordingly.
- **Engine audio** — pitch-modulated engine sound that responds to the car's RPM (`EngineAudioController.cs`).
- **Multiple tracks** — built using the *Environmental Race Track Pack* and *EasyRoads3D* for road generation, with custom interface scenes.
- **HUD** — speedometer and lap-time display rendered with TextMeshPro.

## Stack

- **Engine:** Unity (3D, Built-in Render Pipeline)
- **Language:** C#
- **Notable assets used:** EasyRoads3D, Environmental Race Track Pack, FlamingSands_Cars, Conifers [BOTD], TextMeshPro, Car Engine Sound (i6 German Free)

## Project structure

```
Assets/
├── Scripts/
│   ├── PlayerController.cs       # Car physics, input, speed, steering
│   ├── CamController.cs          # Chase camera
│   ├── EngineAudioController.cs  # RPM-driven engine sound
│   ├── TimePerLap.cs             # Lap timer with checkpoint triggers
│   ├── EndLapController.cs       # End-of-lap handling
│   ├── GameManager.cs            # Scene + game flow
│   ├── GameMode.cs               # Singleplayer / 1v1 flag
│   └── INTERFACE.cs / Interface2.cs / Interface3.cs   # Menu logic
├── Levels/                       # Custom interface and gameplay scenes
├── Scenes/                       # Track scenes
├── Player.prefab                 # The drivable car
└── (third-party asset folders)
```

## Run it

1. Open the project in **Unity** (matching the Unity version used to build it — see `ProjectSettings/ProjectVersion.txt`).
2. Open one of the scenes under `Assets/Levels/` or `Assets/Scenes/`.
3. Press Play.

## Status

Course project, not maintained. Useful as a starting point for Unity racing prototypes (vehicle physics, lap timing, audio integration).
