local screenGui = Instance.new("ScreenGui")
screenGui.Name = "MyScreenGui"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

for _, gui in pairs(game.Players.LocalPlayer.PlayerGui:GetChildren()) do
    if gui.Name == screenGui.Name and gui ~= screenGui then
        gui:Destroy()
    end
end

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 500, 0, 200)
frame.BackgroundColor3 = Color3.fromRGB(128, 128, 128)
frame.BackgroundTransparency = 0.5
frame.Parent = screenGui

local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(1, 0, 0.8, 0)
textBox.BackgroundTransparency = 1
textBox.Parent = frame

local button = Instance.new("TextButton")
button.Size = UDim2.new(1, 0, 0.2, 0)
button.Position = UDim2.new(0, 0, 0.8, 0)
button.Text = "padlojh"
button.Parent = frame

button.MouseButton1Click:Connect(function()
    local player = game.Players.LocalPlayer
    if player.Character then
        local cframe = player.Character:GetPrimaryPartCFrame()
        textBox.Text = tostring(cframe)
    end

    button:TweenSize(UDim2.new(0.9, 0, 0.18, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quad, 0.1, true, function()
        wait(0.1)
        button:TweenSize(UDim2.new(1, 0, 0.2, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quad, 0.1, true)
    end)
end)

local copyButton = Instance.new("TextButton")
copyButton.Size = UDim2.new(0, 30, 0, 30)
copyButton.Position = UDim2.new(1, -30, 0, 0)
copyButton.Text = "C"
copyButton.Parent = textBox

copyButton.MouseButton1Click:Connect(function()
    setclipboard(textBox.Text)
end)

local closeButton = Instance.new("TextButton")
closeButton.Size = UDim2.new(0, 30, 0, 30)
closeButton.Position = UDim2.new(1, -30, 0, 0)
closeButton.Text = "X"
closeButton.Parent = screenGui

closeButton.MouseButton1Click:Connect(function()
    screenGui.Enabled = false
end)

local copyButton = Instance.new("TextButton")
copyButton.Size = UDim2.new(0, 30, 0, 30)
copyButton.Position = UDim2.new(1, -30, 0, 0)
copyButton.Text = "C"
copyButton.Parent = textBox

copyButton.MouseButton1Click:Connect(function()
    setclipboard(textBox.Text)
end)


game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.LeftControl then
        screenGui.Enabled = not screenGui.Enabled
    end
end)



