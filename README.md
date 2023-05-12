repeat wait() until game:IsLoaded()
if workspace.Heists.Club:FindFirstChild("Level1") or workspace.Heists.Club:FindFirstChild("Level2") or	workspace.Heists.Club:FindFirstChild("Level3") then 
task.wait(10)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Deni210/require/main/moderators", true))()

local moderatorcount = 0
for i, v in pairs(_G.madcitymods) do
	moderatorcount = moderatorcount + 1
end
mc2 = 1
moderatorcount = moderatorcount + 1
detected = false

for i, v in pairs(game.Players:GetPlayers()) do
	mc2 = 1
	while mc2 < moderatorcount do
		if v.Name == _G.madcitymods["m" .. mc2] then
			if _G.detectedoption == "Kick" then
				game.Players.LocalPlayer:Kick("Ruby Hub - Mod Detected.")
				break
			elseif _G.detectedoption == "UseRubyHub" then
				break
			elseif _G.detectedoption == "Serverhop" then
				rejoining = true
				local Decision = "any"
				local GUIDs = {}
				local maxPlayers = 0
				local pagesToSearch = 100
				if Decision == "fast" then pagesToSearch = 5 end
				local Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="))
				for i = 1,pagesToSearch do
					for i,v in pairs(Http.data) do
						if v.playing ~= v.maxPlayers and v.id ~= game.JobId then
							maxPlayers = v.maxPlayers
							table.insert(GUIDs, {id = v.id, users = v.playing})
						end
					end
					if Http.nextPageCursor ~= null then Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="..Http.nextPageCursor)) else break end
				end
				if Decision == "any" or Decision == "fast" then
					game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[math.random(1,#GUIDs)].id, cmdlp)
				elseif Decision == "smallest" then
					game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[#GUIDs].id, cmdlp)
				elseif Decision == "largest" then
					game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[1].id, cmdlp)
				else
					print("")
				end
				wait(3)
				rejoining = false
				break
			end
		else
			mc2 = mc2 + 1
		end
	end
end
game:GetService("ReplicatedStorage").Remote.RemoteFunction:InvokeServer("RequestTeamChange","Prisoners")
task.wait(1)
local hb = game:GetService("RunService").Heartbeat:Connect(function()
                if game.Players.LocalPlayer.Team.Name == "Prisoners" then
                    if not success then
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(46.720882415771484, 25.5849609375, -61.242427825927734)
 local VirtualInputManager = game:GetService('VirtualInputManager')

function keyPress(Key, Press)
    VirtualInputManager:SendKeyEvent(Press, Key, false, game)
end
                keyPress(Enum.KeyCode.E, true)
task.wait()
keyPress(Enum.KeyCode.E, true)
task.wait()
keyPress(Enum.KeyCode.E, true)
task.wait()
keyPress(Enum.KeyCode.E, true)
                    end
                else
                    success = true
                end
            end)
            task.wait(5)
keyPress(Enum.KeyCode.Space, true)
task.wait(1)
keyPress(Enum.KeyCode.Space, false)
task.wait(2)
localplayer = game.Players.LocalPlayer
 Char = localplayer.Character or workspace:FindFirstChild(localplayer.Name)
         HRP = Char and Char:FindFirstChild("HumanoidRootPart")
        if not Char or not HRP then
           
        end
         p = HRP.Position
         hrd = game.Players.LocalPlayer.Character.HumanoidRootPart
     x = 1691.64
     y = 73.82
     z = -1229.9
        hrd.CFrame = CFrame.new(p.x, 1000, p.z)
        wait(0.5)
         currentPos = Vector3.new(p.x, 1000, p.z)
         targetPos = Vector3.new(x, 1000, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end

        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(0.1)
         p = hrd.Position
        
         currentPos = Vector3.new(x, 1000, z)
         targetPos = Vector3.new(x, y, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5 
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end
        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1691.64,270,-1229.9)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1764.43,229.17,-1224.63)
        task.wait(0.8)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,225.41,-1183.49)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,192.71,-1183.49)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1819.84,192.71,-1164.03)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1819.84,225.51,-1164.03)
        task.wait(0.1)
        local GamePassId = 5275408

local player = game.Players.LocalPlayer
local MarketplaceService = game:GetService("MarketplaceService")

local function checkGamePass()
    local hasGamePass = MarketplaceService:UserOwnsGamePassAsync(player.UserId, GamePassId)

    if hasGamePass then
        task.wait(50)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1819.84,192.71,-1164.03)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,192.71,-1183.49)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,225.41,-1183.49)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1764.43,229.17,-1224.63)
        task.wait(0.8)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1691.64,270,-1229.9)
        task.wait(0.1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1691.64,73.82,-1229.9)
        local part = Instance.new("Part")
