# SourceMod RTS Starter
**SourceMod RTS Starter** is a proof-of-concept implementation for a Real-Time Strategy (RTS) camera control setup with support for screen-space to world-space point-and-click selection.  It is written in pure SourcePawn and only requires SourceMod running on a Team Fortress 2 server.

Please note the cursor and other movement speeds and sensitivity settings have been hard-coded and should be edited and configured for your implementation.  Users may also have specific preferences that depend on game settings and server latency.

**Custom bots used during testing and demonstration are not part of this release.**

## Features
- Edge scrolling
- WASD-keys scrolling
- Drag-to-scroll (hold right mouse button and drag)
- Zooming (scroll with mouse wheel, see below for binds)
- Rotation (hold mouse wheel down and drag, can be used while scrolling for fly-through)
- Clip camera angles and movements to bounding box
- Left-click to select units (drag rectangle to select multiple)
- Right-click to apply an action to selected units
- Colored health bars drawn above selected unit entities that are visible through walls

## Demonstration Videos
https://github.com/geominorai/sm-rts-starter/assets/13911156/eb8c9126-0e0f-4913-8186-6b55379b0327

https://github.com/geominorai/sm-rts-starter/assets/13911156/e757dda6-cdbf-4be3-9800-92ab2adc6388

https://github.com/geominorai/sm-rts-starter/assets/13911156/26235b3a-06c5-420b-841b-96aa920febf1

https://github.com/geominorai/sm-rts-starter/assets/13911156/5ea4ad68-0d70-43ac-b4a0-6ddec3c7b31a

https://github.com/geominorai/sm-rts-starter/assets/13911156/bfbea860-095c-4461-9f7a-a3c9af8946dc

## Commands
```
sm_rts [min_x min_y min_z max_x max_y max_z] - Enter and exit RTS mode
sm_rts_zoom_in                               - Camera zoom in
sm_rts_zoom_out                              - Camera zoom out

sm_rts_aspect_ratio <ratio>                  - Set camera aspect ratio
sm_rts_aspect_ratio <width> <height>         - Set camera aspect ratio calculated with width and height
```

## Recommended Binds
```
bind MWHEELUP sm_rts_zoom_in
bind MWHEELDOWN sm_rts_zoom_out
```

## Example Test Map
This project was developed and tested on [`jump_academy_classic_b`](https://jumpacademy.tf/maps/jump_academy_classic_b) inside the Market Gardening Arena (MGA) part of the map.  Use the `sm_rts` command with the corresponding bounding box values as follows to start:
`sm_rts 6680 -3750 -1035 10200 -300 785`

## Dependencies
* [SourceMod](https://www.sourcemod.net/) (1.12.0.7038 or newer)
* [SMLib](https://github.com/bcserv/smlib/tree/transitional_syntax)
