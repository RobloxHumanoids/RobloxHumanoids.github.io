# Humanoid/avatar symptoms

This page contains a list of symptoms, each linking to humanoid bugs that may be causing them.

<hr/>

## Avatar sinks into ground and slides everywhere

The avatar appears sunk into the ground, and it randomly slides in whatever direction it is facing.

** Possible causes **

If the avatar is using an R15 rig, [Setting `Humanoid.HipHeight` to 0](./Bugs.md#setting-humanoidhipheight-to-0-on-r15-rigs) might be the cause.

If you are using an R6 or R15 rig and you are directly setting collision group IDs, [you might be setting a humanoid root part to a non-existant collision group](./Bugs.md#setting-humanoidrootpartcollisiongroupid-to-a-non-existant-collision-group).

<hr/>