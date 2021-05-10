local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Hunter15917/Scripts/main/MainGUI.md"))()
local venyx = library.new("Sparrow", 5013109572)
 

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
local section1 = page:addSection("Training")
local section2 = page:addSection("Auto Buy")
local section3 = page:addSection("Extras")


local LP = game.Players.LocalPlayer
local Char = LP.Character
local ShopBuy = nil
local SkillBuy = nil
local CrownShop = nil
local PickBoss = nil
local PickMob = nil

local LP = game:GetService("Players").LocalPlayer
    for i,v in pairs(LP.Character:GetChildren()) do
        if v.Name == "AntiPortNew" or v.Name == "AntiPort" then
            v:Destroy()
        end
     end    
        
section1:addToggle("Auto Strength", nil, function(r)
if r then
          Toggle1 = true
          else
              Toggle1 = false
      end
          while Toggle1 do
           wait()
pcall(
    function()
if game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool") then
    game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
 end
wait()
game:GetService("ReplicatedStorage").Events.Clicked:FireServer()
end)
end
end)
      
           
           
           
           
section1:addToggle("Auto Sell", nil, function(r)
if r then
          Toggle2 = true
          else
              Toggle2 = false
      end
          while Toggle2 do
           wait()
pcall(
    function()
local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart
HRP.CFrame = CFrame.new(532.141418, 183.687805, 147.428802)
 wait()
game:GetService("ReplicatedStorage").Events.Sell:FireServer()          
end)
          end
end)
   

  
section2:addDropdown("Auto Buy Shop Stuff", {"Saber", "DNA", "Class"}, function(Shop)
  ShopBuy = Shop
end)

section2:addDropdown("Auto Buy Skill Stuff", {"Jump", "Boss Hit"}, function(Skill)
  SkillBuy = Skill
end)

section2:addDropdown("Auto Buy Crown Stuff", {"Auras", "Pet Auras"}, function(Crown)
  CrownShop = Crown
end)


