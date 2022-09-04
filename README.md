# ADDED EXAMPLE OF ITEMS.LUA
>### qb-core/shared/items.lua
>### If you are lazy to put. You can use mine replace your items.lua with the one i provided and just modify the ["decay"] = 1.0 = 1 day

# Inventory Decay

![image](https://user-images.githubusercontent.com/80186604/163069477-114e14ec-bec1-4f93-8421-42017c605f15.png)

## Credits:
>### aj - aj-inventory
>### loljoshie - lj-inventory
>### qbcore - qb-inventory
>### Jimathy - Toggle Item
>### Jay - For introducing decay system

# How to install lj-inventory
* Download source files from github
* Drag source files into your resources folder
* Rename folder from `lj-inventory-main` to `lj-inventory`

# TO DO
you need to add a decay and created value in your qb-core/shared/items for all items, the decay is set to be the days the item lasts

```lua
["created"] = nil
["decay"] = 28.0 -- for 28 days
```

### REPLACE ADDITEM EVENT
```lua
TriggerServerEvent("QBCore:Server:AddItem, item, 1)
```

### TO
```lua
exports['qb-inventory']:toggleItem(1, itemName, 1)
```

### REPLACE REMOVEITEM EVENT
```lua
TriggerServerEvent("QBCore:Server:RemoveItem, item, 1)
```

### TO
```lua
exports['qb-inventory']:toggleItem(0, itemName, 1)
```


### REPLACE HASITEM CALLBACK
```lua
QBCore.Functions.TriggerCallback('QBCore:HasItem', function(result)
        if hasitem then
              -- Has Item
        end
end, "sandwich")
```

### TO
```lua
      if QBCore.Functions.HasItem("sandwich") then
             -- Has Item
      end
```
