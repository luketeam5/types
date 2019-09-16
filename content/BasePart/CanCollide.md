The CanCollide property determines whether a part will physically interact with other parts. When disabled, other parts can pass through the brick uninterrupted. Parts used for **decoration** usually have CanCollide disabled, as they need not be considered by the physics engine.

If a part is not [BasePart.Anchored](https://developer.roblox.com/api-reference/property/BasePart/Anchored) and has CanCollide disabled, it may fall out of the world to be eventually destroyed by [Workspace.FallenPartsDestroyHeight](https://developer.roblox.com/api-reference/property/Workspace/FallenPartsDestroyHeight). Therefore, it is usually desirable to anchor such parts or join them to another part that is anchored so that they don't fall out of the level. You can also use an object like `/BodyPosition` or `/BodyForce` to prevent falling out of the level entirely.

Even when CanCollide is disabled, parts may still fire the [BasePart.Touched](https://developer.roblox.com/api-reference/event/BasePart/Touched) event (as well the other parts touching them). In addition, a part allow other parts to pass through even if CanCollide is enabled if their collision groups are not set to collide with each other. Part collision groups are managed by `/PhysicsService`.