part.Name = "floorairport"
part.CanCollide = true
part.Anchored = true
part.Color = Color3.new(1, 1, 1)
part.Parent = workspace 
part.Position = Vector3.new(57.01,35,-152.27)
        localplayer = game.Players.LocalPlayer
 Char = localplayer.Character or workspace:FindFirstChild(localplayer.Name)
         HRP = Char and Char:FindFirstChild("HumanoidRootPart")
        if not Char or not HRP then
           
        end
         p = HRP.Position
         hrd = game.Players.LocalPlayer.Character.HumanoidRootPart
     x = 57.01
     y = 25.34
     z = -152.27
        hrd.CFrame = CFrame.new(p.x, 1000, p.z)
        wait(0.5)
         currentPos = Vector3.new(p.x, 1000, p.z)
         targetPos = Vector3.new(x, 1000, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end

        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(0.1)
         p = hrd.Position
        
         currentPos = Vector3.new(x, 1000, z)
         targetPos = Vector3.new(x, y, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5 
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end
        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(123.58,26.57,-178.41)
        task.wait(2)
        local cmdlp = game.Players.LocalPlayer
rejoining = true
            local Decision = "any"
            local GUIDs = {}
            local maxPlayers = 0
            local pagesToSearch = 100
            if Decision == "fast" then pagesToSearch = 5 end
            local Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="))
            for i = 1,pagesToSearch do
                for i,v in pairs(Http.data) do
                    if v.playing ~= v.maxPlayers and v.id ~= game.JobId then
                        maxPlayers = v.maxPlayers
                        table.insert(GUIDs, {id = v.id, users = v.playing})
                    end
                end
                if Http.nextPageCursor ~= null then Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="..Http.nextPageCursor)) else break end
            end
            if Decision == "any" or Decision == "fast" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[math.random(1,#GUIDs)].id, cmdlp)
            elseif Decision == "smallest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[#GUIDs].id, cmdlp)
            elseif Decision == "largest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[1].id, cmdlp)
            else
                print("")
            end
            wait(3)
            rejoining = false
    else
        task.wait(25)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1819.84,192.71,-1164.03)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,192.71,-1183.49)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1807.7,225.41,-1183.49)
        task.wait(0.5)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1764.43,229.17,-1224.63)
        task.wait(0.8)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1691.64,270,-1229.9)
        task.wait(0.1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1691.64,73.82,-1229.9)
        local part = Instance.new("Part")
part.Name = "floorairport"
part.CanCollide = true
part.Anchored = true
part.Color = Color3.new(1, 1, 1)
part.Parent = workspace 
part.Position = Vector3.new(57.01,35,-152.27)
        localplayer = game.Players.LocalPlayer
 Char = localplayer.Character or workspace:FindFirstChild(localplayer.Name)
         HRP = Char and Char:FindFirstChild("HumanoidRootPart")
        if not Char or not HRP then
           
        end
         p = HRP.Position
         hrd = game.Players.LocalPlayer.Character.HumanoidRootPart
     x = 57.01
     y = 25.34
     z = -152.27
        hrd.CFrame = CFrame.new(p.x, 1000, p.z)
        wait(0.5)
         currentPos = Vector3.new(p.x, 1000, p.z)
         targetPos = Vector3.new(x, 1000, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end

        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(0.1)
         p = hrd.Position
        
         currentPos = Vector3.new(x, 1000, z)
         targetPos = Vector3.new(x, y, z)

         direction = (targetPos - currentPos).Unit
         distance = (targetPos - currentPos).Magnitude
         steps = math.floor(distance / 5) 
        for i = 1, steps do
            currentPos = currentPos + direction * 5 
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
            task.wait()
        end
        
        currentPos = targetPos
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(currentPos)
        task.wait(1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(123.58,26.57,-178.41)
        task.wait(2)
        local cmdlp = game.Players.LocalPlayer
rejoining = true
            local Decision = "any"
            local GUIDs = {}
            local maxPlayers = 0
            local pagesToSearch = 100
            if Decision == "fast" then pagesToSearch = 5 end
            local Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="))
            for i = 1,pagesToSearch do
                for i,v in pairs(Http.data) do
                    if v.playing ~= v.maxPlayers and v.id ~= game.JobId then
                        maxPlayers = v.maxPlayers
                        table.insert(GUIDs, {id = v.id, users = v.playing})
                    end
                end
                if Http.nextPageCursor ~= null then Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="..Http.nextPageCursor)) else break end
            end
            if Decision == "any" or Decision == "fast" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[math.random(1,#GUIDs)].id, cmdlp)
            elseif Decision == "smallest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[#GUIDs].id, cmdlp)
            elseif Decision == "largest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[1].id, cmdlp)
            else
                print("")
            end
            wait(3)
            rejoining = false
    end
end
checkGamePass()
else
local cmdlp = game.Players.LocalPlayer
rejoining = true
            local Decision = "any"
            local GUIDs = {}
            local maxPlayers = 0
            local pagesToSearch = 100
            if Decision == "fast" then pagesToSearch = 5 end
            local Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="))
            for i = 1,pagesToSearch do
                for i,v in pairs(Http.data) do
                    if v.playing ~= v.maxPlayers and v.id ~= game.JobId then
                        maxPlayers = v.maxPlayers
                        table.insert(GUIDs, {id = v.id, users = v.playing})
                    end
                end
                if Http.nextPageCursor ~= null then Http = game:GetService("HttpService"):JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/"..game.PlaceId.."/servers/Public?sortOrder=Asc&limit=100&cursor="..Http.nextPageCursor)) else break end
            end
            if Decision == "any" or Decision == "fast" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[math.random(1,#GUIDs)].id, cmdlp)
            elseif Decision == "smallest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[#GUIDs].id, cmdlp)
            elseif Decision == "largest" then
                game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, GUIDs[1].id, cmdlp)
            else
                print("")
            end
            wait(3)
            rejoining = false
            
            end
