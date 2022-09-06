## Credits:
>### aj - aj-inventory
>### loljoshie - lj-inventory
>### qbcore - qb-inventory
>### Jimathy - Toggle Item

# How to install lj-inventory
* Download source files from github
* Drag source files into your resources folder
* Rename folder from `lj-inventory-main` to `lj-inventory`

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
