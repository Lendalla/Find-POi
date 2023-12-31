-- สร้าง ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "MyScreenGui"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- ตรวจสอบว่ามี ScreenGui ซ้ำหรือไม่
for _, gui in pairs(game.Players.LocalPlayer.PlayerGui:GetChildren()) do
    if gui.Name == screenGui.Name and gui ~= screenGui then
        gui:Destroy()
    end
end

-- สร้าง Frame
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 700, 0, 200)
frame.BackgroundColor3 = Color3.fromRGB(128, 128, 128)
frame.BackgroundTransparency = 0.5
frame.Parent = screenGui

-- สร้าง TextBox
local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(1, 0, 0.8, 0)
textBox.BackgroundTransparency = 1
textBox.Parent = frame

-- สร้างปุ่ม padlojh
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
    -- เล่น animation ลดขนาดปุ่มชั่วคราว
    button:TweenSize(UDim2.new(0.9, 0, 0.18, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quad, 0.1, true, function()
        wait(0.1)
        button:TweenSize(UDim2.new(1, 0, 0.2, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quad, 0.1, true)
    end)
end)

-- สร้างปุ่มคัดลอกข้อความบน TextBox
local copyButton = Instance.new("TextButton")
copyButton.Size = UDim2.new(0, 30, 0, 30)
copyButton.Position = UDim2.new(1, -30, 0, 0)
copyButton.Text = "C"
copyButton.Parent = textBox

copyButton.MouseButton1Click:Connect(function()
    setclipboard(textBox.Text)
end)

-- สร้างปุ่มปิด ScreenGui
local closeButton = Instance.new("TextButton")
closeButton.Size = UDim2.new(0, 30, 0, 30)
closeButton.Position = UDim2.new(1, -30, 0, 0)
closeButton.Text = "X"
closeButton.Parent = screenGui

closeButton.MouseButton1Click:Connect(function()
    screenGui.Enabled = false
end)

-- กำหนดให้สามารถเปิดปิด ScreenGui ด้วย Ctrl
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.LeftControl then
        screenGui.Enabled = not screenGui.Enabled
    end
end)
