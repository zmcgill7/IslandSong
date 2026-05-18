# Color Restoration System

Island Song's core fantasy is that music restores life and color to a gray island. The color restoration mechanic needed to support that fantasy while still being practical inside Unreal Engine.

## Original Mechanic

The team documented an early version of the mechanic using a post-process material, a material parameter collection, a player location vector, and a scalar radius. A sphere mask determined which world pixels stayed in color and which were desaturated. Timelines controlled animated radius changes.

That first version established the visual language: color could grow outward over time and mark progress through the world.

## My Implementation Focus

My later contribution expanded the idea into a more reusable function-library approach for restoration scenes:

- Restoration could radiate from arbitrary 3D points, not only the player.
- Radius behavior could be animated and reused across different events.
- Easy to use bounding capabilities for complex shapes helped constrain where restoration should appear.
- The implementation repurposed Unreal Engine's landscape-painting tools. The team would only need to create a runtime virtual texture (RVT) as a 2D plane. Then draw using an intuitive paint brush tool that is designed for sculpting landscapes. Since RVT's are highly optimized for rendering graphics I was able to use this to support efficent color restoration over world areas.

## Why It Was Hard

The mechanic crossed several Unreal systems at once:

- World-space visual effects.
- Blueprint-driven gameplay events.
- Landscape/material behavior.
- Spatial bounds and restoration masks.
- Artist/designer usability.

The result was a mechanic that connected the game's narrative identity to a reusable technical system.
