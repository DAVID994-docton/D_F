--[[
  Script Hack Blox Fruits | D_F BY DAVID E FRANCISCO
  Fonte: LOCAL COMPLETO
  Mobile-Friendly | Seguro | Atualizável manualmente
]]

-- Serviços
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local TeleportService = game:GetService("TeleportService")
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()

-- Proteções iniciais
pcall(function()
    hookfunction(getrawmetatable(game).__namecall, newcclosure(function(...) return end))
end)

-- Criar GUI Principal
local ScreenGui = Instance.new("ScreenGui", game.CoreGui)
ScreenGui.Name = "DF_HACK_GUI"
ScreenGui.ResetOnSpawn = false

local MainFrame = Instance.new("Frame", ScreenGui)
MainFrame.Size = UDim2.new(0, 400, 0, 500)
MainFrame.Position = UDim2.new(0.5, -200, 0.5, -250)
MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
MainFrame.BorderSizePixel = 0
MainFrame.Active = true
MainFrame.Draggable = true

-- Título
local Title = Instance.new("TextLabel", MainFrame)
Title.Size = UDim2.new(1, 0, 0, 40)
Title.BackgroundTransparency = 1
Title.Text = "D_F BY DAVID E FRANCISCO"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 24

-- ScrollingArea
local Scroll = Instance.new("ScrollingFrame", MainFrame)
Scroll.Size = UDim2.new(1, 0, 1, -40)
Scroll.Position = UDim2.new(0, 0, 0, 40)
Scroll.CanvasSize = UDim2.new(0, 0, 5, 0)
Scroll.ScrollBarThickness = 6
Scroll.BackgroundTransparency = 1

-- Layout para botões
local UIListLayout = Instance.new("UIListLayout", Scroll)
UIListLayout.Padding = UDim.new(0, 5)
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder

-- Função utilitária para criar botões
local function CreateButton(text, callback)
    local Button = Instance.new("TextButton", Scroll)
    Button.Size = UDim2.new(1, -10, 0, 40)
    Button.Position = UDim2.new(0, 5, 0, 0)
    Button.Text = text
    Button.Font = Enum.Font.SourceSansBold
    Button.TextSize = 18
    Button.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    Button.TextColor3 = Color3.fromRGB(255, 255, 255)
    Button.BorderSizePixel = 0
    Button.MouseButton1Click:Connect(callback)
end

-- Exemplo de botão
CreateButton("Auto Farm Level", function()
    print("Ativando Auto Farm Level...")
    -- código real aqui depois
end)

CreateButton("Auto Farm Boss", function()
    print("Ativando Auto Farm Boss...")
end)

CreateButton("Fly Hack", function()
    print("Ativando Fly Hack...")
end)

CreateButton("Aimbot PvP", function()
    print("Ativando Aimbot...")
end)

CreateButton("ESP Frutas", function()
    print("Ativando Fruit ESP...")
end)

CreateButton("Teleport Ilhas", function()
    print("Abrindo menu de teleport...")
end)


-- Auto Click (delay de 0.001s)
local autoClicking = false
local clickConnection = nil

CreateButton("Auto Click (0.001s)", function()
    autoClicking = not autoClicking
    if autoClicking then
        print("Auto Click ON")
        clickConnection = RunService.RenderStepped:Connect(function()
            pcall(function()
                if LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Tool") then
                    local tool = LocalPlayer.Character:FindFirstChildOfClass("Tool")
                    tool:Activate()
                end
            end)
            wait(0.001)
        end)
    else
        print("Auto Click OFF")
        if clickConnection then
            clickConnection:Disconnect()
        end
    end
end)


-- Botão para ocultar/mostrar menu
local ToggleButton = Instance.new("TextButton", ScreenGui)
ToggleButton.Size = UDim2.new(0, 100, 0, 30)
ToggleButton.Position = UDim2.new(0, 10, 0.5, -15)
ToggleButton.Text = "Mostrar/Esconder"
ToggleButton.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ToggleButton.BorderSizePixel = 0
ToggleButton.MouseButton1Click:Connect(function()
    MainFrame.Visible = not MainFrame.Visible
end)

