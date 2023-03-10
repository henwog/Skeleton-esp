--// Skeleton ESP \\--
  
  local SkeletonColor = Color3.fromRGB(225, 225, 225) -- put your color changer stuff here
  local Skeletons = nil
  
  PlayerESPTab:AddToggle('MyToggle', {
  Text = 'Skeleton',
  Default = false, -- Default value (true / false)
  Tooltip = 'On / Off', -- Information shown when you hover over the toggle
  }):AddColorPicker('SkeletonColor', {
  Default = Color3.new(0, 1, 0),
  Title = 'Color',
  })
  Options.SkeletonColor:OnChanged(function(Color)
  SkeletonColor = Color
  end)
  
  local camera = workspace.CurrentCamera
  local function DrawDrop(drop)
  
  local DropText = Drawing.new("Line")
  DropText.Visible = false
  DropText.From = Vector2.new(0, 0)
  DropText.To = Vector2.new(200, 200)
  DropText.Color = SkeletonColor
  DropText.Thickness = 1
  local DropText1 = Drawing.new("Line")
  DropText1.Visible = false
  DropText1.From = Vector2.new(0, 0)
  DropText1.To = Vector2.new(0, 0)
  DropText1.Color = SkeletonColor
  DropText1.Thickness = 1
  local DropText2 = Drawing.new("Line")
  DropText2.Visible = false
  DropText2.From = Vector2.new(0, 0)
  DropText2.To = Vector2.new(0, 0)
  DropText2.Color = SkeletonColor
  DropText2.Thickness = 1
  local DropText3 = Drawing.new("Line")
  DropText3.Visible = false
  DropText3.From = Vector2.new(0, 0)
  DropText3.To = Vector2.new(0, 0)
  DropText3.Color = SkeletonColor
  DropText3.Thickness = 1
  local DropText4 = Drawing.new("Line")
  DropText4.Visible = false
  DropText4.From = Vector2.new(0, 0)
  DropText4.To = Vector2.new(0, 0)
  DropText4.Color = SkeletonColor
  DropText4.Thickness = 1
  local DropText5 = Drawing.new("Line")
  DropText5.Visible = false
  DropText5.From = Vector2.new(0, 0)
  DropText5.To = Vector2.new(0, 0)
  DropText5.Color = SkeletonColor
  DropText5.Thickness = 1
  local DropText6 = Drawing.new("Line")
  DropText6.Visible = false
  DropText6.From = Vector2.new(0, 0)
  DropText6.To = Vector2.new(0, 0)
  DropText6.Color = SkeletonColor
  DropText6.Thickness = 1
  local DropText7 = Drawing.new("Line")
  DropText7.Visible = false
  DropText7.From = Vector2.new(0, 0)
  DropText7.To = Vector2.new(0, 0)
  DropText7.Color = SkeletonColor
  DropText7.Thickness = 1
  local DropText8 = Drawing.new("Line")
  DropText8.Visible = false
  DropText8.From = Vector2.new(0, 0)
  DropText8.To = Vector2.new(0, 0)
  DropText8.Color = SkeletonColor
  DropText8.Thickness = 1
  local DropText9 = Drawing.new("Line")
  DropText9.Visible = false
  DropText9.From = Vector2.new(0, 0)
  DropText9.To = Vector2.new(0, 0)
  DropText9.Color = SkeletonColor
  DropText9.Thickness = 1
  local DropText10 = Drawing.new("Line")
  DropText10.Visible = false
  DropText10.From = Vector2.new(0, 0)
  DropText10.To = Vector2.new(0, 0)
  DropText10.Color = SkeletonColor
  DropText10.Thickness = 1
  local DropText11 = Drawing.new("Line")
  DropText11.Visible = false
  DropText11.From = Vector2.new(0, 0)
  DropText11.To = Vector2.new(0, 0)
  DropText11.Color = SkeletonColor
  DropText11.Thickness = 1
  local DropText12 = Drawing.new("Line")
  DropText12.Visible = false
  DropText12.From = Vector2.new(0, 0)
  DropText12.To = Vector2.new(0, 0)
  DropText12.Color = SkeletonColor
  DropText12.Thickness = 1
  
  local function UPDATER()
  local c
  c = game:GetService("RunService").RenderStepped:Connect(function()
  if drop and workspace:FindFirstChild(drop.Name) and drop:FindFirstChild("Head") and drop:FindFirstChild("RightFoot") then
    local dropvector, onscreen = camera:WorldToViewportPoint(drop.Head.Position)
    local dropvector1, onscreen = camera:WorldToViewportPoint(drop.LowerTorso.Position)
    local dropvector2, onscreen = camera:WorldToViewportPoint(drop.UpperTorso.Position)
    local dropvector3, onscreen = camera:WorldToViewportPoint(drop.LeftUpperArm.Position)
    local dropvector4, onscreen = camera:WorldToViewportPoint(drop.LeftLowerArm.Position)
    local dropvector5, onscreen = camera:WorldToViewportPoint(drop.LeftHand.Position)
    local dropvector6, onscreen = camera:WorldToViewportPoint(drop.RightUpperArm.Position)
    local dropvector7, onscreen = camera:WorldToViewportPoint(drop.RightLowerArm.Position)
    local dropvector8, onscreen = camera:WorldToViewportPoint(drop.RightHand.Position)
    local dropvector9, onscreen = camera:WorldToViewportPoint(drop.LeftUpperLeg.Position)
    local dropvector10, onscreen = camera:WorldToViewportPoint(drop.LeftLowerLeg.Position)
    local dropvector11, onscreen = camera:WorldToViewportPoint(drop.LeftFoot.Position)
    local dropvector12, onscreen = camera:WorldToViewportPoint(drop.RightUpperLeg.Position)
    local dropvector13, onscreen = camera:WorldToViewportPoint(drop.RightLowerLeg.Position)
    local dropvector14, onscreen = camera:WorldToViewportPoint(drop.RightFoot.Position)
    local distance = (game.Workspace.Ignore.LocalCharacter.Middle.Position - drop.Head.Position).magnitude
    if Toggles.MyToggle.Value and onscreen and Options.Esp_Distancce.Value > distance then -- put ur toggle thing in here
      DropText.From = Vector2.new(dropvector.X, dropvector.Y)
      DropText.To = Vector2.new(dropvector1.X, dropvector1.Y)
      DropText.Color = SkeletonColor
      DropText.Visible = true
      DropText1.From = Vector2.new(dropvector2.X, dropvector2.Y)
      DropText1.To = Vector2.new(dropvector3.X, dropvector3.Y)
      DropText1.Color = SkeletonColor
      DropText1.Visible = true
      DropText2.From = Vector2.new(dropvector3.X, dropvector3.Y)
      DropText2.To = Vector2.new(dropvector4.X, dropvector4.Y)
      DropText2.Color = SkeletonColor
      DropText2.Visible = true
      DropText3.From = Vector2.new(dropvector4.X, dropvector4.Y)
      DropText3.To = Vector2.new(dropvector5.X, dropvector5.Y)
      DropText3.Color = SkeletonColor
      DropText3.Visible = true
      DropText4.From = Vector2.new(dropvector2.X, dropvector2.Y)
      DropText4.To = Vector2.new(dropvector6.X, dropvector6.Y)
      DropText4.Color = SkeletonColor
      DropText4.Visible = true
      DropText5.From = Vector2.new(dropvector6.X, dropvector6.Y)
      DropText5.To = Vector2.new(dropvector7.X, dropvector7.Y)
      DropText5.Color = SkeletonColor
      DropText5.Visible = true
      DropText6.From = Vector2.new(dropvector7.X, dropvector7.Y)
      DropText6.To = Vector2.new(dropvector8.X, dropvector8.Y)
      DropText6.Color = SkeletonColor
      DropText6.Visible = true
      DropText7.From = Vector2.new(dropvector1.X, dropvector1.Y)
      DropText7.To = Vector2.new(dropvector9.X, dropvector9.Y)
      DropText7.Color = SkeletonColor
      DropText7.Visible = true
      DropText8.From = Vector2.new(dropvector9.X, dropvector9.Y)
      DropText8.To = Vector2.new(dropvector10.X, dropvector10.Y)
      DropText8.Color = SkeletonColor
      DropText8.Visible = true
      DropText9.From = Vector2.new(dropvector10.X, dropvector10.Y)
      DropText9.To = Vector2.new(dropvector11.X, dropvector11.Y)
      DropText9.Color = SkeletonColor
      DropText9.Visible = true
      DropText10.From = Vector2.new(dropvector1.X, dropvector1.Y)
      DropText10.To = Vector2.new(dropvector12.X, dropvector12.Y)
      DropText10.Color = SkeletonColor
      DropText10.Visible = true
      DropText11.From = Vector2.new(dropvector12.X, dropvector12.Y)
      DropText11.To = Vector2.new(dropvector13.X, dropvector13.Y)
      DropText11.Color = SkeletonColor
      DropText11.Visible = true
      DropText12.From = Vector2.new(dropvector13.X, dropvector13.Y)
      DropText12.To = Vector2.new(dropvector14.X, dropvector14.Y)
      DropText12.Color = SkeletonColor
      DropText12.Visible = true
    else
      DropText.Visible = false
      DropText1.Visible = false
      DropText2.Visible = false
      DropText3.Visible = false
      DropText4.Visible = false
      DropText5.Visible = false
      DropText6.Visible = false
      DropText7.Visible = false
      DropText8.Visible = false
      DropText9.Visible = false
      DropText10.Visible = false
      DropText11.Visible = false
      DropText12.Visible = false
    end
  else
    if game:GetService("Workspace"):FindFirstChild(drop.Name) == nil then
      c:Disconnect()
    end
    DropText.Visible = false
    DropText1.Visible = false
    DropText2.Visible = false
    DropText3.Visible = false
    DropText4.Visible = false
    DropText5.Visible = false
    DropText6.Visible = false
    DropText7.Visible = false
    DropText8.Visible = false
    DropText9.Visible = false
    DropText10.Visible = false
    DropText11.Visible = false
    DropText12.Visible = false
  end
  end)
  end
  coroutine.wrap(UPDATER)()
  end
  for i,drop in pairs(workspace:GetChildren()) do
  if drop:FindFirstChild("Head") and drop:FindFirstChild("RightFoot") then
  coroutine.wrap(DrawDrop)(drop)
  end
  end
  
  workspace.ChildAdded:Connect(function(drop)
  if drop:FindFirstChild("Head") and drop:FindFirstChild("RightFoot") then
  coroutine.wrap(DrawDrop)(drop)
  end
  end)
  