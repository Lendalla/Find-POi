-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame1 = Instance.new("Frame")
local Frame2 = Instance.new("Frame")
local TextBox = Instance.new("TextBox")
local Inject = Instance.new("TextButton")
local Find = Instance.new("TextButton")
local Copy = Instance.new("TextButton")
local TextLabel1 = Instance.new("TextLabel")
local Frame3 = Instance.new("Frame")
local Clear = Instance.new("TextButton")
local close = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.Workspace
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame1.Name = "Frame1"
Frame1.Parent = ScreenGui
Frame1.BackgroundColor3 = Color3.fromRGB(39, 39, 39)
Frame1.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame1.BorderSizePixel = 0
Frame1.Position = UDim2.new(0.303076118, 0, 0.045031134, 0)
Frame1.Size = UDim2.new(0, 288, 0, 327)
Frame1.ZIndex = 0
Frame1.Style = Enum.FrameStyle.DropShadow

Frame2.Name = "Frame2"
Frame2.Parent = ScreenGui
Frame2.BackgroundColor3 = Color3.fromRGB(66, 66, 66)
Frame2.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame2.BorderSizePixel = 0
Frame2.Position = UDim2.new(0.322822809, 0, 0.085561499, 0)
Frame2.Size = UDim2.new(0, 265, 0, 296)

TextBox.Parent = ScreenGui
TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextBox.BackgroundTransparency = 1.000
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BorderSizePixel = 0
TextBox.Position = UDim2.new(0.362568527, 0, 0.384712189, 0)
TextBox.Size = UDim2.new(0, 201, 0, 36)
TextBox.Font = Enum.Font.Unknown
TextBox.PlaceholderColor3 = Color3.fromRGB(214, 214, 214)
TextBox.Text = ""
TextBox.TextColor3 = Color3.fromRGB(0, 0, 0)
TextBox.TextScaled = true
TextBox.TextSize = 23.000
TextBox.TextWrapped = true

Inject.Name = "Inject"
Inject.Parent = ScreenGui
Inject.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Inject.BorderColor3 = Color3.fromRGB(0, 0, 0)
Inject.BorderSizePixel = 0
Inject.Position = UDim2.new(0.623123109, 0, 0.628971338, 0)
Inject.Size = UDim2.new(0, 65, 0, 41)
Inject.Style = Enum.ButtonStyle.RobloxRoundButton
Inject.Font = Enum.Font.Jura
Inject.Text = "INJECT"
Inject.TextColor3 = Color3.fromRGB(0, 0, 0)
Inject.TextScaled = true
Inject.TextSize = 14.000
Inject.TextWrapped = true

Find.Name = "Find"
Find.Parent = ScreenGui
Find.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Find.BorderColor3 = Color3.fromRGB(0, 0, 0)
Find.BorderSizePixel = 0
Find.Position = UDim2.new(0.336336344, 0, 0.628971338, 0)
Find.Size = UDim2.new(0, 65, 0, 41)
Find.Style = Enum.ButtonStyle.RobloxRoundButton
Find.Font = Enum.Font.Jura
Find.Text = "FIND"
Find.TextColor3 = Color3.fromRGB(0, 0, 0)
Find.TextScaled = true
Find.TextSize = 14.000
Find.TextWrapped = true

Copy.Name = "Copy"
Copy.Parent = ScreenGui
Copy.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Copy.BorderColor3 = Color3.fromRGB(0, 0, 0)
Copy.BorderSizePixel = 0
Copy.Position = UDim2.new(0.433933944, 0, 0.628971338, 0)
Copy.Size = UDim2.new(0, 65, 0, 41)
Copy.Style = Enum.ButtonStyle.RobloxRoundButton
Copy.Font = Enum.Font.Jura
Copy.Text = "COPY"
Copy.TextColor3 = Color3.fromRGB(0, 0, 0)
Copy.TextScaled = true
Copy.TextSize = 14.000
Copy.TextWrapped = true

TextLabel1.Name = "TextLabel1"
TextLabel1.Parent = ScreenGui
TextLabel1.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel1.BackgroundTransparency = 1.000
TextLabel1.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel1.BorderSizePixel = 0
TextLabel1.Position = UDim2.new(0.322822809, 0, 0.085561499, 0)
TextLabel1.Size = UDim2.new(0, 200, 0, 50)
TextLabel1.Font = Enum.Font.SciFi
TextLabel1.LineHeight = 3.000
TextLabel1.Text = "แมว HUBx"
TextLabel1.TextColor3 = Color3.fromRGB(195, 195, 195)
TextLabel1.TextScaled = true
TextLabel1.TextSize = 45.000
TextLabel1.TextTransparency = 0.690
TextLabel1.TextWrapped = true

Frame3.Name = "Frame3"
Frame3.Parent = ScreenGui
Frame3.BackgroundColor3 = Color3.fromRGB(120, 120, 120)
Frame3.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame3.BorderSizePixel = 0
Frame3.Position = UDim2.new(0.337661147, 0, 0.279018462, 0)
Frame3.Size = UDim2.new(0, 243, 0, 131)
Frame3.Style = Enum.FrameStyle.DropShadow

Clear.Name = "Clear"
Clear.Parent = ScreenGui
Clear.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Clear.BorderColor3 = Color3.fromRGB(0, 0, 0)
Clear.BorderSizePixel = 0
Clear.Position = UDim2.new(0.379879892, 0, 0.738597035, 0)
Clear.Size = UDim2.new(0, 65, 0, 41)
Clear.Style = Enum.ButtonStyle.RobloxRoundButton
Clear.Font = Enum.Font.Jura
Clear.Text = "CLEAR"
Clear.TextColor3 = Color3.fromRGB(0, 0, 0)
Clear.TextScaled = true
Clear.TextSize = 14.000
Clear.TextWrapped = true

close.Name = "close"
close.Parent = ScreenGui
close.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
close.BorderColor3 = Color3.fromRGB(0, 0, 0)
close.BorderSizePixel = 0
close.Position = UDim2.new(0.659159184, 0, 0.0648002028, 0)
close.Size = UDim2.new(0, 41, 0, 33)
close.Style = Enum.ButtonStyle.RobloxRoundButton
close.Font = Enum.Font.Jura
close.Text = "X"
close.TextColor3 = Color3.fromRGB(255, 255, 255)
close.TextSize = 34.000
close.TextWrapped = true
