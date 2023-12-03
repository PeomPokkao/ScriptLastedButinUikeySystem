if not game:IsLoaded() then repeat game.Loaded:Wait() until game:IsLoaded() end


local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
wait(1)
vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)


if game.PlaceId == 2753915549 then
        W = true
    elseif game.PlaceId == 4442272183 then
        W2 = true
    elseif game.PlaceId == 7449423635 then
        W3 = true
    end




game.StarterGui:SetCore("SendNotification", {
      Icon = "rbxassetid://11915607895"; -- ใส่หน้าพ่อมึงมึง
      Title = "Upper Cut Hub", 
      Text = "loading",
  })

  _G.Team = "Pirate"


if game:GetService("Players").LocalPlayer.PlayerGui.Main:FindFirstChild("ChooseTeam") then
	repeat wait()
		if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
			if _G.Team == "Pirate" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			elseif _G.Team == "Marine" then
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			else
				for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
					v.Function()
				end
			end
		end
	until game.Players.LocalPlayer.Team ~= nil and game:IsLoaded()
end

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Patskorn/GUI/main/Copy-SynapOver.lua"))()

function TP2(P1)
    local Dis = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local Speed
    if Dis < 1000 then
        Speed = 300
    elseif Dis >= 100 then
        Speed = 200
    end
    local tween = game:GetService("TweenService"):Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart,TweenInfo.new(Dis/Speed,Enum.EasingStyle.Linear),{CFrame = P1})
    tween:Play()
	_G.PartNeon = true
end

spawn(function()
    pcall(function()
       game:GetService("RunService").Heartbeat:Connect(function()
        if _G.PartNeon then
          if not game:GetService("Workspace"):FindFirstChild("LOL") then
             local Paertaiteen = Instance.new("Part")
             Paertaiteen.Name = "LOL"
             Paertaiteen.Parent = game.Workspace
             Paertaiteen.Anchored = true
             Paertaiteen.Transparency = 0
             Paertaiteen.Size = Vector3.new(30,0.5,30)
             Paertaiteen.Material = "Neon"
             while true do 
 
                 wait(0.1) 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 155, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 255, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 255, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 255, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 155, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 155)}):Play() 
                 wait(.5)
             end 
         elseif game:GetService("Workspace"):FindFirstChild("LOL") then
             game.Workspace["LOL"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
         end
     else
     if game:GetService("Workspace"):FindFirstChild("LOL") then
             game:GetService("Workspace"):FindFirstChild("LOL"):Destroy()
         end
        end
    end)
 end)
end)

local GUI = library:new("Ents-Hub "," Premium-Scripts ]")
local Tab1 = GUI:Tap("Main")
local Tab2 = GUI:Tap("Additional-functions")
local Tab3 = GUI:Tap("Teleport")

Tab1:Line()

local X2Code = {
    "TheGreatAce",        
    "Bignews",      
    "Fudd10",
    "Axiore",
    "TantaiGaming",
    "StrawHatMaine",
    "Sub20fficialNoobie",
    "Sub2NoobMaster123",
    "Sub2Daigrock",
    "SUB2GAMERROBOT_EXP1",
    "UPD16",
    "3BVISITS",
    "fudd10_v2",
    "Bluxxy",
    "JCWK",
    "Sub2Fer999",
    "Enyu_is_Pro",
    "Magicbus",
    "Starcodeheo"
}

Tab1:Button("RedeemAllCodex2",function(value)
    function RedeemCode(value)
        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(value)
    end
    for i,v in pairs(x2Code) do
        RedeemCode(v)
    end
end)

Tab1:Line()

Tab1:Toggle("AuToFarm",function(value)
    end)


----------------------------------------------------------------

Tab1:Toggle("Fast Attack",function(value)
_G.UesFast = value

local plr = game.Players.LocalPlayer
    
local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]

function GetCurrentBlade() 
    local p13 = CbFw2.activeController
    local ret = p13.blades[1]
    if not ret then return end
    while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
    return ret
end
function AttackNoCD() 
    local AC = CbFw2.activeController
    for i = 1, 1 do 
        local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
            plr.Character,
            {plr.Character.HumanoidRootPart},
            60
        )
        local cac = {}
        local hash = {}
        for k, v in pairs(bladehit) do
            if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
                table.insert(cac, v.Parent.HumanoidRootPart)
                hash[v.Parent] = true
            end
        end
        bladehit = cac
        if #bladehit > 0 then
            local u8 = debug.getupvalue(AC.attack, 5)
            local u9 = debug.getupvalue(AC.attack, 6)
            local u7 = debug.getupvalue(AC.attack, 4)
            local u10 = debug.getupvalue(AC.attack, 7)
            local u12 = (u8 * 798405 + u7 * 727595) % u9
            local u13 = u7 * 798405
            (function()
                u12 = (u12 * u9 + u13) % 1099511627776
                u8 = math.floor(u12 / u9)
                u7 = u12 - u8 * u9
            end)()
            u10 = u10 + 1
            debug.setupvalue(AC.attack, 5, u8)
            debug.setupvalue(AC.attack, 6, u9)
            debug.setupvalue(AC.attack, 4, u7)
            debug.setupvalue(AC.attack, 7, u10)
            pcall(function()
                for k, v in pairs(AC.animator.anims.basic) do
                    v:Play()
                end                  
            end)
            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
            end
        end
    end
