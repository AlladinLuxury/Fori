local placeId = game.PlaceId

local vu = game:GetService("VirtualUser")

local info = game.MarketplaceService:GetProductInfo(placeId)

local Ebun = game:GetService("ReplicatedStorage")

local Sasun = require(Ebun:WaitForChild("Constants"))

local coins = game.Players.LocalPlayer.PlayerGui.MainGui.CoinsContainer.Container.Amount

local coinValue = coins.Text

local ScreenGui = Instance.new("ScreenGui")

ScreenGui.Parent = game.CoreGui

local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/NDL9HYmx')))()

local Window = OrionLib:MakeWindow({Name = info.Name, HidePremium = false})

local Flower = Window:MakeTab({

	Name = "Flowers",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

local Avatar = Window:MakeTab({

	Name = "Avatar",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

local House = Window:MakeTab({

	Name = "House",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

local Misc = Window:MakeTab({

	Name = "Misc",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

Avatar:AddButton({

	Name = "Save Avatar" ,

	Callback = function()

game:GetService("ReplicatedStorage").Connection:InvokeServer(65, "Save")

    end

})

Flower:AddButton({

	Name = "🎁Claim Flower Coins" ,

	Callback = function()

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 1)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 2)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 3)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 4)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 5)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 6)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 7)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 8)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 9)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 10)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 11)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 12)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 13)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 14)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 15)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 16)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 17)

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(228, 18)

    end

})

Misc:AddButton({

	Name = "Money Gui" ,

	Callback = function()

local Frame = Instance.new("Frame")

Frame.BackgroundColor3 = Color3.new(0, 0, 0)

Frame.Position = UDim2.new(0, 0, 0, 0)

Frame.Size = UDim2.new(0.1, 0, 0.05, 0)

Frame.Parent = ScreenGui

Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

-- создаем текстовую метку (TextLabel) внутри панельки

local TextLabel = Instance.new("TextLabel")

TextLabel.BackgroundTransparency = 1

TextLabel.Position = UDim2.new(0, 10, 0, 5)

TextLabel.Size = UDim2.new(0.5, 0, 1, 0)

TextLabel.Font = Enum.Font.SourceSansBold

TextLabel.Text = ("Coins: " .. coinValue)

TextLabel.TextColor3 = Color3.new(255, 160, 30)

TextLabel.TextSize = 20

TextLabel.Parent = Frame

TextLabel.TextColor3 = Color3.fromRGB(255, 160, 30)

-- создаем функцию, которая будет обновлять значение монеток

local function updateCoins()

    local newCoinValue = coins.Text

    if newCoinValue ~= coinValue then

        coinValue = newCoinValue

        TextLabel.Text = ("Coins: " .. coinValue)

    end

end

-- подключаем функцию к событию изменения текста монеток

coins:GetPropertyChangedSignal("Text"):Connect(updateCoins)

end

})

Misc:AddButton({

	Name = "Anti Afk" ,

	Callback = function()

game:GetService("Players").LocalPlayer.Idled:connect(function() vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)

wait(1)

vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)

end)  

  end

})

Misc:AddButton({

  Name = "Fps Boost",

  Callback = function()

    local excludedFolders = {["Worlds"] = true, ["Terrain"] = true, ["xbxJIE7EHDAxdx"] = true, ["lastxbad"] = true, ["NariNzzo"] = true, ["Camera"] = true} -- Папки, которые нужно исключить из удаления

local directory = game.Workspace -- Путь до целевой папки

-- Функция удаления файла

local function deleteFile(file)

    if excludedFolders[file.Name] then -- Если это исключенная папка, то не удаляем ее

        return

    end

    file:Destroy()

end

-- Удаление всех файлов в целевой папке

for _, file in ipairs(directory:GetChildren()) do

    deleteFile(file)

end

-- Прослушивание события создания нового файла в папке

directory.ChildAdded:Connect(function(file)

    deleteFile(file)

end)

end

})

Flower:AddButton({

	Name = "🚿Flowers" ,

	Callback = function()

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 18)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 17)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 16)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 15)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 14)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 13)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 12)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 11)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 10)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 9)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 8)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 7)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 6)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 5)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 4)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 3)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 2)

game:GetService("ReplicatedStorage").Connection:InvokeServer(93, 1)

    end

})

House:AddButton({

	Name = "🏠Monochrome" ,

	Callback = function()

for lol=1, 10, 0.1 do

local a = 127

for x=127, 130, 3 do

a = x

game:GetService("ReplicatedStorage"):WaitForChild("Connection"):InvokeServer(44, a, 1, 21) 

end

local b = 127

for y=127, 130, 3 do

b = y

game:GetService("ReplicatedStorage"):WaitForChild("Connection"):InvokeServer(44, b, 2, 21)

end

local c = 127

for z=127, 130, 3 do

c = z

game:GetService("ReplicatedStorage"):WaitForChild("Connection"):InvokeServer(44, c, 3, 21)

end

end

    end

})

Avatar:AddButton({

	Name = "Custom Mode Off" ,

	Callback = function()

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(323, false)

    end

})

Avatar:AddButton({

	Name = "Custom Mode On" ,

	Callback = function()

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(323, true)

    end

})

local Fish = Window:MakeTab({

	Name = "Fishing",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})

Fish:AddButton({

	Name = "AutoFishing" ,

	Callback = function()

        while wait() do

game:GetService("ReplicatedStorage").ConnectionEvent:FireServer(10)

game:GetService("ReplicatedStorage").Connection:InvokeServer(49)

game:GetService("ReplicatedStorage").Connection:InvokeServer(50)

end

end

})

Fish:AddButton({

	Name = "AutoSell Fish" ,

	Callback = function()

while wait() do

game:GetService("ReplicatedStorage").Connection:InvokeServer(51)

end

    end

})

Fish:AddButton({

	Name = "Silent Aim Fish" ,

	Callback = function()

Sasun.STATS.FISHCastObjectMinDistanceToCatch = 99999

    end

})

House:AddButton({

	Name = "Open Slots Backyard's" ,

	Callback = function()

game:GetService("ReplicatedStorage"):WaitForChild("ConnectionEvent"):FireServer(285, 1, 1)

game:GetService("ReplicatedStorage"):WaitForChild("ConnectionEvent"):FireServer(285, 1, 2)

game:GetService("ReplicatedStorage"):WaitForChild("ConnectionEvent"):FireServer(285, 1, 3)

    end

})
