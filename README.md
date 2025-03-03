# IceHub                                                                                                                                                                                                                                                      -- Create ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "AdminExecutorGui"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create Border Frame
local borderFrame = Instance.new("Frame")
borderFrame.Name = "BorderFrame"
borderFrame.Size = UDim2.new(0.5, 0, 0.6, 0)
borderFrame.Position = UDim2.new(0.25, 0, 0.2, 0)
borderFrame.BackgroundColor3 = Color3.new(0, 0, 0) -- Black
borderFrame.BorderSizePixel = 1
borderFrame.BorderColor3 = Color3.new(0, 0, 0)
borderFrame.Parent = screenGui

-- Create Title Bar
local titleBar = Instance.new("TextLabel")
titleBar.Name = "TitleBar"
titleBar.Size = UDim2.new(1, 0, 0.1, 0)
titleBar.Position = UDim2.new(0, 0, 0, 0)
titleBar.Text = "Script Executor | (v1.0) y.t. - vinciGoRobloxFE"
titleBar.Font = Enum.Font.SourceSans
titleBar.TextSize = 20
titleBar.TextColor3 = Color3.new(1, 1, 1) -- White text
titleBar.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2) -- Dark gray
titleBar.TextXAlignment = Enum.TextXAlignment.Center
titleBar.Parent = borderFrame

-- Create "v1" Label (Top-Right Corner)
local versionLabel = Instance.new("TextLabel")
versionLabel.Name = "VersionLabel"
versionLabel.Size = UDim2.new(0.1, 0, 0.05, 0) -- Adjust size
versionLabel.Position = UDim2.new(0.9, -10, 0.05, 0) -- Top-right corner with padding
versionLabel.Text = "v1.0" -- Example text
versionLabel.Font = Enum.Font.SourceSans
versionLabel.TextSize = 18
versionLabel.TextColor3 = Color3.new(1, 1, 1) -- White text
versionLabel.BackgroundTransparency = 1 -- Transparent background
versionLabel.TextXAlignment = Enum.TextXAlignment.Right -- Align text to the right
versionLabel.Parent = screenGui -- Parent to ScreenGui, so it stays visible when GUI is hidden


-- Add "-" Button to Hide GUI
local minimizeButton = Instance.new("TextButton")
minimizeButton.Name = "MinimizeButton"
minimizeButton.Size = UDim2.new(0.1, 0, 1, 0) -- 10% width of the TitleBar
minimizeButton.Position = UDim2.new(0.9, -5, 0, 0) -- Right corner with 5px padding
minimizeButton.Text = "-"
minimizeButton.Font = Enum.Font.SourceSans
minimizeButton.TextSize = 18
minimizeButton.TextColor3 = Color3.new(1, 1, 1) -- White text
minimizeButton.BackgroundColor3 = Color3.new(0.3, 0.3, 0.3) -- Dark gray
minimizeButton.Parent = titleBar

-- Create TextBox
local textBox = Instance.new("TextBox")
textBox.Name = "ScriptInput"
textBox.Size = UDim2.new(0.9, 0, 0.6, 0)
textBox.Position = UDim2.new(0.05, 0, 0.15, 0)
textBox.Text = "-- nice guy: Vinci, ON TOP!! :3"
textBox.ClearTextOnFocus = false
textBox.Font = Enum.Font.SourceSans
textBox.TextSize = 18
textBox.TextColor3 = Color3.new(0, 0, 0)
textBox.BackgroundColor3 = Color3.new(1, 1, 1)
textBox.Parent = borderFrame

-- Create Execute Button
local executeButton = Instance.new("TextButton")
executeButton.Name = "ExecuteButton"
executeButton.Size = UDim2.new(0.4, 0, 0.1, 0)
executeButton.Position = UDim2.new(0.05, 0, 0.8, 0)
executeButton.Text = "Execute"
executeButton.Font = Enum.Font.SourceSans
executeButton.TextSize = 18
executeButton.TextColor3 = Color3.new(1, 1, 1)
executeButton.BackgroundColor3 = Color3.new(0, 0.6, 0)
executeButton.Parent = borderFrame

-- Create Clear Button
local clearButton = Instance.new("TextButton")
clearButton.Name = "ClearButton"
clearButton.Size = UDim2.new(0.4, 0, 0.1, 0)
clearButton.Position = UDim2.new(0.55, 0, 0.8, 0)
clearButton.Text = "Clear"
clearButton.Font = Enum.Font.SourceSans
clearButton.TextSize = 18
clearButton.TextColor3 = Color3.new(1, 1, 1)
clearButton.BackgroundColor3 = Color3.new(0.6, 0, 0)
clearButton.Parent = borderFrame

-- Create "Show" Button
local showButton = Instance.new("TextButton")
showButton.Name = "ShowButton"
showButton.Size = UDim2.new(0.15, 0, 0.05, 0)
showButton.Position = UDim2.new(0.4, 0, 0.05, 0) -- Initial position
showButton.Text = "Show (+)"
showButton.Font = Enum.Font.SourceSans
showButton.TextSize = 18
showButton.TextColor3 = Color3.new(1, 1, 1)
showButton.BackgroundColor3 = Color3.new(0.3, 0.3, 0.3)
showButton.Parent = screenGui
showButton.Visible = false -- Initially hidden

-- Minimize Functionality
