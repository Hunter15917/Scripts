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
local section1 = page:addSection("Important Stuff")
local section2 = page:addSection("Stat Farm")
local section3 = page:addSection("Money Farm")

local LP = game.Players.LocalPlayer
local Char = LP.Character




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
 

 
section1:addToggle("Hide Identity", nil, function(r)
if r then
          Toggle1 = true
          else
              Toggle1 = false
      end
          while Toggle1 do
           wait()
           pcall(
               function()
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Shirt" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Pants" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Head" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Belt" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Glove" then
v:Destroy()
end
end
end)
end
end)
    


section1:addButton("Anti Admin", function(r)
  if r then   
while wait() do
pcall(
                  function()    
local LP = game:GetService("Players").LocalPlayer
local admins = {
    "OverlordBetty",
    "AnnaStormss",
    "DamageP1ayz",
    "Zetzume",
    "Iuvmin",
    "YpcNate",
    "Reizum",
    "Mealikz",
    "Gunterf"
    
}
while wait() do
    for i,x in pairs(game:GetService("Players"):GetPlayers()) do
        for i,v in pairs(admins) do
            if v == x.Name then
                LP:Kick("An admin is in your game")
            end
        end
    end
end    
end)
end 
end
end)



section2:addToggle("Punching Bag ", nil, function(r)
    if r then
          Toggle10 = true
          else
              Toggle10 = false
      end
          while Toggle10 do
           wait()
           pcall(
               function()
           local name
                for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetChildren()) do
                   if v.Name == "DeleteMe" or v.Name == "Knocked" or v.Name == "Ragdoll" then
                         v:Destroy()
                    end
                end
                wait()
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, game:GetService("Workspace").PunchMe.HumanoidRootPart.Position + Vector3.new(0,-6,0), 300)
wait()
if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") then
    game.Players.LocalPlayer.Backpack:FindFirstChild("Combat").Parent = game.Players.LocalPlayer.Character
end 
wait()               
game.Players.LocalPlayer.Character.Combat:Activate()
end)
end
end)
                   



     
section2:addToggle("Dummies", nil, function(r)
    if r then
          Toggle12 = true
          else
              Toggle12 = false
      end
          while Toggle12 do
              wait()
              pcall(
                  function()
           local name
                for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetChildren()) do
                   if v.Name == "DeleteMe" or v.Name == "Knocked" or v.Name == "Ragdoll" then
                         v:Destroy()
                    end
                end
                wait()
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, game:GetService("Workspace").DuraBag.HumanoidRootPart.Position + Vector3.new(0,-5,0), 300)
wait()
if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") then
    game.Players.LocalPlayer.Backpack:FindFirstChild("Combat").Parent = game.Players.LocalPlayer.Character
end 
wait()               
game.Players.LocalPlayer.Character.Combat:Activate()
end)
end
end)

section2:addToggle("Auto Train Stamina", nil, function(r)
    if r then
          Toggle4 = true
          else
              Toggle4 = false
      end
          while Toggle4 do
              wait()
           pcall(
           function()
if LP.Backpack:FindFirstChild("Combat") then
   LP.Backpack:FindFirstChild("Combat").Parent = game.Players.LocalPlayer.Character
end 
wait()
if LP.Character.Stamina.Value >= 11 then
wait()                 
LP.Character.Combat:Activate()
end
end)
end
end) 
      
 
 
 
 
section2:addToggle("Auto Pushups", nil, function(r)
    if r then
          Toggle5 = true
          else
              Toggle5 = false
      end
          while Toggle5 do
           wait()
           pcall(
               function()
if LP.Backpack:FindFirstChild("Pushup") then
    game.Players.LocalPlayer.Backpack:FindFirstChild("Pushup").Parent = game.Players.LocalPlayer.Character
end   
wait(3)
if LP.Character.Stamina.Value >= 100 then
game.Players.LocalPlayer.Character.Pushup:Activate()  
wait()
elseif LP.Character.Stamina.Value <= 25 then
    return
end
end)
end
end) 
    
  
section2:addToggle("Auto Situps", nil, function(r)
    if r then
          Toggle6 = true
          else
              Toggle6 = false
      end
          while Toggle6 do
           wait()
           pcall(
               function()
if LP.Backpack:FindFirstChild("Situp") then
    game.Players.LocalPlayer.Backpack:FindFirstChild("Situp").Parent = game.Players.LocalPlayer.Character
end       
wait(2.5)
if LP.LocalPlayer.Character.Stamina.Value >= 100 then
game.Players.LocalPlayer.Character.Situp:Activate()  
wait()
elseif LP.Character.Stamina.Value <= 25 then
    return
end
end)
end
end) 
 
  
section2:addToggle("Auto Squats", nil, function(r)
    if r then
          Toggle7 = true
          else
              Toggle7 = false
      end
          while Toggle7 do
           wait()
           pcall(
            function()   
if LP.Backpack:FindFirstChild("Squat") then
    LP.Backpack:FindFirstChild("Squat").Parent = game.Players.LocalPlayer.Character
end       
wait(3)
if LP.Character.Stamina.Value >= 100 then
game.Players.LocalPlayer.Character.Squat:Activate()  
wait()
elseif LP.Character.Stamina.Value <= 25 then
    return
end
end)
end
end)  

  
section3:addButton("Auto Pizza (Turn on Noclip Idiot)", function(r)  
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Left Arm" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Right Arm" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Left Leg" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Right Leg" then
v:Destroy()
end
end
for i,v in pairs(Char:GetChildren()) do
 if v.Name == "Head" then
v:Destroy()
end
end

while wait(0.1) do
fireclickdetector(game.Workspace.Missions.PizzaDelivery.ClickDetector)    
if not Char:FindFirstChild("Arrow") then
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(-71.1761398, 4, -387.617767), 300)

