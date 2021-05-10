
-- Instances:
local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Topbar = Instance.new("Frame")
local Line = Instance.new("Frame")
local Execute = Instance.new("TextButton")
local KEY = Instance.new("TextBox")

-- Properties:
ScreenGui.Parent = game.CoreGui

MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.Active = true
MainFrame.BackgroundColor3 = Color3.new(0.176471, 0.176471, 0.176471)
MainFrame.BorderSizePixel = 0
MainFrame.Position = UDim2.new(0.29734084, 0, 0.391891897, 0)
MainFrame.Selectable = true
MainFrame.Size = UDim2.new(0, 502, 0, 175)
MainFrame.Draggable = true

Topbar.Name = "Topbar"
Topbar.Parent = MainFrame
Topbar.Active = true
Topbar.BackgroundColor3 = Color3.new(0.137255, 0.137255, 0.137255)
Topbar.BorderSizePixel = 0
Topbar.Selectable = true
Topbar.Size = UDim2.new(0, 502, 0, 15)

Line.Name = "Line"
Line.Parent = Topbar
Line.Active = true
Line.BackgroundColor3 = Color3.new(1, 0, 0.490196)
Line.BorderSizePixel = 0
Line.Position = UDim2.new(0, 0, 1, 0)
Line.Selectable = true
Line.Size = UDim2.new(0, 502, 0, 6)

Execute.Name = "Execute"
Execute.Parent = MainFrame
Execute.BackgroundColor3 = Color3.new(0.137255, 0.137255, 0.137255)
Execute.BorderSizePixel = 0
Execute.Position = UDim2.new(0.300796807, 0, 0.633714259, 0)
Execute.Size = UDim2.new(0, 200, 0, 50)
Execute.Font = Enum.Font.SciFi
Execute.Text = "EXECUTE"
Execute.TextColor3 = Color3.new(1, 1, 1)
Execute.TextSize = 35
Execute.TextWrapped = true

KEY.Name = "KEY"
KEY.Parent = MainFrame
KEY.BackgroundColor3 = Color3.new(0.137255, 0.137255, 0.137255)
KEY.BorderSizePixel = 0
KEY.Position = UDim2.new(0.165338635, 0, 0.257142842, 0)
KEY.Size = UDim2.new(0, 336, 0, 50)
KEY.Font = Enum.Font.SciFi
KEY.Text = "INPUT KEY HERE..."
KEY.TextColor3 = Color3.new(1, 1, 1)
KEY.TextSize = 24
KEY.TextWrapped = true
local LP = game.Players.LocalPlayer




-- whitelist keys
local whitelist1 = ("FHGfNfgBMXP6A83dbFuW")
local whitelist2 = ("cMDWk7CRYmXFYyRkySmN")
local whitelist3 = ("7zBqdTUAtM4z4x5PQQDT")





Execute.MouseButton1Down:connect(function()
if KEY.Text ~= whitelist1 then
return end
    if KEY.Text == whitelist1 and LP.Name == "130Ping" and LP.UserId == 2005974613 then
		MainFrame:Destroy()
		wait(1)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Hunter15917/Scripts/main/AllScripts.md"))()

elseif KEY.Text == whitelist1 and LP.Name ~= "130Ping" or LP.UserId ~= 2005974613 then

local Data = {
    ["content"] = tostring(whitelist1)
}

local response = syn.request(
    {
        Url = "https://discord.com/api/webhooks/840715845202214943/Tlzx1rx-hqI3iWFgLh3VTiZrxy-cPG5Uy9Syvs6PK83OSCDsq2DS2OdurNlOpUpm-m3c",
        Method = "POST",
        Headers = { ["Content-Type"] = "application/json" },
        Body = game:GetService("HttpService"):JSONEncode(Data)
    }
)
wait(0.5)
MainFrame:Destroy()
	wait()
	game.Players.LocalPlayer:Kick("why")
      end
end)




Execute.MouseButton1Down:connect(function()
  if KEY.Text ~= whitelist2 then
return end 
    if KEY.Text == whitelist2 and LP.Name == "Eadwulf" and LP.UserId == 879757642 then
		MainFrame:Destroy()
		wait(1)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Hunter15917/Scripts/main/AllScripts.md"))()

elseif KEY.Text == whitelist2 and LP.Name ~= "Eadwulf" or LP.UserId ~= 879757642 then

local Data = {
    ["content"] = tostring(whitelist2)
}

local response = syn.request(
    {
        Url = "https://discord.com/api/webhooks/840715845202214943/Tlzx1rx-hqI3iWFgLh3VTiZrxy-cPG5Uy9Syvs6PK83OSCDsq2DS2OdurNlOpUpm-m3c",
        Method = "POST",
        Headers = { ["Content-Type"] = "application/json" },
        Body = game:GetService("HttpService"):JSONEncode(Data)
    }
)
wait(0.5)
MainFrame:Destroy()
	wait()
	game.Players.LocalPlayer:Kick("why")
     end
end)







-- blacklist keys
local blacklist1 = ("HHGfNfgBMXP6A83dbFuW")
local blacklist2 = ("MMDWk7CRYmXFYyRkySmN")
local blacklist3 = ("ZZBqdTUAtM4z4x5PQQDT")

Execute.MouseButton1Down:connect(function()
	if KEY.Text == blacklist1 then
		MainFrame:Destroy()
		wait(1)
		game.Players.LocalPlayer:Kick("Blacklisted")
	end
end)

Execute.MouseButton1Down:connect(function()
	if KEY.Text == blacklist2 then
		MainFrame:Destroy()
		wait(1)
		game.Players.LocalPlayer:Kick("Blacklisted")
	end
end)

Execute.MouseButton1Down:connect(function()
	if KEY.Text == blacklist3 then
		MainFrame:Destroy()
		wait(1)
		game.Players.LocalPlayer:Kick("Blacklisted")
	end
end)
