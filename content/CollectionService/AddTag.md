AddTag will apply a tag to an object. This method will not throw an error if the object already had the tag. Successfully adding a tag will fire a signal created by [CollectionService.GetInstanceAddedSignal](https://developer.roblox.com/api-reference/function/CollectionService/GetInstanceAddedSignal) with the given tag.

**Warning:** When tagging an object, it is common that some resources are used to give the tag its functionality, e.g. event connections or tables. To prevent memory leaks, it is a good idea to clean these up (disconnect, set to nil, etc) when no longer needed for a tag. Do this when calling [CollectionService.RemoveTag](https://developer.roblox.com/api-reference/function/CollectionService/RemoveTag), calling [Instance.Destroy](https://developer.roblox.com/api-reference/function/Instance/Destroy) or in a function connected to a signal returned by [CollectionService.GetInstanceRemovedSignal](https://developer.roblox.com/api-reference/function/CollectionService/GetInstanceRemovedSignal).