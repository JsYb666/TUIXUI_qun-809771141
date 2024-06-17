function loadscript()



    local REN = {
        ["Name"] = "武士脚本",
        ["限免"] = true;
        ["lp"] = game.Players.LocalPlayer;
        ["游戏名1"] = game.Players.LocalPlayer.Name;
        ["游戏名2"] = game.Players.LocalPlayer.Character.Name;
        ["游戏名3"] = game.Players.LocalPlayer.DisplayName;
    --    ["游戏名4"] = player.Name;
        
        
        ["拓展表"] = {
            ["传送到玩家身边"] = {
                playernamedied = nil;
                dropdown = {};
            };
        };
    };
    
    
    local LBLG = Instance.new("ScreenGui", getParent)
    local LBL = Instance.new("TextLabel", getParent)
    local player = game.Players.LocalPlayer
    
    LBLG.Name = "LBLG"
    LBLG.Parent = game.CoreGui
    LBLG.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    LBLG.Enabled = true
    LBL.Name = "LBL"
    LBL.Parent = LBLG
    LBL.BackgroundColor3 = Color3.new(1, 1, 1)
    LBL.BackgroundTransparency = 1
    LBL.BorderColor3 = Color3.new(0, 0, 0)
    LBL.Position = UDim2.new(0.75,0,0.010,0)
    LBL.Size = UDim2.new(0, 133, 0, 30)
    LBL.Font = Enum.Font.GothamSemibold
    LBL.Text = "TextLabel"
    LBL.TextColor3 = Color3.new(1, 1, 1)
    LBL.TextScaled = true
    LBL.TextSize = 14
    LBL.TextWrapped = true
    LBL.Visible = true
    
    local FpsLabel = LBL
    local Heartbeat = game:GetService("RunService").Heartbeat
    local LastIteration, Start
    local FrameUpdateTable = { }
    
    local function HeartbeatUpdate()
        LastIteration = tick()
        for Index = #FrameUpdateTable, 1, -1 do
            FrameUpdateTable[Index + 1] = (FrameUpdateTable[Index] >= LastIteration - 1) and FrameUpdateTable[Index] or nil
        end
        FrameUpdateTable[1] = LastIteration
        local CurrentFPS = (tick() - Start >= 1 and #FrameUpdateTable) or (#FrameUpdateTable / (tick() - Start))
        CurrentFPS = CurrentFPS - CurrentFPS % 1
        FpsLabel.Text = ("北京时间:"..os.date("%H").."时"..os.date("%M").."分"..os.date("%S"))
    end
    Start = tick()
    Heartbeat:Connect(HeartbeatUpdate)
    
    local NotificationHolder = loadstring(game:HttpGet("https://raw.githubusercontent.com/BocusLuke/UI/main/STX/Module.Lua"))()
    local Notification = loadstring(game:HttpGet("https://raw.githubusercontent.com/BocusLuke/UI/main/STX/Client.Lua"))()
    local ui = loadstring(game:HttpGet("https://raw.githubusercontent.com/renlua/block/main/UI/%E5%BD%A9%E8%99%B9UI.lua"))();		
    local win = ui:new("武士脚本")
    --
    local UITab1 = win:Tab("『信息』",'6035145364')
    
    local about = UITab1:section("『信息』",true)
    
    
    about:Label("感谢支持")
    about:Label("超级脚本")
    about:Label("主作者江")
    about:Label("副作者丁丁 退休")
    
    
    
    
    
    local Player1 = win:Tab("基础功能",'6035145364')--2
    local rgb1 = win:Tab("光影",'6035145364')--3
    local ehe1 = win:Tab("俄亥俄州",'6035145364')--4
    local heh1 = win:Tab("奎尔湖",'6035145364')--4
    local bf1 = win:Tab("Blox fruits",'6035145364')--5
    local jy1 = win:Tab("监狱人生",'6035145364')--6
    local sjx1 = win:Tab("铲雪模拟器",'6035145364')--7
    local jjl = win:Tab("进击的僵尸",'6035145364')--8
    local DoorsTab1 = win:Tab("Doors",'6035145364')--9
    local zcxbrv = win:Tab("造船寻宝",'6035145364')--10
    local PHZMT2Tab1 = win:Tab("破坏者谜团2",'6035145364')--11
    local a1 = win:Tab("刀刃球",'6035145364')--12
    local JS1 = win:Tab("极速传奇",'6035145364')--13
    local RZCQ1 = win:Tab("忍者传奇",'6035145364')--14
    local li1 = win:Tab("力量传奇",'6035145364')--15
    local FM1 = win:Tab("伐木大亨2",'6035145364')--16
    local hjfsmnq = win:Tab("火箭发射模拟器",'6035145364')--17
    local RC1 = win:Tab("rc",'6035145364')--18
    local BZMNQ1 = win:Tab("巴掌模拟器",'6035145364')--19
    local CJ1 = win:Tab("超级大力士模拟器",'6035145364')--20
    local Tab1 = win:Tab("其他脚本『破解』",'6035145364')--21
    local music1 = win:Tab("音乐",'6035145364')--22
    
    local Player = Player1:section("基础功能",true)
    --
    local rgb = rgb1:section("光影",true)
    --
    --
    local ehe = ehe1:section("俄亥俄州",true)
    --
    local heh = heh1:section("奎尔湖",true)
    --
    local jy = jy1:section("监狱人生",true)
    --
    local sjx = sjx1:section("主要功能",true)
    --
    local jjb = jjl:section("主要功能",true)
    --
    local DoorsTab = DoorsTab1:section("中文脚本",false)
    local DoorsZHTab = DoorsTab1:section("招换物品",false)
    local DoorsYWTab = DoorsTab1:section("英文脚本",false)
    --
    local PHZMT2Tab = PHZMT2Tab1:section("主要功能",false)
    --
    local zcxbr = zcxbrv:section("农场",false)
    --
    local a = a1:section("刀刃球",false)
    --
    local JS = JS1:section("极速传奇",true)
    --
    local setup = RZCQ1:section("主要功能",false)
    local RZCQCS = RZCQ1:section("传送",false)
    --
    local li0 = li1:section("主要功能",false)
    local li = li1:section("传送",false)
    --
    local fjfs = hjfsmnq:section("主要功能&传送",false)
    --
    local RC = RC1:section("rc",true)
    --
    local BZMNQ = BZMNQ1:section("主要",true)
    local BZMNQZX = BZMNQ1:section("杂项",true)
    local BZMNQFJN = BZMNQ1:section("防技能",true)
    --
    local CJ = CJ1:section("超级大力士模拟器",true)
    --
    local Tab = Tab1:section("脚本中心",true)
    --
    local music = music1:section("音乐",true)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    function tp(p)
       game.Players.LocalPlayer.Character:PivotTo(p)
    end
    function shuaxinlb(zji)
        REN["拓展表"]["传送到玩家身边"].dropdown={}
        if zji==true then
        for p, I in next,game.Players:GetChildren() do
        table.insert(REN["拓展表"]["传送到玩家身边"].dropdown, I.Name)
        end
        else
        for p, I in next, game.Players:GetChildren() do
        if I ~= lp then
        table.insert(REN["拓展表"]["传送到玩家身边"].dropdown, I.Name)
        end
        end
        end
        end
    shuaxinlb(true)
    
    local dropdown = Player:Dropdown("选择玩家名称",'Dropdown',REN["拓展表"]["传送到玩家身边"].dropdown,function(v)
        REN["拓展表"]["传送到玩家身边"].playernamedied = v
    end)
    
    Player:Button("刷新列表", function()
        shuaxinlb(true)
        dropdown:SetOptions(REN["拓展表"]["传送到玩家身边"].dropdown)
    end)
    
    Player:Button("传送到玩家旁边",function()  
                tp(game:GetService("Players")[REN["拓展表"]["传送到玩家身边"].playernamedied].Character.HumanoidRootPart.CFrame + Vector3.new(0, 3, 0))
    end)
    
    Player:Button("透视",function()  
    _G.FriendColor = Color3.fromRGB(0, 0, 255)
        local function ApplyESP(v)
       if v.Character and v.Character:FindFirstChildOfClass'Humanoid' then
           v.Character.Humanoid.NameDisplayDistance = 9e9
           v.Character.Humanoid.NameOcclusion = "NoOcclusion"
           v.Character.Humanoid.HealthDisplayDistance = 9e9
           v.Character.Humanoid.HealthDisplayType = "AlwaysOn"
           v.Character.Humanoid.Health = v.Character.Humanoid.Health -- triggers changed
       end
    end
    for i,v in pairs(game.Players:GetPlayers()) do
       ApplyESP(v)
       v.CharacterAdded:Connect(function()
           task.wait(0.33)
           ApplyESP(v)
       end)
    end
    
    game.Players.PlayerAdded:Connect(function(v)
       ApplyESP(v)
       v.CharacterAdded:Connect(function()
           task.wait(0.33)
           ApplyESP(v)
       end)
    end)
    
        local Players = game:GetService("Players"):GetChildren()
    local RunService = game:GetService("RunService")
    local highlight = Instance.new("Highlight")
    highlight.Name = "Highlight"
    
    for i, v in pairs(Players) do
        repeat wait() until v.Character
        if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = v.Character
            highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlightClone.Name = "Highlight"
        end
    end
    
    game.Players.PlayerAdded:Connect(function(player)
        repeat wait() until player.Character
        if not player.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = player.Character
            highlightClone.Parent = player.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.Name = "Highlight"
        end
    end)
    
    game.Players.PlayerRemoving:Connect(function(playerRemoved)
        playerRemoved.Character:FindFirstChild("HumanoidRootPart").Highlight:Destroy()
    end)
    
    RunService.Heartbeat:Connect(function()
        for i, v in pairs(Players) do
            repeat wait() until v.Character
            if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
                local highlightClone = highlight:Clone()
                highlightClone.Adornee = v.Character
                highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
                highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
                highlightClone.Name = "Highlight"
                task.wait()
            end
    end
    end)
    end)
    
    Player:Button("飞行", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/28CWNSrK"))()
    end)
    
    Player:Button("飞行2", function()
        local Speed = 498
    
        -- Gui to Lua
        -- Version: 3.2
        local HumanoidRP = game.Players.LocalPlayer.Character.HumanoidRootPart
        -- Instances:
    
        local ScreenGui = Instance.new("ScreenGui")
        local W = Instance.new("TextButton")
        local S = Instance.new("TextButton")
        local A = Instance.new("TextButton")
        local D = Instance.new("TextButton")
        local Fly = Instance.new("TextButton")
        local unfly = Instance.new("TextButton")
        local StopFly = Instance.new("TextButton")
    
        --Properties:
    
        ScreenGui.Parent = game.CoreGui
        ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    
        unfly.Name = "unfly"
        unfly.Parent = ScreenGui
        unfly.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        unfly.Position = UDim2.new(0.694387913, 0, 0.181818187, 0)
        unfly.Size = UDim2.new(0, 72, 0, 50)
        unfly.Font = Enum.Font.SourceSans
        unfly.Text = "取消飞"
        unfly.TextColor3 = Color3.fromRGB(170, 0, 255)
        unfly.TextScaled = true
        unfly.TextSize = 14.000
        unfly.TextWrapped = 
            unfly.MouseButton1Down:Connect(function()
            HumanoidRP:FindFirstChildOfClass("BodyVelocity"):Destroy()
            HumanoidRP:FindFirstChildOfClass("BodyGyro"):Destroy()
        end)
    
        StopFly.Name = "Stop Fly"
        StopFly.Parent = ScreenGui
        StopFly.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        StopFly.Position = UDim2.new(0.695689976, 0, 0.0213903747, 0)
        StopFly.Size = UDim2.new(0, 71, 0, 50)
        StopFly.Font = Enum.Font.SourceSans
        StopFly.Text = "定"
        StopFly.TextColor3 = Color3.fromRGB(170, 0, 255)
        StopFly.TextScaled = true
        StopFly.TextSize = 14.000
        StopFly.TextWrapped = true
        StopFly.MouseButton1Down:Connect(function()
            HumanoidRP.Anchored = true
        end)
    
        Fly.Name = "Fly"
        Fly.Parent = ScreenGui
        Fly.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        Fly.Position = UDim2.new(0.588797748, 0, 0.0213903747, 0)
        Fly.Size = UDim2.new(0, 66, 0, 50)
        Fly.Font = Enum.Font.SourceSans
        Fly.Text = "飞"
        Fly.TextColor3 = Color3.fromRGB(170, 0, 127)
        Fly.TextScaled = true
        Fly.TextSize = 14.000
        Fly.TextWrapped = true
        Fly.MouseButton1Down:Connect(function()
            local BV = Instance.new("BodyVelocity",HumanoidRP)
            local BG = Instance.new("BodyGyro",HumanoidRP)
            BG.MaxTorque = Vector3.new(math.huge,math.huge,math.huge)
            BG.D = 5000
            BG.P = 50000
            BG.CFrame = game.Workspace.CurrentCamera.CFrame
            BV.MaxForce = Vector3.new(math.huge,math.huge,math.huge)
        end)
    
        W.Name = "W"
        W.Parent = ScreenGui
        W.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        W.Position = UDim2.new(0.161668837, 0, 0.601604283, 0)
        W.Size = UDim2.new(0, 58, 0, 50)
        W.Font = Enum.Font.SourceSans
        W.Text = "↑"
        W.TextColor3 = Color3.fromRGB(226, 226, 226)
        W.TextScaled = true
        W.TextSize = 5.000
        W.TextWrapped = true
        W.MouseButton1Down:Connect(function()
            HumanoidRP.Anchored = false
            HumanoidRP:FindFirstChildOfClass("BodyVelocity"):Destroy()
            HumanoidRP:FindFirstChildOfClass("BodyGyro"):Destroy()
            wait(.1)
            local BV = Instance.new("BodyVelocity",HumanoidRP)
            local BG = Instance.new("BodyGyro",HumanoidRP)
            BG.MaxTorque = Vector3.new(math.huge,math.huge,math.huge)
            BG.D = 5000
            BG.P = 50000
            BG.CFrame = game.Workspace.CurrentCamera.CFrame
            BV.MaxForce = Vector3.new(math.huge,math.huge,math.huge)
            BV.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * Speed
        end)
    
    
        S.Name = "S"
        S.Parent = ScreenGui
        S.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        S.Position = UDim2.new(0.161668837, 0, 0.735294104, 0)
        S.Size = UDim2.new(0, 58, 0, 50)
        S.Font = Enum.Font.SourceSans
        S.Text = "↓"
        S.TextColor3 = Color3.fromRGB(255, 255, 255)
        S.TextScaled = true
        S.TextSize = 14.000
        S.TextWrapped = true
        S.MouseButton1Down:Connect(function()
            HumanoidRP.Anchored = false
            HumanoidRP:FindFirstChildOfClass("BodyVelocity"):Destroy()
            HumanoidRP:FindFirstChildOfClass("BodyGyro"):Destroy()
            wait(.1)
            local BV = Instance.new("BodyVelocity",HumanoidRP)
            local BG = Instance.new("BodyGyro",HumanoidRP)
            BG.MaxTorque = Vector3.new(math.huge,math.huge,math.huge)
            BG.D = 5000
            BG.P = 50000
            BG.CFrame = game.Workspace.CurrentCamera.CFrame
            BV.MaxForce = Vector3.new(math.huge,math.huge,math.huge)
            BV.Velocity = game.Workspace.CurrentCamera.CFrame.LookVector * -Speed
        end)
    end)
    
    Player:Button("原子弹", function()
    use_load("https://pastebin.com/raw/FqWgJJEp")
    end)
    
    
    
    Player:Toggle("穿墙","Toggle",false,function(Value)
            if Value then
                Noclip = true
                Stepped = game.RunService.Stepped:Connect(function()
                    if Noclip == true then
                        for a, b in pairs(game.Workspace:GetChildren()) do
                            if b.Name == game.Players.LocalPlayer.Name then
                                for i, v in pairs(game.Workspace[game.Players.LocalPlayer.Name]:GetChildren()) do
                                    if v:IsA("BasePart") then
                                        v.CanCollide = false
                                    end
                                end
                            end
                        end
                    else
                        Stepped:Disconnect()
                    end
                end)
            else
                Noclip = false
            end
    end)
    
    Player:Toggle("夜视","Toggle",false,function(Value)
        Light = Value
        game.RunService.Stepped:Connect(function()
            if Light then
                game.Lighting.Ambient = Color3.new(1, 1, 1)
            else
                game.Lighting.Ambient = Color3.new(0, 0, 0)
            end
        end)
    end)
    
    Player:Toggle("无限跳","Toggle",false,function(Value)
        Jump = Value
        game.UserInputService.JumpRequest:Connect(function()
            if Jump then
                game.Players.LocalPlayer.Character.Humanoid:ChangeState("Jumping")
            end
        end)
    end)
    
    Player:Slider('设置速度', 'Sliderflag', 16, 16, 200,false, function(Value)
    game:GetService("RunService").RenderStepped:Connect(function()
            pcall(function()
                game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
            end)
        end)
    end)
    
    Player:Slider('设置血量', 'Sliderflag', 100, 1, 100,false, function(Value)
    game.Players.LocalPlayer.Character.Humanoid.Health = Value
    end)
    
    Player:Slider('设置重力', 'Sliderflag', 196.2, 196.2, 1000,false, function(Value)
        game.Workspace.Gravity = Value
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    rgb:Button("光影v4(曝光警告)", function()
    print("button pressed")
    use_load('https://pastebin.com/raw/gUceVJig')
    end)
    
    rgb:Button("RTX高仿", function()
    print("button pressed")
    use_load('https://pastebin.com/raw/Bkf0BJb3')
    end)
    
    rgb:Button("国外高质量光影菜单", function()
    print("button pressed")
    use_load('https://pastefy.ga/xXkUxA0P/raw')
    end)
    
    rgb:Button("光影", function()
    print("button pressed")
    use_load("https://raw.githubusercontent.com/MZEEN2424/Graphics/main/Graphics.xml")
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ehe:Button("俄亥俄州", function()
    use_load("https://pastebin.com/raw/hkvHeHed")
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    if game.PlaceId == 2753915549 then
    local bf = bf1:section("Blox fruits",true)
    bf:Label("Blox fruits更新删除")
    bf:Label("别问，问就是自己猜")
    else
    local bf = bf1:section("Blox fruits",true)
    bf:Label("请到Blox fruits使用脚本")
    end
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    heh:Toggle("无敌模式","", false, function(Value)
        game.ReplicatedStorage.DamageHumanoid:FireServer(-2e9)
    end)
    
    heh:Button("无限金钱", function()
    local money = {
       [1] = -9999,
       [2] = "Buy"
    }
    
    game:GetService("ReplicatedStorage").Pay:FireServer(unpack(money))
    end)
    
    heh:Button("无限金币", function()
    local gold = {
       [1] = game:GetService("Players").LocalPlayer.GoldCoins,
       [2] = 99999
    }
    
    game:GetService("ReplicatedStorage").ChangeValue:FireServer(unpack(gold))
    end)
    
    heh:Button("给所有物品", function()
    game.ReplicatedStorage.GiveTool:FireServer("SeaScooter")
    game.ReplicatedStorage.GiveTool:FireServer("Lantern")
    game.ReplicatedStorage.GiveTool:FireServer("Compass")
    game.ReplicatedStorage.GiveTool:FireServer("ItemFinder")
    game.ReplicatedStorage.GiveTool:FireServer("Aquabreather")
    end)
    
    heh:Button("红色套装", function()
    game.ReplicatedStorage.ChangeOutfits:FireServer("FireSuit")
    end)
    
    heh:Button("黄色套装", function()
    game.ReplicatedStorage.ChangeOutfits:FireServer("HazmatSuit")
    end)
    
    heh:Button("海盗套装", function()
    game.ReplicatedStorage.ChangeOutfits:FireServer("PirateCostume")
    end)
    
    heh:Button("动力套装", function()
    game.ReplicatedStorage.ChangeOutfits:FireServer("SuperScuba")
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    jy:Button("循环杀戮", function()
        use_load("https://pastebin.com/raw/ngdnaZbf")
    end)
    
    jy:Button("警卫室", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(847.7261352539062, 98.95999908447266, 2267.387451171875)
    end)
    
    jy:Button("监狱室内", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(919.2575073242188, 98.95999908447266, 2379.74169921875)
    end)
    
    jy:Button("罪犯复活点", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-937.5891723632812, 93.09876251220703, 2063.031982421875)
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    sjx:Toggle("自动收集雪","", false, function(Value)
        toggle = Value
    while toggle do wait()
    local args = {
        [1] = workspace:WaitForChild("HitParts"):WaitForChild("Snow1"),
        [2] = "Snow1",
        [3] = "MagicWand"
    }
    
    game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("e8eGb8RgRXFcug8q"):FireServer(unpack(args))
        end
    end)
    
    sjx:Toggle("自动出售雪（要传送到指定地方）",   "",false, function(Value)
    toggle = Value
    while toggle do wait()
    local args = {
        [1] = "SellSnow",
        [2] = "Frosty"
    }
    
    game:GetService("ReplicatedStorage"):WaitForChild("Modules"):WaitForChild("Network"):WaitForChild("RemoteEvent"):FireServer(unpack(args))
        end
    end)
    
    sjx:Button("传送出售雪的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(481.4659423828125, 15.846257209777832, -66.55204010009766)
    end)
    
    sjx:Button("传送买车的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(90.10160064697266, 16.051794052124023, -141.703125)
    end)
    
    sjx:Button("传送买工具的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(131.7429962158203, 16.39700698852539, -12.935890197753906)
    end)
    
    sjx:Button("传送买背包的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(348.6633605957031, 17.03822898864746, -16.793842315673828)
    end)
    
    sjx:Button("传送买假日礼物的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(154.57424926757812, 16.215335845947266, 147.10423278808594)
    end)
    
    sjx:Button("传送买宠物的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(138.49563598632812, 17.887277603149414, 278.3686218261719)
    end)
    
    sjx:Button("传送超大铲雪的地方", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-391.4309997558594, 15.84949016571045, 150.15187072753906)
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    jjb:Button("自动传送僵尸",function()
        local groundDistance = 8
    local Player = game:GetService("Players").LocalPlayer
    local function getNearest()
    local nearest, dist = nil, 99999
    for _,v in pairs(game.Workspace.BossFolder:GetChildren()) do
    if(v:FindFirstChild("Head")~=nil)then
    local m =(Player.Character.Head.Position-v.Head.Position).magnitude
    if(m<dist)then
    dist = m
    nearest = v
    end
    end
    end
    for _,v in pairs(game.Workspace.enemies:GetChildren()) do
    if(v:FindFirstChild("Head")~=nil)then
    local m =(Player.Character.Head.Position-v.Head.Position).magnitude
    if(m<dist)then
    dist = m
    nearest = v
    end
    end
    end
    return nearest
    end
    _G.farm2 = true
    Player.Chatted:Connect(function(m)
    if(m==";autofarm false")then
    _G.farm2 = false
    elseif(m==";autofarm true")then
    _G.farm2 = true
    end
    end)
    _G.globalTarget = nil
    game:GetService("RunService").RenderStepped:Connect(function()
    if(_G.farm2==true)then
    local target = getNearest()
    if(target~=nil)then
    game:GetService("Workspace").CurrentCamera.CFrame = CFrame.new(game:GetService("Workspace").CurrentCamera.CFrame.p, target.Head.Position)
    Player.Character.HumanoidRootPart.CFrame = (target.HumanoidRootPart.CFrame * CFrame.new(0, groundDistance, 9))
    _G.globalTarget = target
    end
    end
    end)
    spawn(function()
    while wait() do
    game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = Vector3.new(0,0,0)
    game.Players.LocalPlayer.Character.Torso.Velocity = Vector3.new(0,0,0)
    end
    end)
    while wait() do
    if(_G.farm2==true and _G.globalTarget~=nil and _G.globalTarget:FindFirstChild("Head") and Player.Character:FindFirstChildOfClass("Tool"))then
    local target = _G.globalTarget
    game.ReplicatedStorage.Gun:FireServer({["Normal"] = Vector3.new(0, 0, 0), ["Direction"] = target.Head.Position, ["Name"] = Player.Character:FindFirstChildOfClass("Tool").Name, ["Hit"] = target.Head, ["Origin"] = target.Head.Position, ["Pos"] = target.Head.Position,})
    wait()
    end
    end
       end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
         
          DoorsTab:Button("微山DOORS(2.3.2)", function()
          loadstring(game:HttpGet("\104\116\116\112\115\58\47\47\112\97\115\116\101\98\105\110\46\99\111\109\47\114\97\119\47\117\72\72\112\56\102\122\83"))()
    end)
          
          DoorsTab:Button(" 忍  -- Doors", function()
          loadstring(game:HttpGet(utf8.char((function() return table.unpack({104,116,116,112,115,58,47,47,112,97,115,116,101,98,105,110,46,99,111,109,47,114,97,119,47,52,117,109,83,68,85,57,87})end)())))();
    end)
          
    DoorsTab:Button("↓招换物品↓", function()
     end)
     
    
    DoorsZHTab:Button("可以清除东西的枪", function()
        use_load("https://raw.githubusercontent.com/K0t1n/Public/main/Laser%20Gun")
    end)                  
    DoorsZHTab:Button("十字架", function()
        use_load("https://pastebin.com/raw/FCSyG6Th")
    end)
          
    DoorsZHTab:Button("夜视仪", function()
        use_load("https://pastebin.com/raw/4Vsv1Xwn")
    end)
    
    
    DoorsZHTab:Button("神圣炸弹", function()
        use_load("https://pastebin.com/raw/u5B1UjGv")
    end)
          
    DoorsZHTab:Button("吸铁石", function()
        use_load("https://pastebin.com/raw/xHxGDp51")
    end)
          
    DoorsZHTab:Button("剪刀", function()
        use_load("https://pastebin.com/raw/v2yEJYmu")
    end)
          
    DoorsYWTab:Button("↓英文脚本↓", function()
    end)
    
    DoorsYWTab:Button("BlackKingq", function()
        use_load('https://pastebin.com/raw/R8QMbhzv')
    end)
          
    DoorsYWTab:Button("MS DOORS", function()
        use_load('https://raw.githubusercontent.com/mstudio45/MSDOORS/7bd97c2d956a775d683c2d7973d79715b30998ea/MSDOORS/Moonsec.lua')
    end)
          
          DoorsYWTab:Button("KINGHUB", function()
            use_load("https://pastebin.com/raw/x0EyeM6X")
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    PHZMT2Tab:Button("忍破坏者谜团2", function()
            R = "忍脚本交流群:139341298"
    loadstring(game:HttpGet("https://shz.al/~renPHZMT2"))();
    end)
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    PHZMT2Tab:Button("忍破坏者谜团2", function()
            R = "忍脚本交流群:139341298"
    loadstring(game:HttpGet("https://shz.al/~renPHZMT2"))();
    end)
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    zcxbr:Toggle("自动农场","",false, function(FARM)
    _G.FARMs = FARM
    while _G.FARMs do wait()
        pcall(function()
    game.Workspace.Gravity = 0
        wait(0.5)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-51.05019, 43.5682182, 702.193481, -0.999886811, -0.000135422233, 0.0150433034, 8.65181704e-09, 0.999959469, 0.00900237076, -0.0150439134, 0.00900135189, -0.999846339)}):Play()
        wait(1)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(30, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-50.4467354, 34.108551, 8676.95117, -0.999937415, -0.000405743311, 0.0111814411, -6.1212857e-09, 0.999342263, 0.0362627953, -0.0111888004, 0.0362605266, -0.999279737)}):Play()
        wait(30)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(5, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-54.1517258, -359.077667, 9497.03418, -0.99982208, 0.00359633542, -0.0185163822, -7.16419102e-09, 0.981655717, 0.190661997, 0.0188623965, 0.190628082, -0.981481075)}):Play()
        wait(5)
    game.Workspace.Gravity = 200
        wait(20)
        end)
     end
    end)
    zcxbr:Toggle("自动农场快速[测试版]","",false, function(FARM2)
    _G.FARM2s = FARM2
    while _G.FARM2s do wait()
        pcall(function()
    game.Workspace.Gravity = 0
        wait(0.5)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-51.05019, 43.5682182, 702.193481, -0.999886811, -0.000135422233, 0.0150433034, 8.65181704e-09, 0.999959469, 0.00900237076, -0.0150439134, 0.00900135189, -0.999846339)}):Play()
        wait(1)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(5, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-50.4467354, 34.108551, 8676.95117, -0.999937415, -0.000405743311, 0.0111814411, -6.1212857e-09, 0.999342263, 0.0362627953, -0.0111888004, 0.0362605266, -0.999279737)}):Play()
        wait(5)
    local TweenService = game:GetService("TweenService")
    local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(5, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
    {CFrame = CFrame.new(-51.05019, 43.5682182, 702.193481, -0.999886811, -0.000135422233, 0.0150433034, 8.65181704e-09, 0.999959469, 0.00900237076, -0.0150439134, 0.00900135189, -0.999846339)}):Play()
        wait(5)
    local Event = game:GetService("Workspace").ClaimRiverResultsGold
    Event:FireServer()
        wait(0.1)
    game.Players.LocalPlayer.Character.Humanoid.Health = -1000
        wait(0.1)
    game.Workspace.Gravity = 200
        wait(7)
        end)
     end
    end)
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    a:Button("忍刀刃球 V2",function()
    local Library = use_load("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard")
    
    local PhantomForcesWindow = Library:NewWindow("忍刀刃球 V2")
    
    local Bladeball = PhantomForcesWindow:NewSection("刀刃球")
    
    Bladeball:CreateToggle("Auto Parry ", function()
        use_load("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Parry")
      end)
    
    Bladeball:CreateToggle("Auto Spam V1 (Credits=JoeHub)", function()
        use_load("https://raw.githubusercontent.com/DonGabrielle/AutoDetectV4/main/MainBalls")
    end)
    
    Bladeball:CreateButton("Auto Spam V2", function()
        use_load("https://pastebin.com/raw/t2391h1A")
    
    end)
    
    Bladeball:CreateToggle("AutoDetectV1", function ()
        use_load('https://pastebin.com/raw/HPNBFGSf')
    end)
    
    Bladeball:CreateButton("ToggleBlockSpam:By Hosvile", function()game:GetService("StarterGui"):SetCore("SendNotification",{
        Title = "Script by Hosvile",
        Text = "Hold Block button to Spam",
        Duration = 5
    })
    
    getgenv().SpamSpeed = 25 -- 1-25
    
    if not getgenv().exeSpam then
        use_load("https://raw.githubusercontent.com/Hosvile/Refinement/main/Toggle%20Block%20Spam")
    end
    
    getgenv().exeSpam = true
      end)
    
    Bladeball:CreateButton("Fps Booster", function()_G.Settings = {
        Players = {
            ["Ignore Me"] = true, -- Ignore your Character
            ["Ignore Others"] = true-- Ignore other Characters
        },
        Meshes = {
            Destroy = false, -- Destroy Meshes
            LowDetail = true -- Low detail meshes (NOT SURE IT DOES ANYTHING)
        },
        Images = {
            Invisible = true, -- Invisible Images
            LowDetail = false, -- Low detail images (NOT SURE IT DOES ANYTHING)
            Destroy = false, -- Destroy Images
        },
        ["No Particles"] = true, -- Disables all ParticleEmitter, Trail, Smoke, Fire and Sparkles
        ["No Camera Effects"] = true, -- Disables all PostEffect's (Camera/Lighting Effects)
        ["No Explosions"] = true, -- Makes Explosion's invisible
        ["No Clothes"] = true, -- Removes Clothing from the game
        ["Low Water Graphics"] = true, -- Removes Water Quality
        ["No Shadows"] = true, -- Remove Shadows
        ["Low Rendering"] = true, -- Lower Rendering
        ["Low Quality Parts"] = true -- Lower quality parts
    }
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CasperFlyModz/discord.gg-rips/main/FPSBooster.lua"))()
      end)
    
    Bladeball:CreateToggle("Destroy Particle", function()loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/Destroy%20Particle%20Emitters",true))()
      end)
    
    Bladeball:CreateButton("HoldToSpam:By Hosvile",
    function()getgenv().SpamSpeed = 9
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Spam",true))()
      end) 
    
    Bladeball:CreateToggle("Aiming Mechanism", 
    function()loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/M%3ABlade%20Ball%20Mechanism",true))()
      end)
      
    BladeBall:CreateToggle("Auto Clash", 
    function()loadstring(game:HttpGet("https://pastebin.com/raw/t2391h1A"))()
     end)
     end)
    
    a:Button("忍刀刃球 V3",function()
    local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/FUEx0f3G')))()
    
    
    
    local Window = OrionLib:MakeWindow({Name = "忍刀刃球 V3", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
    
    --[[
    Name = <string> - The name of the UI.
    HidePremium = <bool> - Whether or not the user details shows Premium status or not.
    SaveConfig = <bool> - Toggles the config saving in the UI.
    ConfigFolder = <string> - The name of the folder where the configs are saved.
    IntroEnabled = <bool> - Whether or not to show the intro animation.
    IntroText = <string> - Text to show in the intro animation.
    IntroIcon = <string> - URL to the image you want to use in the intro animation.
    Icon = <string> - URL to the image you want displayed on the window.
    CloseCallback = <function> - Function to execute when the window is closed.
    ]]
    
    
    
    local Tab = Window:MakeTab({
        Name = "自动打击",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })
    
    --[[
    Name = <string> - The name of the tab.
    Icon = <string> - The icon of the tab.
    PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
    ]]
    
    
    
    local Section = Tab:AddSection({
        Name = "Menu"
    })
    
    --[[
    Name = <string> - The name of the section.
    ]]
    
    
    
    OrionLib:MakeNotification({
        Name = "Title!",
        Content = "Notification content... what will it say??",
        Image = "rbxassetid://4483345998",
        Time = 5
    })
    
    --[[
    Title = <string> - The title of the notification.
    Content = <string> - The content of the notification.
    Image = <string> - The icon of the notification.
    Time = <number> - The duration of the notfication.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Galaxy Hub",
        Callback = function()
                  loadstring(game:HttpGet("https://pastebin.com/raw/fruEwHqY"))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]] 
    
    
    
    Tab:AddButton({
        Name = "Hold To Spam (Op)",
        Callback = function()
                  getgenv().SpamSpeed = 9
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Spam",true))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Auto Parry",
        Callback = function()
                  loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Parry",true))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Auto Clash!",
        Callback = function()
                  loadstring(game:HttpGet("https://pastebin.com/raw/t2391h1A"))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Aiming Mechainsm!",
        Callback = function()
                  loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/M%3ABlade%20Ball%20Mechanism",true))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Fps Boost!",
        Callback = function()
                  _G.Settings = {
        Players = {
            ["Ignore Me"] = true, -- Ignore your Character
            ["Ignore Others"] = true-- Ignore other Characters
        },
        Meshes = {
            Destroy = false, -- Destroy Meshes
            LowDetail = true -- Low detail meshes (NOT SURE IT DOES ANYTHING)
        },
        Images = {
            Invisible = true, -- Invisible Images
            LowDetail = false, -- Low detail images (NOT SURE IT DOES ANYTHING)
            Destroy = false, -- Destroy Images
        },
        ["No Particles"] = true, -- Disables all ParticleEmitter, Trail, Smoke, Fire and Sparkles
        ["No Camera Effects"] = true, -- Disables all PostEffect's (Camera/Lighting Effects)
        ["No Explosions"] = true, -- Makes Explosion's invisible
        ["No Clothes"] = true, -- Removes Clothing from the game
        ["Low Water Graphics"] = true, -- Removes Water Quality
        ["No Shadows"] = true, -- Remove Shadows
        ["Low Rendering"] = true, -- Lower Rendering
        ["Low Quality Parts"] = true -- Lower quality parts
    }
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CasperFlyModz/discord.gg-rips/main/FPSBooster.lua"))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Auto Spam",
        Callback = function()
                  loadstring(game:HttpGet("https://pastebin.com/raw/t2391h1A"))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Auto Detect Spam",
        Callback = function()
                  loadstring(game:HttpGet(('https://pastebin.com/raw/HPNBFGSf'),true))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Toggle block spam",
        Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/L6d4u6me",true))()
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    local Tab = Window:MakeTab({
        Name = "目录2",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })
    
    --[[
    Name = <string> - The name of the tab.
    Icon = <string> - The icon of the tab.
    PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Wait Next Update",
        Callback = function()
                  print("button pressed")
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Owner Gerend",
        Callback = function()
                  print("button pressed")
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Dev Suzuyan",
        Callback = function()
                  print("button pressed")
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
    
    
    
    Tab:AddButton({
        Name = "Partner KKUR0MI",
        Callback = function()
                  print("button pressed")
          end    
    })
    
    --[[
    Name = <string> - The name of the button.
    Callback = <function> - The function of the button.
    ]]
     end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    
    JS:Button("极速传奇", function()
        use_load('https://shz.al/~renJS')
    end)
    
    JS:Button("极速传奇", function()
        use_load('https://pastebin.com/raw/rqnKXF4h')
    end)
    
    JS:Button("返回出生岛", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-9682.98828125, 58.87917709350586, 3099.033935546875)      
    end)
    
    JS:Button("白雪城", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-9676.138671875, 58.87917709350586, 3782.69384765625)   
    end)
    
    JS:Button("熔岩城", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-11054.96875, 216.83917236328125, 4898.62841796875)       
    end)
    
    JS:Button("传奇公路", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-13098.87109375, 216.83917236328125, 5907.6279296875)    
    end)
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    
    setup:Toggle("白天",function()
    Day = Value
    end)
    
    setup:Toggle("自动挥舞","", false, function(v)
        if v or not v then
            getgenv().autoswing = v
                while true do
                    if not getgenv().autoswing then return end
                    for _,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v:FindFirstChild("ninjitsuGain") then
                            game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                            break
                        end
                    end
                    local A_1 = "swingKatana"
                    local Event = game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(A_1)
                    wait()
                end
            end
    end)
    
    setup:Toggle("自动售卖", "",false, function(v)
        getgenv().autosell = v
            while true do
                if not getgenv().autosell then return end
                game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                wait(0.1)
                game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = CFrame.new(0,0,0)
                wait(0.1)
            end
        end)
    
    setup:Toggle("自动购买排名", "",false, function(v)
        getgenv().autobuyranks = v
            while true do
                if not getgenv().autobuyranks then return end
                local deku1 = "buyRank"
                for i = 1, #ranks do
                    game:GetService("Players").LocalPlayer.ninjaEvent:FireServer(deku1, ranks[i])
                end
                wait(0.1)
            end
    end)
    
    setup:Toggle("自动购买腰带", "",false, function(v)
        getgenv().autobuybelts = v
            while true do
                if not getgenv().autobuybelts then return end
                local A_1 = "buyAllBelts"
                local A_2 = "Inner Peace Island"
                local Event = game:GetService("Players").LocalPlayer.ninjaEvent
                Event:FireServer(A_1, A_2)
                wait(0.5)
            end
    end)
    
    setup:Toggle("自动购买技能", "",false, function(v)
        getgenv().autobuyskills = v
            while true do
                if not getgenv().autobuyskills then return end
                local A_1 = "buyAllSkills"
                local A_2 = "Inner Peace Island"
                local Event = game:GetService("Players").LocalPlayer.ninjaEvent
                Event:FireServer(A_1, A_2)
                wait(0.5)
            end
    end)
    
    setup:Toggle("自动购买剑", "",false, function(v)
        getgenv().autobuy = v
            while true do
                if not getgenv().autobuy then return end
                local A_1 = "buyAllSwords"
                local A_2 = "Inner Peace Island"
                local Event = game:GetService("Players").LocalPlayer.ninjaEvent
                Event:FireServer(A_1, A_2)
                wait(0.5)
            end
    end)
    
    
    
    
    setup:Button("解锁所有岛屿",function()
        for i,v in next, game.workspace.islandUnlockParts:GetChildren() do 
            if v then 
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.islandSignPart.CFrame -Vector3.new(0,80, 0)
               wait(0.5)
            end
        end
    end)
    setup:Button("收集所有宝箱",function()
        game:GetService("Workspace").mythicalChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").goldenChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").enchantedChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").magmaChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").legendsChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").eternalChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").saharaChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").thunderChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").ancientChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").midnightShadowChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").groupRewardsCircle["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace")["Daily Chest"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace")["wonderChest"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(3.5)
            game:GetService("Workspace").wonderChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            game:GetService("Workspace").midnightShadowChest["circleInner"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            game:GetService("Workspace").ancientChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").midnightShadowChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").thunderChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").saharaChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").eternalChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").legendsChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").magmaChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").enchantedChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").goldenChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").mythicalChest["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace").groupRewardsCircle["circleInner"].CFrame = game.Workspace.Part.CFrame
            game:GetService("Workspace")["Daily Chest"].circleInner.CFrame = game.Workspace.Part.CFrame
    end)
    setup:Button("杀死所有人",function()
                   for i,v in pairs(game.Players:GetChildren()) do
                    if v.Name~=game.Players.LocalPlayer then
                         for i=1,50 do
                                                     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=v.Character.HumanoidRootPart.CFrame+ Vector3.new(0, .4, 2)
                             
                                 task.wait()
                          if game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart") then
                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") then 
                    game.Players.LocalPlayer.ninjaEvent:FireServer("swingKatana")
                else
                    for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do 
                        if v.ClassName == "Tool" and v:FindFirstChild("attackShurikenScript") then 
                            game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                        end
                            if v.ClassName == "Tool" and v:FindFirstChild("attackKatanaScript") then 
                                game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)                            
                            end
                    end
                   end
         
            
                
           
                    end
                end
            end
        
                
                end
       
    end)
    
    
    RZCQCS:Button("出生点",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(25.665502548217773, 3.4228405952453613, 29.919952392578125)
    end)
    
    RZCQCS:Button("附魔岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(51.17238235473633, 766.1807861328125, -138.44842529296875)
    end)
    
    RZCQCS:Button("星界岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(207.2932891845703, 2013.88037109375, 237.36672973632812)
    end)
    
    RZCQCS:Button("神秘岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(171.97178649902344, 4047.380859375, 42.0699577331543)
    end)
    
    RZCQCS:Button("太空岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(148.83824157714844, 5657.18505859375, 73.5014877319336)
    end)
    
    RZCQCS:Button("冻土岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(139.28330993652344, 9285.18359375, 77.36406707763672)
    end)
    
    RZCQCS:Button("永恒岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(149.34817504882812, 13680.037109375, 73.3861312866211)
    end)
    
    RZCQCS:Button("沙暴岛",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(133.37144470214844, 17686.328125, 72.00334167480469)
    end)
    
    
    RZCQCS:Button("雷暴岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(143.19349670410156, 24070.021484375, 78.05432891845703)
        end)
    
    RZCQCS:Button("远古炼狱岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(141.27163696289062, 28256.294921875, 69.3790283203125)
        end)
    
    RZCQCS:Button("午夜暗影岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(132.74267578125, 33206.98046875, 57.495574951171875)
        end)
    
    RZCQCS:Button("神秘灵魂岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(137.76148986816406, 39317.5703125, 61.06639862060547)
        end)
    
    RZCQCS:Button("冬季奇迹岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(137.2720184326172, 46010.5546875, 55.941951751708984)
        end)
    
    RZCQCS:Button("黄金大师岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(128.32339477539062, 52607.765625, 56.69411849975586)
        end)
    
    RZCQCS:Button("龙传奇岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(146.35226440429688, 59594.6796875, 77.53300476074219)
        end)
    
    RZCQCS:Button("赛博传奇岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(137.3321075439453, 66669.1640625, 72.21722412109375)
        end)
    
    RZCQCS:Button("天岚超能岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.48077392578125, 70271.15625, 57.02311325073242)
        end)
    
    RZCQCS:Button("混沌传奇岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(148.58590698242188, 74442.8515625, 69.3177719116211)
        end)
    
    RZCQCS:Button("灵魂融合岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(136.9700927734375, 79746.984375, 58.54051971435547)
        end)
    
    RZCQCS:Button("黑暗元素岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(141.697265625, 83198.984375, 72.73107147216797)
        end)
    
    RZCQCS:Button("内心和平岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.3157501220703, 87051.0625, 66.78429412841797)
        end)
    
    RZCQCS:Button("炽烈漩涡岛",function()
        
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.08216857910156, 91246.0703125, 69.56692504882812)
            end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------    
    li0:Button("忍力量传奇",function()
            R = "忍脚本交流群:139341298"
    loadstring(game:HttpGet("https://shz.al/~renli"))();
    end)
    
    li0:Toggle("自动举哑铃开关",'Toggleflag',false, function(state)
        if li0.Text=="关"
        then li0.Text="开"
        else li0.Text="关"
        end
        if state then
            local part = Instance.new('Part', workspace)
            part.Size = Vector3.new(500, 20, 530.1)
            part.Position = Vector3.new(0, 100000, 133.15)
            part.CanCollide = true
            part.Anchored = true
            local rs = game:GetService("RunService").RenderStepped
            while wait() do 
            if li0.Text=="关" then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0)
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v.ClassName == "Tool" and v.Name == "Weight" then
            v.Parent = game.Players.LocalPlayer.Character
            end
            end
            game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
            end
            end
            end
    end)
    li0:Toggle("自动俯卧撑开关",'Toggleflag',false, function(state)
        if li0.Text=="关"
        then li0.Text="开"
        else li0.Text="关"
        end
        if state then
            local part = Instance.new('Part', workspace)
            part.Size = Vector3.new(500, 20, 530.1)
            part.Position = Vector3.new(0, 100000, 133.15)
            part.CanCollide = true
            part.Anchored = true
            local rs = game:GetService("RunService").RenderStepped
            while wait() do 
            if li0.Text=="关" then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0)
            
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v.ClassName == "Tool" and v.Name == "Pushups" then
                    v.Parent = game.Players.LocalPlayer.Character
                    end
            end
            game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
            end
            end
            end 
    end)
    li0:Toggle("自动仰卧起坐开关",'Toggleflag',false, function(state)
        if li0.Text=="关"
        then li0.Text="开"
        else li0.Text="关"
        end
        if state then
            local part = Instance.new('Part', workspace)
            part.Size = Vector3.new(500, 20, 530.1)
            part.Position = Vector3.new(0, 100000, 133.15)
            part.CanCollide = true
            part.Anchored = true
            local rs = game:GetService("RunService").RenderStepped
            while wait() do 
            if li0.Text=="关" then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0)
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v.ClassName == "Tool" and v.Name == "Situps" then
                    v.Parent = game.Players.LocalPlayer.Character
                    end
                    end
            end
            game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
             end
        end
    end)
    li0:Toggle("自动倒立身体",'Toggleflag',false, function(state)
        if li0.Text=="关"
        then li0.Text="开"
        else li0.Text="关"
        end
        if state then
            local part = Instance.new('Part', workspace)
        part.Size = Vector3.new(500, 20, 530.1)
        part.Position = Vector3.new(0, 100000, 133.15)
        part.CanCollide = true
        part.Anchored = true
        local rs = game:GetService("RunService").RenderStepped
        while wait() do 
        if li0.Text=="关" then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0)
        
        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v.ClassName == "Tool" and v.Name == "Handstands" then
                v.Parent = game.Players.LocalPlayer.Character
                
                end
                end
        end
        game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
        end
        end
        end)
        li0:Toggle("自动锻炼开关",'Toggleflag',false, function(state)
            if li0.Text=="关"
        then li0.Text="开"
        else li0.Text="关"
        end
            if state then
                local part = Instance.new('Part', workspace)
        part.Size = Vector3.new(500, 20, 530.1)
        part.Position = Vector3.new(0, 100000, 133.15)
        part.CanCollide = true
        part.Anchored = true
    
        while wait() do 
        if li0.Text=="关" then
    
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0, 50, 0)
            for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if
                    v.ClassName == "Tool" and v.Name == "Handstands" or v.Name == "Situps" or v.Name == "Pushups" or
                        v.Name == "Weight"
                 then
                    v:FindFirstChildOfClass("NumberValue").Value = 0
                    repeat
                        wait()
                    until game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool")
                    game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):EquipTool(v)
                    game:GetService("Players").LocalPlayer.muscleEvent:FireServer("rep")
    
    end
    end
    end
    end
              end
        end)
        li0:Toggle("自动重生开关",'Toggleflag',false, function(state)
            if li0.Text=="关"
    then li0.Text="开"
    else li0.Text="关"
    end
            if state then
                while wait() do 
                    if li0.Text=="关" then
                        game:GetService("ReplicatedStorage").rEvents.rebirthRemote:InvokeServer("rebirthRequest")
                    
                    end
                    end                
            end
        end)
        li0:Button("收集宝石",function()
            jk = {}
    for _, v in pairs(game:GetService("ReplicatedStorage").chestRewards:GetDescendants()) do
        if v.Name ~= "Light Karma Chest" or v.Name ~= "Evil Karma Chest" then
            table.insert(jk, v.Name)
        end
    end
    for i = 1, #jk do
        wait(2)
        game:GetService("ReplicatedStorage").rEvents.checkChestRemote:InvokeServer(jk[i])
    end
        end)
        li0:Toggle("自动比赛开关",'Toggleflag',false, function(state)
            if li0.Text=="关"
    then li0.Text="开"
    else li0.Text="关"
        end
            if state then
                while wait() do 
                    if li0.Text=="自动加入战斗（开）" then
                wait(2)
                game:GetService("ReplicatedStorage").rEvents.brawlEvent:FireServer("joinBrawl")
                    end
                    end
            end
        end)
    
    
    li:Button("传送到出生点", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(7, 3, 108)
    end)
    
    li:Button("传送到冰霜健身房", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2543, 13, -410)
    end)
     
    li:Button("传送到神话健身房", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2177, 13, 1070)
    end)
     
    li:Button("传送到永恒健身房", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6686, 13, -1284)
    end)
     
    li:Button("传送到传说健身房", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4676, 997, -3915)
    end)
     
    li:Button("传送到肌肉之王健身房", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-8554, 22, -5642)
    end)
     
    li:Button("传送到安全岛", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-39, 10, 1838)
    end)
     
    li:Button("传送到幸运抽奖区域", function()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2606, -2, 5753)
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------    
    
    local FM = FM1:section("伐木大亨2",false)
    
    FM:Button("bark2.0", function()
        use_load(utf8.char(104,116,116,112,115,58,47,47,114,97,119,46,103,105,116,104,117,98,117,115,101,114,99,111,110,116,101,110,116,46,99,111,109,47,110,111,111,98,54,49,54,49,54,49,47,82,79,66,76,79,88,47,109,97,105,110,47,98,97,114,107,50,46,48,46,108,117,97))
    end)    
                          
        
     FM:Button(" 忍  -- 伐木大亨2(盗版浮光掠影)", function()
     loadstring(game:HttpGet(utf8.char((function() return table.unpack({104,116,116,112,115,58,47,47,112,97,115,116,101,98,105,110,46,99,111,109,47,114,97,119,47,98,51,115,84,68,86,112,116})end)())))();
     
     end)
    
          
    FM:Button("白脚本伐木大亨2[免费](已修复)", function()
        use_load("https://raw.githubusercontent.com/noob616161/KphoooOooooOoOo-wprfbdksorbfKvsdcIUH-194jddJ-___-_-lIlIIIllIIIlllIIIIlIlIIlIllIIIllllllIllllllIIIl/main/bai/%E4%BC%90%E6%9C%A8")
    end)
        
    FM:Button("伐木大亨2多功能", function()
        use_load('https://raw.githubusercontent.com/Butterisgood/butter-hub/main/Butterhub.txt')
    end)
    
    FM:Dropdown("传送", 'Dropdown',
        {'出生点', '木材反斗城', '土地商店', '桥', '码头', '椰子岛', '洞穴', '鲨鱼斧合成',
         '火山', '沼泽', '家具店', '盒子车行', '连锁逻辑店', '鲍勃的小店', '画廊', '雪山',
         '灵视神殿', '怪人', '小绿盒', '滑雪小屋', '黄金木洞穴', '小鸟斧头', "灯塔"},
        function(b)
            if b == '木材反斗城' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(270, 4, 60)
            elseif b == '出生点' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(174, 10.5, 66)
            elseif b == '土地商店' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(270, 3, -98)
            elseif b == '桥' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(112, 37, -892)
            elseif b == '码头' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1136, 0, -206)
            elseif b == '椰子岛' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2614, -4, -34)
            elseif b == '洞穴' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3590, -177, 415)
            elseif b == '火山' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1588, 623, 1069)
            elseif b == '沼泽' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1216, 131, -822)
            elseif b == '家具店' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(486, 3, -1722)
            elseif b == '盒子车行' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(509, 3, -1458)
            elseif b == '雪山' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1487, 415, 3259)
            elseif b == '连锁逻辑店' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4615, 7, -794)
            elseif b == '鲍勃的小店' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(292, 8, -2544)
            elseif b == '画廊' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(5217, -166, 721)
            elseif b == '灵视神殿' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1608, 195, 928)
            elseif b == '怪人' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1071, 16, 1141)
            elseif b == '小绿盒' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1667, 349, 1474)
            elseif b == '滑雪小屋' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1244, 59, 2290)
            elseif b == '黄金木洞穴' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1080, -5, -942)
            elseif b == '鲨鱼斧合成' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(330.259735, 45.7998505, 1943.30823, 0.972010553, -8.07546598e-08, 0.234937176,
                    7.63610259e-08, 1, 2.77986647e-08, -0.234937176, -9.08055142e-09, 0.972010553)
            elseif b == '小鸟斧头' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4813.1, 33.5, -978.8)
            elseif b == '灯塔' then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1464.8, 356.3, 3257.2)
            end
    
        end)
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  
    
    fjfs:Button("发射台岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-123.15931701660156, 2.7371432781219482, 3.491959810256958)
    end)
    
    fjfs:Button("白云岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-76.13252258300781, 170.55825805664062, -60.4516716003418)
    end)
    
    fjfs:Button("浮漂岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-66.51714324951172, 720.4866333007812, -5.391753196716309)
    end)
    
    fjfs:Button("卫星岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-34.2462043762207, 1429.4990234375, 1.3739361763000488)
    end)
    
    fjfs:Button("蜜蜂迷宫岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6.5361199378967285, 3131.249267578125, -29.759048461914062)
    end)
    
    fjfs:Button("月球人救援", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-7.212917804718018, 5016.341796875, -19.815933227539062)
    end)
    
    fjfs:Button("暗物质岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(68.43186950683594, 6851.94091796875, 7.890637397766113)
    end)
    
    fjfs:Button("太空岩石岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(49.92888641357422, 8942.955078125, 8.674375534057617)
    end)
    
    fjfs:Button("零号火星岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(54.44503402709961, 11270.0927734375, -1.273137092590332)
    end)
    
    fjfs:Button("太空水晶小行星岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-11.579089164733887, 15295.6318359375, -27.54974365234375)
    end)
    
    fjfs:Button("月球浆果岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-14.601255416870117, 18410.9609375, 0.9418511986732483)
    end)
    
    fjfs:Button("铺路石岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3.272758960723877, 22539.494140625, 63.283935546875)
    end)
    
    fjfs:Button("流星岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-45.515689849853516, 27961.560546875, -7.358333110809326)
    end)
    
    fjfs:Button("升级岛", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2.7595248222351074, 33959.98828125, 53.93095397949219)
    end)
    
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  
    RC:Button("白脚本rc[免费](已修复)", function()
        use_load("https://raw.githubusercontent.com/noob616161/KphoooOooooOoOo-wprfbdksorbfKvsdcIUH-194jddJ-___-_-lIlIIIllIIIlllIIIIlIlIIlIllIIIllllllIllllllIIIl/main/bai/rc")
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------      
    
    BZMNQ:Toggle("无CD","Toggle" ,false, function(Value)
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local tool = character:FindFirstChildOfClass("Tool") or player.Backpack:FindFirstChildOfClass("Tool")
    
    bazhangmnq = Value
    
    while bazhangmnq do
    local localscript = tool:FindFirstChildOfClass("LocalScript")
    local localscriptclone = localscript:Clone()
    localscriptclone = localscript:Clone()
    localscriptclone:Clone()
    localscript:Destroy()
    localscriptclone.Parent = tool
    wait(0.1)
    end
    end)
    
    BZMNQ:Button("获取计数器手套", function()
    fireclickdetector(game.Workspace.CounterLever.ClickDetector)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,100,0)
    wait(0.2)
    game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
    wait(121)
    for i,v in pairs(workspace.Maze:GetDescendants()) do
    if v:IsA("ClickDetector") then
    fireclickdetector(v)
    end
    end
    end)
    
    BZMNQ:Toggle("地牢亮度","Toggle" ,false, function(Value)
     Light = Value
        if not Light then
            game.Lighting.Ambient = Color3.new(0, 0, 0)
        end
    end)
    
    BZMNQ:Dropdown("传送","Dropdown",{"安全区","竞技场","埃及岛","果实岛","盘子","锦标赛","默认竞技场"},function(Value)
    if Value == "安全区" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Spot.CFrame * CFrame.new(0,40,0)
    elseif Value == "竞技场" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Origo.CFrame * CFrame.new(0,-5,0)
    elseif Value == "埃及岛" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(215, -15.5, 0.5)
    elseif Value == "果实岛" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Arena.island5.Union.CFrame * CFrame.new(0,3.25,0)
    elseif Value == "盘子" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Arena.Plate.CFrame * CFrame.new(0,2,0)
    elseif Value == "锦标赛" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Battlearena.Arena.CFrame * CFrame.new(0,10,0)
    elseif Value == "默认竞技场" then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(120,360,-3)
    end
    end)
    
    BZMNQ:Toggle("复古技能","Toggle" ,false, function(Value)
    RetroSpam = Value
    while RetroSpam do
    game:GetService("ReplicatedStorage").RetroAbility:FireServer(RetroAbility)
    task.wait()
    end
    end)
    
    BZMNQ:Dropdown("复古技能选择","Dropdown",{"Rocket Launcher","Ban Hammer","Bomb"}, function(Value)
    RetroAbility = Value
    end)
    
    BZMNQ:Toggle("自动捡糖果","Toggle",false, function(Value)
    CandyCornFarm = Value
    while CandyCornFarm do
    for i, v in pairs(workspace.CandyCorns:GetChildren()) do
                    if v:FindFirstChildWhichIsA("TouchTransmitter") then
    v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                    end
                end
    task.wait()
    end
    end)
    
    BZMNQ:Toggle("获取炼金术师材料","Toggle", false, function(Value)
    AlchemistIngredients = Value
    if game.Players.LocalPlayer.leaderstats.Glove.Value == "Alchemist" then
    while AlchemistIngredients do
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Mushroom")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Glowing Mushroom")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Fire Flower")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Winter Rose")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Dark Root")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Dire Flower")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Autumn Sprout")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Elder Wood")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Hazel Lily")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Wild Vine")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Jade Stone")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Lamp Grass")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Plane Flower")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Blood Rose")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Red Crystal")
    game.ReplicatedStorage.AlchemistEvent:FireServer("AddItem","Blue Crystal")
    task.wait()
    end
    end
    end)
    
    BZMNQ:Toggle("自动加入竞技场","Toggle", false, function(Value)
    AutoEnterArena = Value
    while AutoEnterArena do
    if game.Players.LocalPlayer.Character:FindFirstChild("entered") == nil and game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport1, 0)
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport1, 1)
        end
    task.wait()
    end
    end)
    
    BZMNQ:Toggle("自动光波球","Toggle", false, function(Value)
    if Person == nil then
    Person = game.Players.LocalPlayer.Name
    end
    _G.RojoSpam = Value
    while _G.RojoSpam do
    game:GetService("ReplicatedStorage"):WaitForChild("RojoAbility"):FireServer("Release", {game.Players[Person].Character.HumanoidRootPart.CFrame})
    task.wait()
    end
    end)
    
    BZMNQ:Button("Rojo技能", function(Value)
    _G.RojoSpam = Value
    game:GetService("ReplicatedStorage"):WaitForChild("RojoAbility"):FireServer("Charge")
    wait(6)
    game:GetService("ReplicatedStorage"):WaitForChild("RojoAbility"):FireServer("Release", {game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame})
    task.wait()
    end)
    
    BZMNQ:Toggle("音符技能","Toggle", false, function(Value)
    _G.RhythmSpam = Value
    while _G.RhythmSpam do
    game:GetService("ReplicatedStorage").rhythmevent:FireServer("AoeExplosion",0)
    task.wait()
    end
    end)
    
    BZMNQ:Toggle("Null技能","Toggle", false, function(Value)
    NullSpam = Value
    while NullSpam do
    game:GetService("ReplicatedStorage").NullAbility:FireServer()
    task.wait()
    end
    end)
    
    BZMNQZX:Toggle("自动拾取黄金果实","Toggle", false, function(Value)
    SlappleFarm = Value
    while SlappleFarm do
    for i, v in ipairs(workspace.Arena.island5.Slapples:GetDescendants()) do
                    if game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") and game.Players.LocalPlayer.Character:FindFirstChild("entered") and v.Name == "Glove" and v:FindFirstChildWhichIsA("TouchTransmitter") then
                        firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v, 0)
            firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v, 1)
                    end
                end
    task.wait()
    end
    end)
    
    BZMNQZX:Toggle("自动捡飞行宝珠","Toggle", false, function(Value)
    Jetfarm = Value
    while Jetfarm do
    for i,v in pairs(game.Workspace:GetChildren()) do
                        if v.Name == "JetOrb" and v:FindFirstChild("TouchInterest") then
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), v, 0)
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), v, 1)
                        end
                    end
    task.wait()
    end
    end)
    
    BZMNQZX:Toggle("自动捡相位球","Toggle", false, function(Value)
    Phasefarm = Value
    while Phasefarm do
    for i,v in pairs(game.Workspace:GetChildren()) do
                        if v.Name == "PhaseOrb" and v:FindFirstChild("TouchInterest") then
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), v, 0)
    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), v, 1)
                        end
                    end
    task.wait()
    end
    end)
    
    BZMNQZX:Toggle("自动刷bob","Toggle", false, function(Value)
    ReplicaFarm = Value
    while ReplicaFarm do
    for i, v in pairs(workspace:GetChildren()) do
                    if v.Name:match(game.Players.LocalPlayer.Name) and v:FindFirstChild("HumanoidRootPart") then
    game.ReplicatedStorage.b:FireServer(v:WaitForChild("HumanoidRootPart"))
                    end
                end
    task.wait()
    game:GetService("ReplicatedStorage").Duplicate:FireServer()
    task.wait(7)
    end
    end)
    
    BZMNQZX:Toggle("无限反转","Toggle", false, function(Value)
    _G.InfReverse = Value
    while _G.InfReverse do
    game:GetService("ReplicatedStorage").ReverseAbility:FireServer()
    wait(6)
    end
    end)
    
    BZMNQZX:Toggle("彩虹角色(装备黄金手套)","Toggle", false, function(Value)
    _G.Rainbow = Value
    while _G.Rainbow do
    for i = 0,1,0.001*25 do
    game:GetService("ReplicatedStorage").Goldify:FireServer(false, BrickColor.new(Color3.fromHSV(i,1,1)))
    task.wait()
    end
    end
    end)
    
    BZMNQFJN:Toggle("防击飞","Toggle", false, function(Value)
    AntiRagdoll = Value
    if AntiRagdoll then
    game.Players.LocalPlayer.Character.Humanoid.Health = 0
    game.Players.LocalPlayer.CharacterAdded:Connect(function()
    game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Changed:Connect(function()
    if game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Value == true and AntiRagdoll then
    repeat task.wait() game.Players.LocalPlayer.Character.Torso.Anchored = true
    until game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Value == false
    game.Players.LocalPlayer.Character.Torso.Anchored = false
    end
    end)
    end)
    end
    end)
    
    BZMNQFJN:Toggle("反虚空(锦标赛也有效果)","Toggle", false, function(Value)
    game.Workspace.dedBarrier.CanCollide = Value
    game.Workspace.TAntiVoid.CanCollide = Value
    end)
    
    BZMNQFJN:Toggle("防死亡屏障","Toggle", false, function(Value)
    if Value == true then
    for i,v in pairs(game.Workspace.DEATHBARRIER:GetChildren()) do
                        if v.ClassName == "Part" and v.Name == "BLOCK" then
                            v.CanTouch = false
                        end
                    end
    workspace.DEATHBARRIER.CanTouch = false
    workspace.DEATHBARRIER2.CanTouch = false
    workspace.dedBarrier.CanTouch = false
    workspace.ArenaBarrier.CanTouch = false
    workspace.AntiDefaultArena.CanTouch = false
    else
    for i,v in pairs(game.Workspace.DEATHBARRIER:GetChildren()) do
                        if v.ClassName == "Part" and v.Name == "BLOCK" then
                            v.CanTouch = true
                        end
                    end
    workspace.DEATHBARRIER.CanTouch = true
    workspace.DEATHBARRIER2.CanTouch = true
    workspace.dedBarrier.CanTouch = true
    workspace.ArenaBarrier.CanTouch = true
    workspace.AntiDefaultArena.CanTouch = true
    end
    end)
    
    BZMNQFJN:Toggle("反巴西","Toggle", false, function(Value)
    if Value == true then
    for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                            v.CanTouch = false
                    end
    else
    for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                            v.CanTouch = true
                    end
    end
    end)
    
    BZMNQFJN:Toggle("反死亡方块","Toggle", false, function(Value)
    if Value == true then
            workspace.Arena.CubeOfDeathArea["the cube of death(i heard it kills)"].CanTouch = false
            else
                    workspace.Arena.CubeOfDeathArea["the cube of death(i heard it kills)"].CanTouch = true
            end
    end)
    
    BZMNQFJN:Toggle("反上帝技能","Toggle", false, function(Value)
    AntiTimestop = Value
    while AntiTimestop do
                    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                        if v.ClassName == "Part" then
                            v.Anchored = false
                        end
                    end
    task.wait()
    end
    end)
    
    BZMNQFJN:Toggle("反鱿鱼","Toggle", false, function(Value)
    AntiSquid = Value
    if AntiSquid == false then
            game.Players.LocalPlayer.PlayerGui.SquidInk.Enabled = true
            end
    while AntiSquid do
    if game.Players.LocalPlayer.PlayerGui:FindFirstChild("SquidInk") then
            game.Players.LocalPlayer.PlayerGui.SquidInk.Enabled = false
    end
    task.wait()
    end
    end)
    
    BZMNQFJN:Toggle("反神圣杰克","Toggle", false, function(Value)
    game.Players.LocalPlayer.PlayerScripts.HallowJackAbilities.Disabled = Value
    end)
    
    BZMNQFJN:Toggle("反传送带","Toggle", false, function(Value)
    game.Players.LocalPlayer.PlayerScripts.ConveyorVictimized.Disabled = Value
    end)
    
    BZMNQFJN:Toggle("反板砖","Toggle", false, function(Value)
    AntiBrick = Value
    while AntiBrick do
    for i,v in pairs(game.Workspace:GetChildren()) do
                        if v.Name == "Union" then
                            v.CanTouch = false
                        end
                    end
    task.wait()
    end
    end)
    
    BZMNQFJN:Toggle("反Null","Toggle", false, function(Value)
    AntiNull = Value
    while AntiNull do
    for i,v in pairs(game.Workspace:GetChildren()) do
                        if v.Name == "Imp" and v:FindFirstChild("Body") then
    shared.gloveHits[game.Players.LocalPlayer.leaderstats.Glove.Value]:FireServer(v.Body,true)
    end
    end
    task.wait()
    end
    end)
    
    
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------      
    CJ:Button("传送到开始区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(85.86943817138672, 11.751949310302734, -198.07127380371094)
    end)
    
    CJ:Button("传送到健身区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(93.60747528076172, 11.751947402954102, -10.266206741333008)
    end)
    
    CJ:Button("传送到食物区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(78.86384582519531, 11.751947402954102, 228.9690399169922)
    end)
    
    CJ:Button("传送到街机区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(88.99887084960938, 11.751949310302734, 502.90997314453125)
    end)
    
    CJ:Button("传送到农场区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(85.6707763671875, 11.751947402954102, 788.5997314453125)
    end)
    
    CJ:Button("传送到城堡区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(84.87281036376953, 11.84177017211914, 1139.7509765625)
    end)
    
    CJ:Button("传送到蒸汽朋克区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(92.63227081298828, 11.841767311096191, 1692.7890625)
    end)
    
    CJ:Button("传送到迪斯科区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(98.69613647460938, 16.015085220336914, 2505.213134765625)
    end)
    
    CJ:Button("传送到太空区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(88.42948150634766, 11.841769218444824, 3425.941650390625)
    end)
    
    CJ:Button("传送到糖果区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(63.55805969238281, 11.841663360595703, 4340.69921875)
    end)
    
    CJ:Button("送到实验室区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(78.00920867919922, 11.841663360595703, 5226.60205078125)
    end)
    
    CJ:Button("传送到热带区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(80.26090240478516, 12.0902681350708, 6016.16552734375)
    end)
    
    CJ:Button("传送到恐龙区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(38.4753303527832, 25.801530838012695, 6937.779296875)
    end)
    
    CJ:Button("传送到复古区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(99.81867218017578, 12.89099407196045, 7901.74755859375)
    end)
    
    CJ:Button("传送到冬季区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(63.47243881225586, 11.841662406921387, 8983.810546875)
    end)
    
    CJ:Button("传送到深海区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(105.36250305175781, 26.44820213317871, 9970.0849609375)
    end)
    
    CJ:Button("传送到狂野西部区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(68.69414520263672, 15.108586311340332, 10938.654296875)
    end)
    
    CJ:Button("传送到豪华公寓区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(86.75145721435547, 11.313281059265137, 12130.349609375)
    end)
    
    CJ:Button("传送到宝剑战斗区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(111.25597381591797, 11.408829689025879, 12945.57421875)
    end)
    
    CJ:Button("传送到童话区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(121.14932250976562, 11.313281059265137, 14034.50390625)
    end)
    
    CJ:Button("传送到桃花区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(108.2142333984375, 11.813281059265137, 15131.861328125)
    end)
    
    CJ:Button("传送到厨房区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.78338623046875, 21.76291847229004, 16204.9755859375)
    end)
    
    CJ:Button("传送到下水道区域", function()
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(47.36086654663086, 12.25178050994873, 17656.04296875)
    end)
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------                                                                                                                                                                                                                                                                                                                            
    
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    music:Button("防空警报", function()
    local sound = Instance.new("Sound")
    sound.SoundId = "rbxassetid://792323017"
    sound.Parent = game.Workspace
    sound:Play()
    end)
    
    music:Button("义勇军进行曲", function()
    local sound = Instance.new("Sound")
    sound.SoundId = "rbxassetid://1845918434"
    sound.Parent = game.Workspace
    sound:Play()
    end)
    
    music:Button("彩虹瀑布",function()
    local sound = Instance.new("Sound")
    sound.SoundId = "rbxassetid://1837879082"
    sound.Parent = game.Workspace
    sound:Play()
    end)
    end
        
        
        
        
        
        
        
        