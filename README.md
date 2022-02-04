# qb-inventory_oldver
this a new inventory created by loljoshie#0001 or https://github.com/loljoshie make it to work with old qb-core


add this to qb-core\client\functions.lua
```
function QBCore.Functions.GetPlate(vehicle)
    if vehicle == 0 then return end
    return QBCore.Shared.Trim(GetVehicleNumberPlateText(vehicle))
end

```

add this to qb-core\shared.lua
```
QBShared.Trim = function(value)
	if not value then return nil end
    return (string.gsub(value, '^%s*(.-)%s*$', '%1'))
end

```
