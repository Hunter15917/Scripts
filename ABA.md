local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Hunter15917/Scripts/main/MainGUI.md"))()
local venyx = library.new("Sparrow", 5013109572)
 
-- themes
       local themes = {
       Background = Color3.fromRGB(0, 0, 0),
        Glow = Color3.fromRGB(159, 0, 255),
        Accent = Color3.fromRGB(47, 11, 227),
        LightContrast = Color3.fromRGB(17, 17, 223),
        DarkContrast = Color3.fromRGB(12, 12, 12),  
        TextColor = Color3.fromRGB(255, 255, 255)
}
 
-- first page
local page = venyx:addPage("Farm Stuff", 5012544693)
local section1 = page:addSection("Auto Farm")

local LP = game.Players.LocalPlayer
local Char = LP.Character

section1:addToggle("Auto farm", nil, function(r)
if r then
          Toggle1 = true
          else
              Toggle1 = false
      end
          while Toggle1 do
           wait()
local args = {
    [1] = "Naruto"
}

game:GetService("Players").LocalPlayer.Backpack.ServerTraits.Choose:FireServer(unpack(args))
wait()
local args = {
    [1] = "PLAY"
}

game:GetService("Players").LocalPlayer.Backpack.ServerTraits.Choose:FireServer(unpack(args))
local args = {
    [1] = "m1",
    [2] = {
        ["air"] = false,
        ["mousehit"] = CFrame.new(Vector3.new(326.79678344727, 33.919578552246, -72.842926025391), Vector3.new(-0.15582385659218, 0.13428877294064, 0.97861403226852))
    }
}

game:GetService("Players").LocalPlayer.Backpack.ServerTraits.Input:FireServer(unpack(args))
end
end)




section1:addButton("Anti Afk (not pressing buttons)", function(r)
 if r then
pcall(
    function()
while wait(0.1) do
print("Anti AFK Activated")
local VirtualUser=game:service'VirtualUser'
game:service('Players').LocalPlayer.Idled:connect(function()
VirtualUser:CaptureController()
VirtualUser:ClickButton2(Vector2.new())
wait()
local args = {
    [1] = game:GetService("Players").LocalPlayer.PlayerGui.afker.Frame.YES.LocalScript
}

game:GetService("ReplicatedStorage").afk:FireServer(unpack(args))
end)
end

    
 local page = venyx:addPage("Settings", 5012544693)
local section2 = page:addSection("Settings")
section2:addKeybind("Minimize Key", Enum.KeyCode.Minus, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end)  

