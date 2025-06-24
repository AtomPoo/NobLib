local library = {}

function library:CreateGui(parameters)

    local Pages = {}
    local GuiFunctions = {}
    local UIElements = {}
    local ThemeColor = Color3.fromRGB(255, 255, 127)
    local OpenedPage = nil


    local AtomLib = Instance.new("ScreenGui")
    if get_hidden_gui or gethui then
        local hiddenUI = get_hidden_gui or gethui
        AtomLib.Parent = hiddenUI()
    else
        for i,v in pairs(game:GetChildren()) do
            if v:IsA("CoreGui") then
                AtomLib.Parent = v
            end
        end
    end


    local MainUI = Instance.new("Frame")
    local UICorner = Instance.new("UICorner")
    local DropShadowHolder = Instance.new("Frame")
    local DropShadow = Instance.new("ImageLabel")
    local LocationInfo = Instance.new("Frame")
    local Title = Instance.new("TextLabel")
    local Details = Instance.new("ImageLabel")
    local Version2 = Instance.new("TextLabel")
    local Details_2 = Instance.new("ImageLabel")
    local PageName = Instance.new("TextLabel")
    local TopBar = Instance.new("Frame")
    local ImageLabel = Instance.new("ImageLabel")
    local TitleName = Instance.new("TextLabel")
    local VersionTop = Instance.new("TextLabel")
    local DetailIgnore = Instance.new("Frame")
    local Navigations = Instance.new("Frame")
    local UICorner_2 = Instance.new("UICorner")
    local UIListLayout = Instance.new("UIListLayout")
    local GapIgnore = Instance.new("Frame")
    local DetailIgnore_2 = Instance.new("Frame")
    local DetailIgnore_3 = Instance.new("Frame")
    AtomLib.Name = "AtomLib"
    AtomLib.Parent = game.CoreGui
    AtomLib.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    AtomLib.ResetOnSpawn = false
    MainUI.Name = "MainUI"
    MainUI.AnchorPoint = Vector2.new(0.5,0.5)
    MainUI.Parent = AtomLib
    MainUI.BackgroundColor3 = Color3.fromRGB(8, 8, 8)
    MainUI.BorderColor3 = Color3.fromRGB(0, 0, 0)
    MainUI.BorderSizePixel = 0
    MainUI.Position = UDim2.new(0,0,0,0)
    MainUI.Size = UDim2.new(0, 613, 0, 370)
    UICorner.Parent = MainUI
    DropShadowHolder.Name = "DropShadowHolder"
    DropShadowHolder.Parent = MainUI
    DropShadowHolder.BackgroundTransparency = 1.000
    DropShadowHolder.BorderSizePixel = 0
    DropShadowHolder.Size = UDim2.new(1, 0, 1, 0)
    DropShadowHolder.ZIndex = 0
    DropShadow.Name = "DropShadow"
    DropShadow.Parent = DropShadowHolder
    DropShadow.AnchorPoint = Vector2.new(0.5, 0.5)
    DropShadow.BackgroundTransparency = 1.000
    DropShadow.BorderSizePixel = 0
    DropShadow.Position = UDim2.new(0.5, 0, 0.5, 0)
    DropShadow.Size = UDim2.new(1, 47, 1, 47)
    DropShadow.ZIndex = 0
    DropShadow.Image = "rbxassetid://6014261993"
    DropShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
    DropShadow.ImageTransparency = 0.500
    DropShadow.ScaleType = Enum.ScaleType.Slice
    DropShadow.SliceCenter = Rect.new(49, 49, 450, 450)
    LocationInfo.Name = "LocationInfo"
    LocationInfo.Parent = MainUI
    LocationInfo.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
    LocationInfo.BorderColor3 = Color3.fromRGB(0, 0, 0)
    LocationInfo.BorderSizePixel = 0
    LocationInfo.Position = UDim2.new(0.00163132139, 0, 0.113513514, 0)
    LocationInfo.Size = UDim2.new(0, 611, 0, 25)
    Title.Name = "Title"
    Title.Parent = LocationInfo
    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Title.BackgroundTransparency = 1.000
    Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Title.BorderSizePixel = 0
    Title.Position = UDim2.new(0.0605564639, 0, 0.119999997, 0)
    Title.Size = UDim2.new(0, 41, 0, 19)
    Title.Font = Enum.Font.SourceSans
    Title.Text = parameters["Name"]
    Title.TextColor3 = Color3.fromRGB(157, 157, 157)
    Title.TextSize = 12.000
    Title.TextXAlignment = Enum.TextXAlignment.Left
    Details.Name = "Details"
    Details.Parent = LocationInfo
    Details.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Details.BackgroundTransparency = 1.000
    Details.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Details.BorderSizePixel = 0
    Details.Position = UDim2.new(0.100000001, 0, 0.280000001, 0)
    Details.Size = UDim2.new(0, 11, 0, 11)
    Details.Image = "http://www.roblox.com/asset/?id=92541339821709"
    Details.ImageColor3 = Color3.fromRGB(157, 157, 157)
    Version2.Name = "Version"
    Version2.Parent = LocationInfo
    Version2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Version2.BackgroundTransparency = 1.000
    Version2.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Version2.BorderSizePixel = 0
    Version2.Position = UDim2.new(0.123000003, 0, 0.119999997, 0)
    Version2.Size = UDim2.new(0, 41, 0, 19)
    Version2.Font = Enum.Font.SourceSans
    Version2.Text = "Version "..parameters["Version"] or "1"
    Version2.TextColor3 = Color3.fromRGB(157, 157, 157)
    Version2.TextSize = 12.000
    Version2.TextXAlignment = Enum.TextXAlignment.Left
    Details_2.Name = "Details"
    Details_2.Parent = LocationInfo
    Details_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Details_2.BackgroundTransparency = 1.000
    Details_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Details_2.BorderSizePixel = 0
    Details_2.Position = UDim2.new(0.186000004, 0, 0.280000001, 0)
    Details_2.Size = UDim2.new(0, 11, 0, 11)
    Details_2.Image = "http://www.roblox.com/asset/?id=92541339821709"
    Details_2.ImageColor3 = Color3.fromRGB(157, 157, 157)
    PageName.Name = "PageName"
    PageName.Parent = LocationInfo
    PageName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    PageName.BackgroundTransparency = 1.000
    PageName.BorderColor3 = Color3.fromRGB(0, 0, 0)
    PageName.BorderSizePixel = 0
    PageName.Position = UDim2.new(0.209999993, 0, 0.119999997, 0)
    PageName.Size = UDim2.new(0, 41, 0, 19)
    PageName.Font = Enum.Font.SourceSans
    PageName.Text = "Page"
    PageName.TextColor3 = Color3.fromRGB(157, 157, 157)
    PageName.TextSize = 12.000
    PageName.TextXAlignment = Enum.TextXAlignment.Left
    TopBar.Name = "TopBar"
    TopBar.Parent = MainUI
    TopBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    TopBar.BackgroundTransparency = 1.000
    TopBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
    TopBar.BorderSizePixel = 0
    TopBar.Size = UDim2.new(0, 612, 0, 42)
    ImageLabel.Parent = TopBar
    ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    ImageLabel.BackgroundTransparency = 1.000
    ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
    ImageLabel.BorderSizePixel = 0
    ImageLabel.Position = UDim2.new(0.0245098043, 0, 0.214285716, 0)
    ImageLabel.Size = UDim2.new(0, 23, 0, 23)
    ImageLabel.Image = "http://www.roblox.com/asset/?id=91585427286587"
    ImageLabel.ImageColor3 = Color3.fromRGB(255, 255, 127)
    TitleName.Name = "TitleName"
    TitleName.Parent = TopBar
    TitleName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    TitleName.BackgroundTransparency = 1.000
    TitleName.BorderColor3 = Color3.fromRGB(0, 0, 0)
    TitleName.BorderSizePixel = 0
    TitleName.Position = UDim2.new(0.0784313753, 0, 0, 0)
    TitleName.Size = UDim2.new(0, 31, 0, 42)
    TitleName.FontFace = Font.new("rbxasset://fonts/families/Arimo.json", Enum.FontWeight.SemiBold, Enum.FontStyle.Normal)
    TitleName.Text = parameters["Name"]
    TitleName.TextColor3 = Color3.fromRGB(255, 255, 255)
    TitleName.TextSize = 14.000
    TitleName.TextXAlignment = Enum.TextXAlignment.Left
    VersionTop.Name = "VersionTop"
    VersionTop.Parent = TopBar
    VersionTop.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    VersionTop.BackgroundTransparency = 1.000
    VersionTop.BorderColor3 = Color3.fromRGB(0, 0, 0)
    VersionTop.BorderSizePixel = 0
    VersionTop.Position = UDim2.new(0.142156869, 0, 0, 0)
    VersionTop.Size = UDim2.new(0, 31, 0, 42)
    VersionTop.FontFace = Font.new("rbxasset://fonts/families/Arimo.json", Enum.FontWeight.SemiBold, Enum.FontStyle.Normal)
    VersionTop.Text = "V"..parameters["Version"] or "1"
    VersionTop.TextColor3 = Color3.fromRGB(255, 255, 127)
    VersionTop.TextSize = 14.000
    VersionTop.TextXAlignment = Enum.TextXAlignment.Left
    DetailIgnore.Name = "DetailIgnore"
    DetailIgnore.Parent = MainUI
    DetailIgnore.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
    DetailIgnore.BorderColor3 = Color3.fromRGB(0, 0, 0)
    DetailIgnore.BorderSizePixel = 0
    DetailIgnore.Position = UDim2.new(0.209055468, 0, 0.181081086, 0)
    DetailIgnore.Size = UDim2.new(0, 8, 0, 303)
    Navigations.Name = "Navigations"
    Navigations.Parent = MainUI
    Navigations.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
    Navigations.BorderColor3 = Color3.fromRGB(0, 0, 0)
    Navigations.BorderSizePixel = 0
    Navigations.Position = UDim2.new(0, 0, 0.181081086, 0)
    Navigations.Size = UDim2.new(0, 137, 0, 303)
    UICorner_2.Parent = Navigations
    UIListLayout.Parent = Navigations
    UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
    GapIgnore.Name = "GapIgnore"
    GapIgnore.Parent = Navigations
    GapIgnore.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    GapIgnore.BackgroundTransparency = 1.000
    GapIgnore.BorderColor3 = Color3.fromRGB(0, 0, 0)
    GapIgnore.BorderSizePixel = 0
    GapIgnore.Size = UDim2.new(0, 137, 0, 14)
    DetailIgnore_2.Name = "DetailIgnore"
    DetailIgnore_2.Parent = MainUI
    DetailIgnore_2.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
    DetailIgnore_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
    DetailIgnore_2.BorderSizePixel = 0
    DetailIgnore_2.Position = UDim2.new(0.223491028, 0, 0.183783785, 0)
    DetailIgnore_2.Size = UDim2.new(0, 1, 0, 302)
    DetailIgnore_3.Name = "DetailIgnore"
    DetailIgnore_3.Parent = MainUI
    DetailIgnore_3.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
    DetailIgnore_3.BorderColor3 = Color3.fromRGB(0, 0, 0)
    DetailIgnore_3.BorderSizePixel = 0
    DetailIgnore_3.Position = UDim2.new(0, 0, 0.181081086, 0)
    DetailIgnore_3.Size = UDim2.new(0, 137, 0, 1)

    MainUI.Position = UDim2.new(0.5, 0, 0.5, 0)
    MainUI.AnchorPoint = Vector2.new(0.5, 0.5)

    pcall(function() local a=game:GetService("UserInputService")local b=game:GetService("RunService")local c=MainUI;local d;local e;local f;local g;function Lerp(h,i,j)return h+(i-h)*j end;local k;local l;local m=8;function Update(n)if not g then return end;if not d and l then c.Position=UDim2.new(g.X.Scale,Lerp(c.Position.X.Offset,l.X.Offset,n*m),g.Y.Scale,Lerp(c.Position.Y.Offset,l.Y.Offset,n*m))return end;local o=k-a:GetMouseLocation()local p=g.X.Offset-o.X;local q=g.Y.Offset-o.Y;l=UDim2.new(g.X.Scale,p,g.Y.Scale,q)c.Position=UDim2.new(g.X.Scale,Lerp(c.Position.X.Offset,p,n*m),g.Y.Scale,Lerp(c.Position.Y.Offset,q,n*m))end;c.InputBegan:Connect(function(r)if r.UserInputType==Enum.UserInputType.MouseButton1 or r.UserInputType==Enum.UserInputType.Touch then d=true;f=r.Position;g=c.Position;k=a:GetMouseLocation()r.Changed:Connect(function()if r.UserInputState==Enum.UserInputState.End then d=false end end)end end)c.InputChanged:Connect(function(r)if r.UserInputType==Enum.UserInputType.MouseMovement or r.UserInputType==Enum.UserInputType.Touch then e=r end end)b.Heartbeat:Connect(Update) end)


    function GuiFunctions:AddPage(parameters)

        local PageFunctions = {}

        local Page = Instance.new("Frame")
        local Features = Instance.new("ScrollingFrame")
        Features.AutomaticCanvasSize = "Y"
        local UIListLayout = Instance.new("UIListLayout")
        local UICorner = Instance.new("UICorner")
        local TextLabel = Instance.new("TextLabel")
        Page.Name = "Page"
        Page.Parent = MainUI
        Page.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Page.BackgroundTransparency = 1.000
        Page.BorderColor3 = Color3.fromRGB(0, 0, 0)
        Page.BorderSizePixel = 0
        Page.Position = UDim2.new(0.225122347, 0, 0.183783785, 0)
        Page.Size = UDim2.new(0, 475, 0, 302)
        Page.Visible = false
        Features.Name = "Features"
        Features.Parent = Page
        Features.Active = true
        Features.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
        Features.BorderColor3 = Color3.fromRGB(0, 0, 0)
        Features.BorderSizePixel = 0
        Features.Position = UDim2.new(0.0357894748, 0, 0.089403972, 0)
        Features.Size = UDim2.new(0, 441, 0, 261)
        Features.CanvasSize = UDim2.new(0, 0, 0, 0)
        Features.ScrollBarThickness = 2
        local uistroke = Instance.new("UIStroke")
        uistroke.Color = Color3.fromRGB(26, 26, 26)
        uistroke.Parent = Features
        uistroke.ApplyStrokeMode = "Border"
        UIListLayout.Parent = Features
        UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        UIListLayout.VerticalAlignment = Enum.VerticalAlignment.Top --
        UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center --
        UICorner.Parent = Features
        TextLabel.Parent = Page
        TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        TextLabel.BackgroundTransparency = 1.000
        TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
        TextLabel.BorderSizePixel = 0
        TextLabel.Position = UDim2.new(0.0480000004, 0, 0.0160000008, 0)
        TextLabel.Size = UDim2.new(0, 177, 0, 20)
        TextLabel.Font = Enum.Font.SourceSans
        TextLabel.Text = parameters["Name"] or "Page"
        TextLabel.TextColor3 = Color3.fromRGB(125, 125, 125)
        TextLabel.TextSize = 14.000
        TextLabel.TextXAlignment = Enum.TextXAlignment.Left

        local ButtonNav = Instance.new("TextButton")
        local TextLabel2 = Instance.new("TextLabel")
        local ImageLabel = Instance.new("ImageLabel")
        ButtonNav.Name = "ButtonNav"
        ButtonNav.Parent = Navigations
        ButtonNav.Active = false
        ButtonNav.BackgroundColor3 = Color3.fromRGB(255, 170, 255)
        ButtonNav.BackgroundTransparency = 1.000
        ButtonNav.BorderColor3 = Color3.fromRGB(0, 0, 0)
        ButtonNav.BorderSizePixel = 0
        ButtonNav.Position = UDim2.new(0, 0, 0.0957095698, 0)
        ButtonNav.Selectable = false
        ButtonNav.Size = UDim2.new(0, 137, 0, 25)
        ButtonNav.Text = ""
        ButtonNav.FontFace = Font.new("rbxasset://fonts/families/Arimo.json", Enum.FontWeight.Regular, Enum.FontStyle.Normal)
        TextLabel2.Parent = ButtonNav
        TextLabel2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        TextLabel2.BackgroundTransparency = 1.000
        TextLabel2.BorderColor3 = Color3.fromRGB(0, 0, 0)
        TextLabel2.BorderSizePixel = 0
        TextLabel2.Position = UDim2.new(0.241897911, 0, 0.0799999982, 0)
        TextLabel2.Size = UDim2.new(0, 95, 0, 21)
        TextLabel2.Font = Enum.Font.SourceSansSemibold
        TextLabel2.Text = parameters["Name"] or "Page"
        TextLabel2.TextColor3 = Color3.fromRGB(176, 176, 176)
        TextLabel2.TextSize = 14.000
        TextLabel2.TextXAlignment = Enum.TextXAlignment.Left
        ImageLabel.Parent = ButtonNav
        ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        ImageLabel.BackgroundTransparency = 1.000
        ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
        ImageLabel.BorderSizePixel = 0
        ImageLabel.Position = UDim2.new(0.0700000003, 0, 0.159999996, 0)
        ImageLabel.Size = UDim2.new(0, 17, 0, 17)
        ImageLabel.Image = parameters["Icon"] or "http://www.roblox.com/asset/?id=134185092738546"
        ImageLabel.ImageColor3 = Color3.fromRGB(176, 176, 176)

        if #Pages <= 0 then
            OpenedPage = Page
            Page.Visible = true
            ImageLabel.ImageColor3 = ThemeColor
            TextLabel2.TextColor3 = ThemeColor
            PageName.Text = parameters["Name"] or "Page"
        end

        table.insert(Pages, {
            ["NavigationFrame"] = ButtonNav,
            ["PageFrame"] = Page
        })

        ButtonNav.MouseButton1Click:connect(function()
            for i,v in pairs(Pages) do
                if v.PageFrame ~= OpenedPage then continue end
                v.PageFrame.Visible = false
                game:GetService("TweenService"):Create(v.NavigationFrame.TextLabel, TweenInfo.new(0.25), {TextColor3 = Color3.fromRGB(176, 176, 176)}):Play()
                game:GetService("TweenService"):Create(v.NavigationFrame.ImageLabel, TweenInfo.new(0.25), {ImageColor3 = Color3.fromRGB(176, 176, 176)}):Play()
            end

            

            Page.Visible = true

            game:GetService("TweenService"):Create(TextLabel2, TweenInfo.new(0.25), {TextColor3 = ThemeColor}):Play()
            game:GetService("TweenService"):Create(ImageLabel, TweenInfo.new(0.25), {ImageColor3 = ThemeColor}):Play()


            

            OpenedPage = Page
            PageName.Text = parameters["Name"] or "Page"
        end)



        function PageFunctions:AddButton(parameters)

            local ElementData = {
                ["Type"] = "Button",
                ["Trigger"] = nil,
                ["Object"] = nil,
            }


            local Button = Instance.new("TextButton")
            local UICorner = Instance.new("UICorner")
            local DetailIgnore = Instance.new("Frame")
            local TextLabel = Instance.new("TextLabel")
            local ImageLabel = Instance.new("ImageLabel")
            local Description = Instance.new("TextLabel")
            Button.Name = "Button"
            Button.Parent = Features
            Button.Active = false
            Button.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
            Button.BorderColor3 = Color3.fromRGB(26, 26, 26)
            Button.Position = UDim2.new(0.0113378689, 0, 0.383141756, 0)
            Button.Selectable = false
            Button.Size = UDim2.new(0, 438, 0, 40)
            Button.Text = ""
            UICorner.Parent = Button
            DetailIgnore.Name = "DetailIgnore"
            DetailIgnore.Parent = Button
            DetailIgnore.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
            DetailIgnore.BorderColor3 = Color3.fromRGB(0, 0, 0)
            DetailIgnore.BorderSizePixel = 0
            DetailIgnore.Position = UDim2.new(0.0319634713, 0, 0.925000012, 0)
            DetailIgnore.Size = UDim2.new(0, 412, 0, 1)
            TextLabel.Parent = Button
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
            TextLabel.BorderSizePixel = 0
            TextLabel.Position = UDim2.new(0.0319634713, 0, 0.174999997, 0)
            TextLabel.Size = UDim2.new(0, 185, 0, 23)
            TextLabel.Font = Enum.Font.SourceSansSemibold
            TextLabel.Text = parameters["Name"] or "Button"
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 14.000
            TextLabel.TextXAlignment = Enum.TextXAlignment.Left
            ImageLabel.Parent = Button
            ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 127)
            ImageLabel.BackgroundTransparency = 1.000
            ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
            ImageLabel.BorderSizePixel = 0
            ImageLabel.Position = UDim2.new(0.920091331, 0, 0.200000003, 0)
            ImageLabel.Size = UDim2.new(0, 23, 0, 23)
            ImageLabel.Image = "http://www.roblox.com/asset/?id=16630151971"
            ImageLabel.ImageColor3 = Color3.fromRGB(255, 255, 127)
            Description.Name = "Description"
            Description.Parent = Button
            Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Description.BackgroundTransparency = 1.000
            Description.BorderColor3 = Color3.fromRGB(0, 0, 0)
            Description.BorderSizePixel = 0
            Description.Position = UDim2.new(0.0319634713, 0, 0.435000002, 0)
            Description.Size = UDim2.new(0, 201, 0, 14)
            Description.Visible = false
            Description.Font = Enum.Font.SourceSansSemibold
            Description.Text = "DescriptionExample"
            Description.TextColor3 = Color3.fromRGB(148, 148, 148)
            Description.TextSize = 13.000
            Description.TextXAlignment = Enum.TextXAlignment.Left

            if parameters["Description"] then
                Description.Visible = true
                Description.Text = parameters["Description"]
                Button.Size = UDim2.new(0, 438, 0, 50)
                ImageLabel.Position = UDim2.new(0.92, 0,0.26, 0)
                TextLabel.Position = UDim2.new(0.032, 0,0.135, 0)
                Description.Position = UDim2.new(0.032, 0,0.495, 0)
            end

            local function OnClicked()
                if parameters["Function"] and type(parameters["Function"]) == "function" then
                    parameters["Function"]()
                else
                    print("No function assigned, add the table index Function = function() ... end")
                end
            end

            Button.MouseButton1Click:connect(OnClicked)

            ElementData.Object = Button
            ElementData.Trigger = OnClicked
            table.insert(UIElements, ElementData)
            return ElementData
        end

        function PageFunctions:AddToggle(parameters)

            local ElementData = {
                ["Type"] = "Toggle",
                ["Trigger"] = nil,
                ["Object"] = nil,
                ["Attributes"] = {
                    ["Toggled"] = false
                }
            }

            local Toggle = Instance.new("Frame")
            local UICorner = Instance.new("UICorner")
            local DetailIgnore = Instance.new("Frame")
            local TextLabel = Instance.new("TextLabel")
            local Description = Instance.new("TextLabel")
            local MainToggle = Instance.new("TextButton")
            local UICorner_2 = Instance.new("UICorner")
            local Toggle_2 = Instance.new("TextButton")
            local UICorner_3 = Instance.new("UICorner")
            local uistroke = Instance.new("UIStroke")
            Toggle.Name = "Toggle"
            Toggle.Parent = Features
            Toggle.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
            Toggle.BorderColor3 = Color3.fromRGB(26, 26, 26)
            Toggle.Position = UDim2.new(0, 0, 0.00766283507, 0)
            Toggle.Size = UDim2.new(0, 438, 0, 40)
            UICorner.Parent = Toggle
            DetailIgnore.Name = "DetailIgnore"
            DetailIgnore.Parent = Toggle
            DetailIgnore.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
            DetailIgnore.BorderColor3 = Color3.fromRGB(0, 0, 0)
            DetailIgnore.BorderSizePixel = 0
            DetailIgnore.Position = UDim2.new(0.0319634713, 0, 0.925000012, 0)
            DetailIgnore.Size = UDim2.new(0, 412, 0, 1)
            TextLabel.Parent = Toggle
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
            TextLabel.BorderSizePixel = 0
            TextLabel.Position = UDim2.new(0.0319634713, 0, 0.174999997, 0)
            TextLabel.Size = UDim2.new(0, 185, 0, 23)
            TextLabel.Font = Enum.Font.SourceSansSemibold
            TextLabel.Text = parameters["Name"] or "Toggle"
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 14.000
            TextLabel.TextXAlignment = Enum.TextXAlignment.Left
            MainToggle.Name = "MainToggle"
            MainToggle.Parent = Toggle
            MainToggle.BackgroundColor3 = Color3.fromRGB(17, 17, 20)
            MainToggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
            MainToggle.BorderSizePixel = 0
            MainToggle.BackgroundTransparency = 0.3
            MainToggle.Position = UDim2.new(0.905994594, 0, 0.26600036, 0)
            MainToggle.Size = UDim2.new(0, 29, 0, 14)
            MainToggle.Text = ""
            uistroke.Color = Color3.fromRGB(26, 26, 26)
            uistroke.Parent = MainToggle
            uistroke.ApplyStrokeMode = "Border"
            MainToggle.AutoButtonColor = true
            UICorner_2.CornerRadius = UDim.new(0, 10)
            UICorner_2.Parent = MainToggle
            Toggle_2.Name = "Toggle"
            Toggle_2.Parent = MainToggle
            Toggle_2.Active = false
            Toggle_2.Interactable = false
            Toggle_2.BackgroundColor3 = Color3.fromRGB(255, 255, 127)
            Toggle_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
            Toggle_2.BorderSizePixel = 0
            Toggle_2.Selectable = false
            Toggle_2.Size = UDim2.new(0, 14, 0, 14)
            Toggle_2.Text = ""
            UICorner_3.CornerRadius = UDim.new(0, 10)
            UICorner_3.Parent = Toggle_2
            Description.Name = "Description"
            Description.Parent = Toggle
            Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Description.BackgroundTransparency = 1.000
            Description.BorderColor3 = Color3.fromRGB(0, 0, 0)
            Description.BorderSizePixel = 0
            Description.Position = UDim2.new(0.0319634713, 0, 0.435000002, 0)
            Description.Size = UDim2.new(0, 201, 0, 14)
            Description.Visible = false
            Description.Font = Enum.Font.SourceSansSemibold
            Description.Text = "DescriptionExample"
            Description.TextColor3 = Color3.fromRGB(148, 148, 148)
            Description.TextSize = 13.000
            Description.TextXAlignment = Enum.TextXAlignment.Left

            if parameters["Description"] then
                Description.Visible = true
                Description.Text = parameters["Description"]
                Toggle.Size = UDim2.new(0, 438, 0, 50)
                TextLabel.Position = UDim2.new(0.032, 0,0.135, 0)
                Description.Position = UDim2.new(0.032, 0,0.495, 0)
                MainToggle.Position = UDim2.new(0.906, 0,0.346, 0)
            end

            local function OnToggle(Toggled)
                if Toggled == true then
                    game:GetService("TweenService"):Create(MainToggle, TweenInfo.new(0.07, Enum.EasingStyle.Linear), {BackgroundColor3 = ThemeColor}):Play()
                    game:GetService("TweenService"):Create(Toggle_2, TweenInfo.new(0.07, Enum.EasingStyle.Linear), {Position = UDim2.new(0, 15,0, 0)}):Play()
                    ElementData["Attributes"].Toggled = true
                    parameters["Function"](true)
                elseif Toggled == false then
                    game:GetService("TweenService"):Create(MainToggle, TweenInfo.new(0.07, Enum.EasingStyle.Linear), {BackgroundColor3 = Color3.fromRGB(17, 17, 20)}):Play()
                    game:GetService("TweenService"):Create(Toggle_2, TweenInfo.new(0.07, Enum.EasingStyle.Linear), {Position = UDim2.new(0,0,0,0)}):Play()
                    ElementData["Attributes"].Toggled = false
                    parameters["Function"](false)
                end
            end
            ElementData.Trigger = OnToggle
            ElementData.Object = Toggle
            MainToggle.MouseButton1Click:connect(function()
                OnToggle(not ElementData["Attributes"].Toggled)
            end)
            
            table.insert(UIElements, ElementData)
            return ElementData
        end

        function PageFunctions:AddSlider(parameters)
            local ElementData = {
                ["Type"] = "Slider",
                ["Trigger"] = nil,
                ["Object"] = nil,
                ["Attributes"] = {
                    ["Value"] = 0
                }
            }

            local Slider = Instance.new("Frame")
            local UICorner = Instance.new("UICorner")
            local DetailIgnore = Instance.new("Frame")
            local TextLabel = Instance.new("TextLabel")
            local SlideValue = Instance.new("TextLabel")
            local Slider_2 = Instance.new("Frame")
            local Slider_3 = Instance.new("TextButton")
            local UIListLayout = Instance.new("UIListLayout")
            local Bar = Instance.new("Frame")
            local UICorner_2 = Instance.new("UICorner")
            local circ = Instance.new("TextButton")
            local UICorner_3 = Instance.new("UICorner")
            local UICorner_4 = Instance.new("UICorner")
            local UIListLayout_2 = Instance.new("UIListLayout")
            local UICorner_5 = Instance.new("UICorner")
            local Description = Instance.new("TextLabel")
            Slider.Name = "Slider"
            Slider.Parent = Features
            Slider.BackgroundColor3 = Color3.fromRGB(10, 10, 12)
            Slider.BorderColor3 = Color3.fromRGB(26, 26, 26)
            Slider.Position = UDim2.new(0, 0, 0.153256699, 0)
            Slider.Size = UDim2.new(0, 438, 0, 50)
            UICorner.Parent = Slider
            DetailIgnore.Name = "DetailIgnore"
            DetailIgnore.Parent = Slider
            DetailIgnore.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
            DetailIgnore.BorderColor3 = Color3.fromRGB(0, 0, 0)
            DetailIgnore.BorderSizePixel = 0
            DetailIgnore.Position = UDim2.new(0.0319634713, 0, 0.925000012, 0)
            DetailIgnore.Size = UDim2.new(0, 412, 0, 1)
            TextLabel.Parent = Slider
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
            TextLabel.BorderSizePixel = 0
            TextLabel.Position = UDim2.new(0.0319634713, 0, -0.00499999989, 0)
            TextLabel.Size = UDim2.new(0, 185, 0, 23)
            TextLabel.Font = Enum.Font.SourceSansSemibold
            TextLabel.Text = parameters["Name"] or "Slider"
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 14.000
            TextLabel.TextXAlignment = Enum.TextXAlignment.Left
            SlideValue.Name = "SlideValue"
            SlideValue.Parent = Slider
            SlideValue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            SlideValue.BackgroundTransparency = 1.000
            SlideValue.BorderColor3 = Color3.fromRGB(0, 0, 0)
            SlideValue.BorderSizePixel = 0
            SlideValue.Position = UDim2.new(0.847031951, 0, 0, 0)
            SlideValue.Size = UDim2.new(0, 55, 0, 22)
            SlideValue.Font = Enum.Font.SourceSansSemibold
            SlideValue.Text = "100"
            SlideValue.TextColor3 = Color3.fromRGB(255, 255, 255)
            SlideValue.TextSize = 14.000
            SlideValue.TextXAlignment = Enum.TextXAlignment.Right
            Slider_2.Name = "Slider"
            Slider_2.Parent = Slider
            Slider_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Slider_2.BackgroundTransparency = 1.000
            Slider_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
            Slider_2.BorderSizePixel = 0
            Slider_2.Position = UDim2.new(0.0180000756, 0, 0.49000001, 0)
            Slider_2.Size = UDim2.new(0.961473703, 0, 0.313253343, 0)
            Slider_3.Name = "Slider"
            Slider_3.Parent = Slider_2
            Slider_3.AnchorPoint = Vector2.new(0.5, 0.5)
            Slider_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
            Slider_3.BorderColor3 = Color3.fromRGB(27, 42, 53)
            Slider_3.BorderSizePixel = 0
            Slider_3.Position = UDim2.new(0.50000006, 0, 0.468076438, 0)
            Slider_3.Size = UDim2.new(0.967999995, 0, 0.349999994, 0)
            Slider_3.Font = Enum.Font.Cartoon
            Slider_3.Text = ""
            Slider_3.TextColor3 = Color3.fromRGB(0, 0, 0)
            Slider_3.TextSize = 14.000
            UIListLayout.Parent = Slider_3
            UIListLayout.FillDirection = Enum.FillDirection.Horizontal
            UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
            UIListLayout.VerticalAlignment = Enum.VerticalAlignment.Center
            UIListLayout.Padding = UDim.new(0, -6)
            Bar.Name = "Bar"
            Bar.Parent = Slider_3
            Bar.BackgroundColor3 = Color3.fromRGB(255, 255, 127)
            Bar.BorderColor3 = Color3.fromRGB(27, 42, 53)
            Bar.BorderSizePixel = 0
            Bar.Position = UDim2.new(0, 0, 0.0499979518, 0)
            Bar.Size = UDim2.new(0.971000016, 0, 0.950001538, 0)
            UICorner_2.CornerRadius = UDim.new(0, 70)
            UICorner_2.Parent = Bar
            circ.Name = "circ"
            circ.Parent = Slider_3
            circ.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            circ.BorderColor3 = Color3.fromRGB(0, 0, 0)
            circ.BorderSizePixel = 0
            circ.Position = UDim2.new(0.956285119, 0, -1.64303362, 0)
            circ.Size = UDim2.new(0, 10, 0, 19)
            circ.Font = Enum.Font.SourceSans
            circ.Text = ""
            circ.TextColor3 = Color3.fromRGB(0, 0, 0)
            circ.TextSize = 14.000
            UICorner_3.Parent = circ
            UICorner_4.Parent = Slider_3
            UIListLayout_2.Parent = Slider_2
            UIListLayout_2.HorizontalAlignment = Enum.HorizontalAlignment.Center
            UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
            UIListLayout_2.VerticalAlignment = Enum.VerticalAlignment.Center
            UICorner_5.CornerRadius = UDim.new(0, 4)
            UICorner_5.Parent = Slider_2
            Description.Name = "Description"
            Description.Parent = Slider
            Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Description.BackgroundTransparency = 1.000
            Description.BorderColor3 = Color3.fromRGB(0, 0, 0)
            Description.BorderSizePixel = 0
            Description.Position = UDim2.new(0.0319634713, 0, 0.435000002, 0)
            Description.Size = UDim2.new(0, 201, 0, 14)
            Description.Visible = false
            Description.Font = Enum.Font.SourceSansSemibold
            Description.Text = "DescriptionExample"
            Description.TextColor3 = Color3.fromRGB(148, 148, 148)
            Description.TextSize = 13.000
            Description.TextXAlignment = Enum.TextXAlignment.Left

            if parameters["Description"] then
                Description.Visible = true
                Description.Text = parameters["Description"]
                Slider.Size = UDim2.new(0, 438, 0, 50)
                TextLabel.Size = UDim2.new(0, 185,0, 15)
                TextLabel.Position = UDim2.new(0.03, 0,0, 0)
                Description.Position = UDim2.new(0.032, 0,0.279, 0)
                Description.Size = UDim2.new(0, 201,0, 14)
                Slider_2.Position = UDim2.new(0.018, 0,0.55, 0)
                Slider_2.Size = UDim2.new(0.961, 0,0.313, 0)
            end
            
        
            pcall(function()
                local min, max, init,func = (parameters["Minimum"] or parameters["Min"] or 0), (parameters["Maximum"] or parameters["Max"] or 100), (parameters["Initial"] or parameters["Init"] or 50), (parameters["Function"] or function(value) end)
                local h = Slider_2
                local val, sldr, bar, mouse = h.Parent.SlideValue, h.Slider, h.Slider.Bar, game.Players.LocalPlayer:GetMouse()
                local circ, held = sldr.circ, false

                local function SetValue(value, dontusefunc)
                    bar.Size = UDim2.new((value - min)/(max - min), 0, 0.95, 0)
                    val.Text = tostring(value)
                    ElementData.Attributes.Value = tonumber(value)
                    if not dontusefunc then
                        func(tonumber(value))
                    end
                end

                SetValue(init, true)
                ElementData.Trigger = SetValue
                
                local function update()
                    local x = mouse.X
                    local scale = math.clamp((x - sldr.AbsolutePosition.X)/sldr.AbsoluteSize.X, 0, 1)
                    bar.Size = UDim2.new(scale, 0, 0.95, 0)
                    val.Text = tostring(math.floor(scale * (max - min) + min))
                    ElementData.Attributes.Value = tonumber(math.floor(scale * (max - min) + min))
                    func(tonumber(math.floor(scale * (max - min) + min)))
                end
                sldr.MouseButton1Down:Connect(function() held = true update() end)
                circ.MouseButton1Down:Connect(function() held = true update() end)
                game:GetService("UserInputService").InputEnded:Connect(function(input)
                    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then held = false end
                end)
                mouse.Move:Connect(function() if held then update() end end)
            end)

            ElementData.Object = Slider
            table.insert(UIElements, ElementData)
            return ElementData
        end

        return PageFunctions
    end

    return GuiFunctions
end

return library
