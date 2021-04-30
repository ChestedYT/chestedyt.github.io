### AE Module
```lua
--Remember to add this
local module = require(game.ServerScriptService.StandModules)
```

### module.takeDamage(playerChar, targetChar, hp)
```
module.takeDamage(playerChar, targetChar, 10)
```

### module.heal(playerChar, targetChar, hp)
```
module.heal(playerChar, targetChar, 10)
```

### module.onHit(playerChar, targetChar, timeDelay, effectType)
```
module.onHit(playerChar, targetChar, .1, "Strong") --pls set timeDelay to .1 everytime (ik its unnecessarily)
--effectType : "Strong" or "Normal"
```

### module.createHitbox(part)
```lua
local a = module.createHitbox(part)
-- creates hitbox on the selected part with its size
game.Debris:AddItem(a, .1)
```



### module.knockback(playerChar, targetChar, power, direction)
```lua
module.knockback(playerChar, targetChar, 5, "Front")
--Direction : Up, Front, AOE [Center is at playerChar HRP Position]
```


### module.ragdoll(targetChar)
### module.unragdoll(targetChar)

### module.stunPlr(targetChar, duration, playStunAnimation)
```lua
local a = module.createHitbox(limb)
a.Touched:Connect(function(hit)
  if hit.Parent:FindFirstChild("HumanoidRootPart") and hit.Parent:FindFirstChild("Ragdoll") then --hit.Parent:FindFirstChild("Ragdoll") prevents dialogNPC from getting detected
    module.stunPlr(hit.Parent, 5, true)
  end
end)
```

### module.explode(playerChar, targetChar, hp)
```lua
module.explode(playerChar, targetChar, 20) --Has Explosion Effect and Doesn't require module.takedamage
```

### module.playSound(char, sound, types)
```lua
--Source for this
function module.playSound(char, sound, types)
	if types == nil then
		local sounds = sound:Clone()
		sounds.Parent = char.Torso
		return sounds
	elseif types == "Stand" then
		local sounds = sound:Clone()
		sounds.Parent = char
		return sounds
	end
end
```

### module.hitAnim(targetChar)
```lua
--Play random hit animation on selected character/npc
```

### module.AdjustSpeed(char, WalkSpeed, DebrisTime, DontParent)
```lua
standmod.AdjustSpeed(Target, 4, 2)
--that would set their speed to 4 for 2 seconds
--and lets say for example another script does 
standmod.AdjustSpeed(Target, 8, 2)
--their speed will stay at 4
```