elseif Char:FindFirstChild("Arrow") then
if Char.Mission.Location.Value == 1 then
print("its 1")
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(-377.63147, 3.49999928, -466.254089), 300) 

elseif Char.Mission.Location.Value == 2 then
print("its 2")
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(305.26532, 3.04999757, -177.3582), 300) 


elseif Char.Mission.Location.Value == 3 then
print("its 3")
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(-62.3808975, 2.99999928, -79.8169479), 300)   


elseif Char.Mission.Location.Value == 4 then
print("its 4")
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(-91.1889114, 3.49999928, -602.918152), 300)        

end
end
end
end)
  
    
local page = venyx:addPage("Extra", 5012544693)
local section1 = page:addSection("Auto Buy Stuff")
local section2 = page:addSection("Settings")

section1:addToggle("Auto Buy", nil, function(r)
    if r then
          Toggle3 = true
          else
              Toggle3 = false
      end
          while Toggle3 do
           wait(300)
           pcall(
               function()
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, game:GetService("Workspace").Buyables["Beatdown Burger"]["Beatdown Burger 32$"].Head.Position, 150)
wait(0.7)
fireclickdetector(game:GetService("Workspace").Buyables["Beatdown Burger"].ClickDetector)
wait(0.4)
local ts = game:GetService("TweenService")
local function Tween(part, endpos, speed)
    if part and endpos then
        local Time = (endpos - part.Position).magnitude/speed
        local Info = TweenInfo.new(Time, Enum.EasingStyle.Linear)
        local Tween = ts:Create(part,Info,{CFrame = CFrame.new(endpos.X,endpos.Y,endpos.Z)})
        Tween:Play()
        wait(Time)
    end
end
Tween(game.Players.LocalPlayer.Character.HumanoidRootPart, Vector3.new(-70.918869, 4, -401.940399), 300)    
end)
end
end)


section1:addToggle("Auto Eat", nil, function(r)
    if r then
          Toggle25 = true
          else
              Toggle25 = false
      end
          while Toggle25 do
           wait()
           pcall(
               function()
if LP.Backpack:FindFirstChild("Beatdown Burger") then
    game.Players.LocalPlayer.Backpack:FindFirstChild("Beatdown Burger").Parent = game.Players.LocalPlayer.Character
end
wait()
LP.Character["Beatdown Burger"]:Activate() 
end)
end
end)

section1:addToggle("Auto Buy Gym Time", nil, function(r)
    if r then
          Toggle13 = true
          else
              Toggle13 = false
      end
          while Toggle13 do
           wait(110)
           pcall(
               function()
game:GetService("ReplicatedStorage").Events.MembershipEvent:FireServer(2)
end)
end
end)










 section2:addButton("No-Stun", function(r)
  if r then   
while wait() do
pcall(
                  function()
                for i,v in pairs(Char:GetChildren()) do
                   if v.Name == "Stun" or v.Name == "CombatStun" then
                         v:Destroy()
                   end
                end
                  end)
end
end
end)


section2:addButton("Reset", function(r)
  if r then 
              pcall(
                  function()     
 if LP.Character then
            LP.Character:Destroy()
 end  
                  end)
                  end
end)    

     
 
   
 section2:addButton("God Mode", function(r)
  if r then 
              pcall(
                  function()   
for i,v in pairs(Char.Humanoid:GetChildren()) do
 if v.Name == "Animator" then
v:Destroy()
end
end
end)
end
end)

 section2:addButton("Inf Stam", function(r)
  if r then 
              pcall(
                  function()    
loadstring(game:HttpGet('http://gameovers.net/Scripts/Free/ProjectBeatdown/InfRun.lua',true))() 
end)
end
end)
    








    
local page = venyx:addPage("Settings", 5012544693)
local section2 = page:addSection("Settings")
section2:addKeybind("Minimize Key", Enum.KeyCode.Minus, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end)

section2:addButton("Anti Afk", function()
local VirtualUser = game:service'VirtualUser'
game:service('Players').LocalPlayer.Idled:connect(function()
VirtualUser:CaptureController()
VirtualUser:ClickButton2(Vector2.new())
end)
end)