end

require(game.ReplicatedStorage.Util.CameraShaker):Stop()
task.spawn(function()
    while task.wait() do
        pcall(function()
          if _G.UesFast then
              if _G.UesFast then
                AttackNoCD(100)
              end
          end
      end)
    end
end)
                            end)

Tab1:Toggle("Part Neon",function(value)

_G.PartNeon = value
if _G.PartNeon == true then
spawn(function()
    pcall(function()
       game:GetService("RunService").Heartbeat:Connect(function()
        if _G.PartNeon then
          if not game:GetService("Workspace"):FindFirstChild("LOL") then
             local Paertaiteen = Instance.new("Part")
             Paertaiteen.Name = "LOL"
             Paertaiteen.Parent = game.Workspace
             Paertaiteen.Anchored = true
             Paertaiteen.Transparency = 0
             Paertaiteen.Size = Vector3.new(30,0.5,30)
             Paertaiteen.Material = "Neon"
             while true do 
 
                 wait(0.1) 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 155, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 255, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 255, 0)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 255, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(0, 155, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 255)}):Play() 
                 wait(.5)
 
                 game:GetService('TweenService'):Create(
                     Paertaiteen,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                 {Color = Color3.fromRGB(255, 0, 155)}):Play() 
                 wait(.5)
             end 
         elseif game:GetService("Workspace"):FindFirstChild("LOL") then
             game.Workspace["LOL"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
             
         end
     else
         if _G.PartNeon == false then
                 game:GetService("Workspace"):FindFirstChild("LOL")
                 game:GetService("Workspace"):FindFirstChild("LOL"):Destroy()
                 end
        end
        end)
 end)
end)
end
end)

Tab3:Line()

Tab3:Dropdown("Teleport in world 1",{"Pirate Starter Island", "Marine Starter Island", "Middle Town", "Jungle", "Pirate Village", "Desert", "Frozen Village", "Marine Fortress", "Skylands", "Prison", "Colosseum", "Magma Village", "Underwater City", "Upper Skylands", "Fountain City"},function(t)
    _G.Teleport = t
end)

Tab3:Button("Tween",function(value)
    pcall(function()
        if _G.Teleport == "Pirate Starter Island" then
            TP2(CFrame.new(1072.9288330078125, 16.542423248291016, 1354.3056640625))
        elseif _G.Teleport == "Marine Starter Island" then
             TP2(CFrame.new(-2531.5439453125, 6.881457328796387, 2041.8248291015625))
         elseif _G.Teleport == "Middle Town" then
             TP2(CFrame.new(-654.193603515625, 7.877630233764648, 1423.10009765625))
         elseif
             _G.Teleport == "Jungle" then
            TP2(CFrame.new(-1414.7398681640625, 32.877777099609375, 9.830777168273926)) 
             elseif
              _G.Teleport == "Pirate Village" then
            TP2(CFrame.new(-1250.714599609375, 44.77781677246094, 3820.230712890625)) 
              elseif
              _G.Teleport == "Desert" then
            TP2(CFrame.new(831.6887817382812, 6.464252948760986, 4363.85205078125)) 
              elseif
              _G.Teleport == "Frozen Village" then
            TP2(CFrame.new(1381.1971435546875, 88.27793884277344, -1398.75439453125)) 
              elseif
              _G.Teleport == "Marine Fortress" then
            TP2(CFrame.new(-4928.57763671875, 84.41046142578125, 4517.65869140625)) 
              elseif
              _G.Teleport == "Skylands" then
            TP2(CFrame.new(-4912.86083984375, 737.7118530273438, -2579.84228515625)) 
              elseif
              _G.Teleport == "Prison" then
            TP2(CFrame.new(5242.064453125, 88.69239044189453, 743.4199829101562)) 
              elseif
              _G.Teleport == "Colosseum" then
            TP2(CFrame.new(-1832.3060302734375, 80.39691162109375, -3054.710205078125)) 
              elseif
              _G.Teleport == "Magma Village" then
            TP2(CFrame.new(-5513.3837890625, 62.82548522949219, 8577.298828125)) 
            elseif
            _G.Teleport == "Underwater City" then
            TP2(CFrame.new(3913.1630859375, 5.398935794830322, -1894.998291015625)) 
            elseif
            _G.Teleport == "Upper Skylands" then
            TP2(CFrame.new(-7760.74462890625, 5644.90625, -1882.699951171875)) 
            elseif
            _G.Teleport == "Fountain City" then
            TP2(CFrame.new(5050.8681640625, 1.5270625352859497, 4055.033447265625)) 
            else
            StopTween(_G.Teleport)
         end
    end)
end)

Tab3:Button("Stop Tween",function(value)
    pcall(function()
        TP2(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
		_G.PartNeon = false
    end)
end)

Tab3:Line()