print("[D_F] Menu carregado com sucesso.")
--[[
  Script Hack Blox Fruits | D_F BY DAVID E FRANCISCO
  Fonte: LOCAL COMPLETO
  Mobile-Friendly | Seguro | Atualizável manualmente
]]

-- Serviços
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local TeleportService = game:GetService("TeleportService")
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()

-- Proteções iniciais
pcall(function()
    hookfunction(getrawmetatable(game).__namecall, newcclosure(function(...) return end))
end)

-- Criar GUI Principal
local ScreenGui = Instance.new("ScreenGui", game.CoreGui)
ScreenGui.Name = "DF_HACK_GUI"
ScreenGui.ResetOnSpawn = false

local MainFrame = Instance.new("Frame", ScreenGui)
MainFrame.Size = UDim2.new(0, 400, 0, 500)
MainFrame.Position = UDim2.new(0.5, -200, 0.5, -250)
MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
MainFrame.BorderSizePixel = 0
MainFrame.Active = true
MainFrame.Draggable = true

-- Título
local Title = Instance.new("TextLabel", MainFrame)
Title.Size = UDim2.new(1, 0, 0, 40)
Title.BackgroundTransparency = 1
Title.Text = "D_F BY DAVID E FRANCISCO"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 24

-- ScrollingArea
local Scroll = Instance.new("ScrollingFrame", MainFrame)
Scroll.Size = UDim2.new(1, 0, 1, -40)
Scroll.Position = UDim2.new(0, 0, 0, 40)
Scroll.CanvasSize = UDim2.new(0, 0, 5, 0)
Scroll.ScrollBarThickness = 6
Scroll.BackgroundTransparency = 1

-- Layout para botões
local UIListLayout = Instance.new("UIListLayout", Scroll)
UIListLayout.Padding = UDim.new(0, 5)
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder

-- Função utilitária para criar botões
local function CreateButton(text, callback)
    local Button = Instance.new("TextButton", Scroll)
    Button.Size = UDim2.new(1, -10, 0, 40)
    Button.Position = UDim2.new(0, 5, 0, 0)
    Button.Text = text
    Button.Font = Enum.Font.SourceSansBold
    Button.TextSize = 18
    Button.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    Button.TextColor3 = Color3.fromRGB(255, 255, 255)
    Button.BorderSizePixel = 0
    Button.MouseButton1Click:Connect(callback)
end

-- Exemplo de botão
CreateButton("Auto Farm Level", function()
    print("Ativando Auto Farm Level...")
    -- código real aqui depois
end)

CreateButton("Auto Farm Boss", function()
    print("Ativando Auto Farm Boss...")
end)

CreateButton("Fly Hack", function()
    print("Ativando Fly Hack...")
end)

CreateButton("Aimbot PvP", function()
    print("Ativando Aimbot...")
end)

CreateButton("ESP Frutas", function()
    print("Ativando Fruit ESP...")
end)

CreateButton("Teleport Ilhas", function()
    print("Abrindo menu de teleport...")
end)


-- Auto Click (delay de 0.001s)
local autoClicking = false
local clickConnection = nil

CreateButton("Auto Click (0.001s)", function()
    autoClicking = not autoClicking
    if autoClicking then
        print("Auto Click ON")
        clickConnection = RunService.RenderStepped:Connect(function()
            pcall(function()
                if LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Tool") then
                    local tool = LocalPlayer.Character:FindFirstChildOfClass("Tool")
                    tool:Activate()
                end
            end)
            wait(0.001)
        end)
    else
        print("Auto Click OFF")
        if clickConnection then
            clickConnection:Disconnect()
        end
    end
end)


-- Botão para ocultar/mostrar menu
local ToggleButton = Instance.new("TextButton", ScreenGui)
ToggleButton.Size = UDim2.new(0, 100, 0, 30)
ToggleButton.Position = UDim2.new(0, 10, 0.5, -15)
ToggleButton.Text = "Mostrar/Esconder"
ToggleButton.BackgroundColor3 = Color3.fromRGB(0, 120, 255)
ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ToggleButton.BorderSizePixel = 0
ToggleButton.MouseButton1Click:Connect(function()
    MainFrame.Visible = not MainFrame.Visible
end)

print("[D_F] Menu carregado com sucesso.")
