# Humanoid bugs

This is a list of known bugs with humanoids, containing detailed information about the bugs, their reproduction steps, and potential workarounds.

<hr/>

## Setting `Humanoid.HipHeight` to 0 on R15 rigs

In any R15 rig, if you set `Humanoid.HipHeight` to 0, the humanoid will speed off in the direction it is facing when it makes contact with a surface, as if it were standing on a fast conveyor belt. This is due to the `HumanoidRootPart` touching the ground, which most likely causes miscalculation in collisions between the `HumanoidRootPart` and the surface it is on.

** Workarounds **

There are no known workarounds at this time.

??? bug "Reproduction"
    ```lua
    local Players = game:GetService("Players")

    Players.PlayerAdded:Connect(function(Player)
        Player.CharacterAdded:Connect(function(Character)
            Character:WaitForChild("Humanoid").HipHeight = 0
        end)
    end)
    ```

<hr/>

## Setting `HumanoidRootPart.CollisionGroupId` to a non-existant collision group

If `HumanoidRootPart.CollisionGroupId` is set to a collision group that does not exist, the humanoid will speed off in the direction it is facing when it makes contact with a surface, as if it were standing on a fast conveyor belt. This is due to `Humanoid.HipHeight` not being respected if the assigned group for `HumanoidRootPart` does not exist.

!!! note
    While `BasePart.CollisionGroupId` *can* be set by developers, the recommended way to assign collision groups is via `PhysicsService:SetPartCollisionGroup()`, as noted the [Roblox API documentation](https://developer.roblox.com/en-us/api-reference/property/BasePart/CollisionGroupId)


** Workarounds ** 

There are no known workarounds at this time.

??? bug "Reproduction"
    ```lua
    local Players = game:GetService("Players")

    Players.PlayerAdded:Connect(function(Player)
        Player.CharacterAdded:Connect(function(Character)
            Character:WaitForChild("HumanoidRootPart").CollisionGroupId = 1
        end)
    end)
    ```

<hr/>