section2:addToggle("Auto Buy (Buy everything)", nil, function(r)
if r then
          Toggle3 = true
          else
              Toggle3 = false
      end
          while Toggle3 do
           wait()    
pcall(
    function()
local args = {
    [1] = "Swords"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
wait()
local args = {
    [1] = "Backpacks"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
wait()
local args = {
    [1] = "JumpBoosts"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
wait()
local args = {
    [1] = "BossBoosts"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
wait()
local args = {
    [1] = "Auras"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
wait()
local args = {
    [1] = "PetAuras"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
end)
end
end)





section2:addToggle("Auto Buy (Shop)", nil, function(r)
if r then
          Toggle4 = true
          else
              Toggle4 = false
      end
          while Toggle4 do
           wait()           
pcall(
    function()
if ShopBuy == "Saber" then
wait(1)
local args = {
    [1] = "Swords"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))

elseif ShopBuy == "DNA" then
wait(1)
local args = {
    [1] = "Backpacks"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))

elseif ShopBuy == "Class" then
print("NOT FINISHED")
end
end)
end
end)


section2:addToggle("Auto Buy (Skill Shop)", nil, function(r)
if r then
          Toggle5 = true
          else
              Toggle5 = false
      end
          while Toggle5 do
           wait(1)           
pcall(
    function()
if SkillBuy == "Jump" then
local args = {
    [1] = "JumpBoosts"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
elseif SkillBuy == "Boss Hit" then
local args = {
    [1] = "BossBoosts"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
end
end)
end
end)




section2:addToggle("Auto Buy (Crown Shop)", nil, function(r)
if r then
          Toggle6 = true
          else
              Toggle6 = false
      end
          while Toggle6 do
           wait(1)        
pcall(
    function()
if CrownShop == "Auras" then
local args = {
    [1] = "Auras"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))

elseif CrownShop == "Pet Auras" then
    
local args = {
    [1] = "PetAuras"
}

game:GetService("ReplicatedStorage").Events.BuyAll:FireServer(unpack(args))
end
end)
end
end)
    
    



section3:addToggle("Collect Islands", nil, function(r)
if r then
          Toggle7 = true
          else
              Toggle7 = false
      end
          while Toggl7  do
           wait()   
pcall(
    function()
local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart

HRP.CFrame = CFrame.new(513.954651, 798.303345, 167.93161)
wait(3.5)
HRP.CFrame = CFrame.new(483.276123, 2651.73389, -302.033752)
wait(3.5)
HRP.CFrame = CFrame.new(656.159119, 7090.82422, -293.15625)
wait(3.5)
HRP.CFrame = CFrame.new(584.680603, 12697.998, -232.666412)
wait(3.5)
HRP.CFrame = CFrame.new(506.208557, 19438.6797, -76.0912094)
wait(3.5)
HRP.CFrame = CFrame.new(476.973358, 26256.7263, -197.769379)
wait(3.5)
HRP.CFrame = CFrame.new(632.277832, 29799.8867, -84.1698303)
wait(3.5)
HRP.CFrame = CFrame.new(519.992554, 34169.4141, -212.145584)
wait(3.5)
HRP.CFrame = CFrame.new(568.779663, 38094.0391, -129.08991)
wait(3.5)
HRP.CFrame = CFrame.new(569.948596, 42887.7344, -192.901947)
wait(3.5)
HRP.CFrame = CFrame.new(631.483704, 48848.4961, -300.894867)
wait(3.5)
HRP.CFrame = CFrame.new(540.004822, 52642.5, -157.713303)
wait(3.5)
HRP.CFrame = CFrame.new(539.372131, 57626.3945, -157.113037)
wait(3.5)
HRP.CFrame = CFrame.new(539.955872, 62382.3945, -156.356842)
wait(3.5)
HRP.CFrame = CFrame.new(543.352661, 67086.9844, -66.5517578)
wait(3.5)
HRP.CFrame = CFrame.new(539.677673, 72951.0391, -157.457123)
wait(3.5)
HRP.CFrame = CFrame.new(608.518311, 76590.0391, -35.6972656)
wait(3.5)
HRP.CFrame = CFrame.new(472.137817, 80723.7422, -23.8265915)
wait(3.5)
HRP.CFrame = CFrame.new(470.21994, 84821.7969, -23.3687286)
wait(3.5)
HRP.CFrame = CFrame.new(471.804474, 90389.1641, -23.9025383)
wait(3.5)
HRP.CFrame = CFrame.new(469.870758, 94252.0781, -22.8204479)
wait(3.5)
HRP.CFrame = CFrame.new(470.874298, 97711.5, -22.9485168)
wait(2.5)
HRP.CFrame = CFrame.new(470.33847, 101248.5, -22.787384)
wait(3.5)
HRP.CFrame = CFrame.new(556.069153, 104246.82, -141.799332)
wait(3.5)
HRP.CFrame = CFrame.new(689.237122, 108786.203, -3.19855666)
wait(3.5)
HRP.CFrame = CFrame.new(688.624695, 113361.625, -3.29329658)                         
wait(3.5)			
HRP.CFrame = CFrame.new(688.618958, 117958.602, -3.68112302)
wait(3.5)
HRP.CFrame = CFrame.new(688.923584, 121863.602, -3.09160757)
wait(3.5)
HRP.CFrame = CFrame.new(690.270874, 127920.102, -2.238792242)
wait(3.5)
HRP.CFrame = CFrame.new(633.859436, 131087.219, -52.4764252)
wait(3.5)
HRP.CFrame = CFrame.new(554.475342, 135606.938, -141.328171)
wait(3.5)
HRP.CFrame = CFrame.new(688.398217, 140146.219, -2.98687148)
wait(3.5)
HRP.CFrame = CFrame.new(688.77771, 143497.359, -3.08410716)
wait(3.5)
HRP.CFrame = CFrame.new(582.669922, 146932, -197.54129)
wait(3.5)
HRP.CFrame = CFrame.new(582.670166,146932, -197.541519)
wait(3.5)
HRP.CFrame = CFrame.new(583.500854, 150268.297, -200.225616)
wait(3.5)
HRP.CFrame = CFrame.new(368.45993, 152666.891, 21.7177887)
wait(3.5)
HRP.CFrame = CFrame.new(631.435852, 158319.578, -303.138153)
wait(3.5)
HRP.CFrame = CFrame.new(539.977661, 162113.609, -154.714294)
wait(3.5)
HRP.CFrame = CFrame.new(539.863098, 164289.547, -155.60466)
wait(3.5)
HRP.CFrame = CFrame.new(539.939026, 166415.563, -155.454407)
wait(3.5)
HRP.CFrame = CFrame.new(539.204895, 171578.891, -97.9063187)
wait(3.5)
HRP.CFrame = CFrame.new(364.851776, 175488.234, -247.135269)
wait(3.5)
HRP.CFrame = CFrame.new(556.690552, 179362.188, -290.851868)
wait(3.5)
HRP.CFrame = CFrame.new(505.59079, 182101.391, -215.772568)
wait(3.5)
HRP.CFrame = CFrame.new(488.132599, 184961.375, -248.158936)
wait(3.5)
HRP.CFrame = CFrame.new(482.710114, 187551.391, -237.773422)
wait(3.5)
HRP.CFrame = CFrame.new(641.150696, 190398.656, -115.813164)
wait(3.5)
HRP.CFrame = CFrame.new(539.776245, 192606.234, -156.834778)
wait(3.5)
HRP.CFrame = CFrame.new(539.155356, 195963.781, -156.578186)
wait(3.5)
HRP.CFrame = CFrame.new(539.778137, 199263.406, -156.751730)
wait(3.5)
HRP.CFrame = CFrame.new(539.633362, 202505.203, -156.630249)
wait(3.5)
HRP.CFrame = CFrame.new(632.117065, 206037.234, -299.96579)
wait(3.5)
HRP.CFrame = CFrame.new(631.519592, 209507.516, -301.182556)
wait(3.5)
HRP.CFrame = CFrame.new(631.731506, 213007.702, -295.925842)
wait(3.5)
HRP.CFrame = CFrame.new(630.770325, 216609.719, -299.943298)
wait(3.5)
HRP.CFrame = CFrame.new(631.015747, 220080.859, -299.398254)
wait(3.5)
HRP.CFrame = CFrame.new(630.378357, 223508.469, -300.144958)
wait(3.5)
HRP.CFrame = CFrame.new(631.652588, 226952.984, -298.53952)
wait(3.5)
HRP.CFrame = CFrame.new(630.93512, 230472.594, -297.687805)
wait(3.5)
HRP.CFrame = CFrame.new(631.730164, 233948.672, -296.615784)
wait(3.5)
HRP.CFrame = CFrame.new(631.128906, 237502.547, -297.650787)
wait(3.5)
HRP.CFrame = CFrame.new(631.106506,241062.516, -299.004089)
wait(3.5)
HRP.CFrame = CFrame.new(631.602722, 244540.922, -300.526428)
wait(3.5)
HRP.CFrame = CFrame.new(631.21814, 248003.813, -299.643768)
wait(3.5)
HRP.CFrame = CFrame.new(631.523804, 251556.234, -300.910187)
wait(3.5)
HRP.CFrame = CFrame.new(631.059814, 255099.016, -299.370544)
wait(3.5)
HRP.CFrame = CFrame.new(630.875977, 258652.313, -295.641296)
wait(3.5)
HRP.CFrame = CFrame.new(630.876404, 262198.875, -303.96405)  
wait(3.5)   
 HRP.CFrame = CFrame.new(630.986877, 265715.344, -302.151611)          
 wait(3.5)  
HRP.CFrame = CFrame.new(631.128967, 269270.688, -300.371887)   
wait(3.5)
HRP.CFrame = CFrame.new(631.000244, 272961.688, -300.79184)
wait(3.5)
HRP.CFrame = CFrame.new(631.498169, 276486.594, -299.965759)
wait(3.5)
HRP.CFrame = CFrame.new(631.152954, 279947.306, -299.938019)
wait(3.5)
HRP.CFrame = CFrame.new(631.203552, 283381, -300.098083)   
 wait(3.5) 
HRP.CFrame = CFrame.new(630.960022, 286886.469, -303.541816)   
wait(3.5)  
HRP.CFrame = CFrame.new(631.211181, 290427.469, -301.887421)
wait(3.5)
HRP.CFrame = CFrame.new(631.209717, 293910.469, -301.917938)
wait(3.5)
HRP.CFrame = CFrame.new(631.068726, 297356.218, -302.331024)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 300852.25, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 304279.75, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 307728.438, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 311222.656, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 314668.469, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 318112.719, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 321673.688, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 325145.844, -299.907471)
wait(3.5)
HRP.CFrame = CFrame.new(631.154175, 328593.844, -299.907471)
end)
end
end)


section3:addToggle("Crown", nil, function(r)
if r then
          Toggle8 = true
          else
              Toggle8 = false
      end
          while Toggle8 do
           wait()   
pcall(
    function()
local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart
HRP.CFrame = CFrame.new(791.691162, 249.928604, 38.2487793)
end)
 end
end)

section3:addToggle("Flags (Deactivate after activating to not loop)", nil, function(r)
if r then
          Toggle9 = true
          else
              Toggle9 = false
      end
          while Toggle9 do
           wait()   
pcall(
    function()
local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart
HRP.CFrame = CFrame.new(630.022, 259.91, 142.856)
wait(26)
HRP.CFrame = CFrame.new(-32.5713, 253.66, 71.691)
wait(26)
HRP.CFrame = CFrame.new(430.894, 279.88, -258.473)
wait(26)
HRP.CFrame = CFrame.new(706.172, 210.12, 467.019)
wait(26)
HRP.CFrame = CFrame.new(618.601, 475.087, -106.264)
wait(26)
HRP.CFrame = CFrame.new(698.198, 1143.24, -214.447)
wait(26)
HRP.CFrame = CFrame.new(596.459, 1445.31, 65.7102)
wait(26)
HRP.CFrame = CFrame.new(247.547, 2160.23, -68.32)
wait(26)
HRP.CFrame = CFrame.new(588.348, 3180.76, -15.644)
wait(26)
end)
end
end)





local page = venyx:addPage("Mobs", 5012544693)
local section1 = page:addSection("Bosses")
local section2 = page:addSection("Mobs")


section1:addDropdown("Pick Boss", {"Boss", "Fire Boss", "Earth Boss", "Water Boss", "Plasma Boss"}, function(Boss)
  PickBoss = Boss
end)
 


section1:addToggle("Boss", nil, function(r)
if r then
          Toggle10 = true
          else
              Toggle10 = false
      end
          while Toggle10 do
             wait(0.1)
pcall(
    function()
local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart
  if game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool") then
    game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
end
wait(0.1)
game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").RemoteClick:FireServer()
wait()
if PickBoss == "Boss" then
HRP.CFrame = workspace.Boss.RightLowerLeg.CFrame
elseif PickBoss == "Fire Boss" then
HRP.CFrame = game:GetService("Workspace").Mobs["Fire Boss"].RightLowerLeg.CFrame
elseif PickBoss == "Earth Boss" then
HRP.CFrame = game:GetService("Workspace").Mobs["Earth Boss"].RightLowerLeg.CFrame
elseif PickBoss == "Water Boss" then
HRP.CFrame = game:GetService("Workspace").Mobs["Water Boss"].RightLowerLeg.CFrame
elseif PickBoss == "Plasma Boss" then
HRP.CFrame = game:GetService("Workspace").Mobs["Plasma Boss"].RightLowerLeg.CFrame
        end 
    end)
end
end)



section2:addDropdown("Mobs", {"Fire Golem", "Earth Golem", "Water Golem", "Plasma Golem"}, function(Mob)
  PickMob = Mob
end)


section2:addToggle("Pick Mobs", nil, function(r)
if r then
          Toggle11 = true
          else
              Toggle11 = false
      end
          while Toggle11 do
             wait(0.1)
pcall(
    function()
 local HRP = game.Players.LocalPlayer.Character.HumanoidRootPart
  if game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool") then
    game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
end
wait(0.1)
game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").RemoteClick:FireServer()
wait()
if PickBoss == "Fire Golem" then
HRP.CFrame = game:GetService("Workspace").Mobs["Fire Golem"].RightLowerLeg.CFrame
elseif PickBoss == "Earth Golem" then
HRP.CFrame = game:GetService("Workspace").Mobs["Earth Golem"].RightLowerLeg.CFrame
elseif PickBoss == "Water Golem" then
HRP.CFrame = game:GetService("Workspace").Mobs["Water Golem"].RightLowerLeg.CFrame
elseif PickBoss == "Plasma Golem" then
HRP.CFrame = game:GetService("Workspace").Mobs["Plasma Golem"].RightLowerLeg.CFrame
        end 
    end)
end
end)




local page = venyx:addPage("Settings", 5012544693)
local section1 = page:addSection("Settings")


section1:addKeybind("Minimize Key", Enum.KeyCode.Minus, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end)



section1:addButton("Anti Afk", function()
local VirtualUser = game:service'VirtualUser'
game:service('Players').LocalPlayer.Idled:connect(function()
VirtualUser:CaptureController()
VirtualUser:ClickButton2(Vector2.new())
end)
end)

section1:addButton("No clip (Press E to Deactivate)", function(r)
 if r then 
            noclip = true
            pcall(
                function()
game:GetService('RunService').Stepped:connect(function()
if noclip then
Char.Humanoid:ChangeState(11)
end
end)
plr = LP
mouse = plr:GetMouse()
mouse.KeyDown:connect(function(key)
 
if key == "e" then
noclip = not noclip
Char.Humanoid:ChangeState(11)
end
end)
end)
end
end)
