# Bleklib UI (xsx lib)
This documentation is for Bleklib UI Credit To The Owner

## Booting the Bleklib UI Library
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Consistt/Ui/main/UnLeaked"))()
```




## Creating a Bleklib UI Window / Library
```lua
library.title = "Riley Hub"

library:Introduction()
wait(1)
local Init = library:Init()
    }
})
```

## Creating a Notify
```lua
local Notif = library:InitNotifications()

for i = 20,0,-1 do 
    task.wait(0.05)
    local LoadingXSX = Notif:Notify("Riley Hub ", 3, "information") -- notification, alert, error, success, information
end 
```

## Creating a Tab
```lua
local Tab1 = Init:NewTab("Example tab")
```

## Creating a Section
```lua
local Section1 = Tab1:NewSection("Example Components")
```

## Creating a Rank
```lua
library.rank = "Dev"
local Wm = library:Watermark("riley hub" .. library.version ..  " | " .. library:GetUsername() .. " | rank: " .. library.rank)
local FpsWm = Wm:AddWatermark("fps: " .. library.fps)
coroutine.wrap(function()
    while wait(.75) do
        FpsWm:Text("fps: " .. library.fps)
    end
end)()
```

## Creating a Label
```lua
local Label1 = Tab1:NewLabel("Example label", "left")--"left", "center", "right"
```

## Creating a Toggle With Keybind
```lua
local Toggle1 = Tab1:NewToggle("Example toggle", false, function(value)
    local vers = value and "on" or "off"
    print("one " .. vers)
end):AddKeybind(Enum.KeyCode.RightControl)
```

## Creating a Button
```lua
local Button1 = Tab1:NewButton("Button", function()
    print("one")
end)
```

## Creating a keybind
```lua
local Keybind1 = Tab1:NewKeybind("Keybind 1", Enum.KeyCode.RightAlt, function(key)
    Init:UpdateKeybind(Enum.KeyCode[key])
end)
```

## Creating a Toggling UI with Keybinds
```lua
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)
```

## Creating Small Textbox
```lua
local Textbox1 = Tab1:NewTextbox("Text box 1 [auto scales // small]", "", "1", "all", "small", true, false, function(val)
    print(val)
end)
```

## Creating Medium Textbox
```lua
local Textbox2 = Tab1:NewTextbox("Text box 2 [medium]", "", "2", "all", "medium", true, false, function(val)
    print(val)
end)
```

## Creating Large Textbox
```lua
local Textbox3 = Tab1:NewTextbox("Text box 3 [large]", "", "3", "all", "large", true, false, function(val)
    print(val)
end)
```

## Creating a Selector
```lua
local Selector1 = Tab1:NewSelector("Selector 1", "bungie", {"fg", "fge", "fg", "fg"}, function(d)
    print(d)
end):AddOption("fge")
```

## Creating a Slider
```lua
local Slider1 = Tab1:NewSlider("Slider 1", "", true, "/", {min = 1, max = 100, default = 20}, function(value)
    print(value)
end)
```

## Creating the Finish Loading
```lua
local FinishedLoading = Notif:Notify("Loaded Riley Hub", 4, "Success")
```
