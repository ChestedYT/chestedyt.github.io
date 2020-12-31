## This module is server sided

### Remember to add
```lua
require(game.ServerScriptService.StandModules)
```

### module.takeDamage
```
module.takeDamage(char, targetChar, hp)
```
Deal damage to target

### module.heal
```
module.heal(char, targetChar, hp)
```
Heal Target

### module.onHit
```
module.onHit(char, targetChar, timeDelay, effectType)
```
timeDelay = camera shake delay (.1s) Default
effectType : "Strong" or "Normal"


### module.createHitbox
```lua
local a = module.createHitbox(limb)

--for removing hitbox
a:Destroy() 
game:GetService("Debris"):AddItem(a, .1)
```
creates 2x2x2 hitbox on the selected limb


### module.knockback
```
module.knockback(char, targetChar, power)
```
knockbacks enemy


### module.ragdoll(targetChar)
### module.unragdoll(targetChar)

### module.standJump(char)
stand leap/stand jump
(will update this in the future)

### module.noGrav
```lua
local a = module.noGrav(char)

--for removing anti gravity
a:Destroy()
game:GetService("Debris"):AddItem(a,.1)
```
Basically Anti Gravity or (0,0,0) Velocity
