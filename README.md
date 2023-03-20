                if not game:IsLoaded()then 
                    local a=Instance.new("Message",workspace);
                    a.Text='Waiting game to loaded before scripts is getting executed by Winnable Hub';
                    game.Loaded:Wait();
                    a:Destroy();
                    wait(10);
                end;
            
            function executenow()
                local placeId = game.PlaceId
            if placeId == 2866967438 then -- Fishing Simulator
        if not game:IsLoaded()then 
                local a=Instance.new("Message",workspace);
                a.Text='Waiting game to loaded before scripts is getting executed by Winnable Hub';
                game.Loaded:Wait();
                a:Destroy();
                wait(10);
            end;
                
        function totarget(p)
            local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/2000, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p.CFrame * CFrame.new(0,0,30)})
            tween:Play()
        end
        
        function totargetv2(p)
            local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/2000, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p.CFrame * CFrame.new(0,0,0)})
            tween:Play()
        end
        
                spear = {}
                for i,v in pairs(game:GetService("ReplicatedStorage").Assets.Spears:GetChildren()) do
                        if v:IsA("Tool") then
                            table.insert(spear ,v.Name)
                        end
                end
        
        local TweenService = game:GetService('TweenService')
        local object = cre
        local tweenInfo = TweenInfo.new(2.5)
        
        while getfenv().RGB do
        local r, g, b = math.random(), math.random(), math.random()
        local goal = {Color = Color3.new(r, g, b)}
        
        local tween = TweenService:Create(object, tweenInfo, goal)
        tween:Play()
        tween.Completed:Wait()
        end
        
        if game.CoreGui:FindFirstChild("ToggleUI") then
        	game.CoreGui:FindFirstChild("ToggleUI"):Destroy()
        end
        local ToggleUI = Instance.new("ScreenGui")
        local ToggleButton = Instance.new("TextButton")
        local ToggleButtonHUI = Instance.new("UICorner")
        ToggleUI.Name = "ToggleUI"
        ToggleUI.Parent = game.CoreGui
        ToggleUI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        
        ToggleButton.Name = "ToggleButton"
        ToggleButton.Parent = ToggleUI
        ToggleButton.BackgroundColor3 = Color3.fromRGB(30,20,20)
        ToggleButton.BackgroundTransparency = 0.1
        ToggleButton.BorderSizePixel = 0
        ToggleButton.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
        ToggleButton.Size = UDim2.new(0, 50, 0, 50)
        ToggleButton.Font = Enum.Font.SourceSans
        ToggleButton.Text = ""
        ToggleButton.TextColor3 = Color3.fromRGB(0, 0, 0)
        ToggleButton.TextSize = 14.000
        ToggleButton.Draggable = true
        ToggleButton.MouseButton1Click:Connect(function()
        	game.CoreGui:FindFirstChild("Kenei").Enabled = not game.CoreGui:FindFirstChild("Kenei").Enabled
        end)
        
        coroutine.wrap(
        	function()
        	do
            local CoreGui = {}
            local CheckCoreGui = {}
            local CoreGui = game:GetService("CoreGui"):FindFirstChild("Kenei")
                if CoreGui then 
                 CoreGui:Destroy() 
                elseif CoreGui then 
                local CheckCoreGui = not game.CoreGui:FindFirstChild("Kenei").Enabled
                    if CheckCoreGui then
                    CoreGui:Destroy()
                    elseif not CoreGui and CheckCoreGuithen == nil then
                         local CoreGui = nil or {nil}
                         local CheckCoreGu = nil or {nil}
                    end
                end
            end
        end)();
        -- // variables
        local library = {}
        local pages = {}
        local sections = {}
        local multisections = {}
        local mssections = {}
        local toggles = {}
        local buttons = {}
        local sliders = {}
        local dropdowns = {}
        local multiboxs = {}
        local buttonboxs = {}
        local textboxs = {}
        local keybinds = {}
        local colorpickers = {}
        local configloaders = {}
        local watermarks = {}
        local loaders = {}
        --
        local utility = {}
        --
        local plrs = game:GetService("Players")
        local cre = game:GetService("CoreGui")
        local rs = game:GetService("RunService")
        local ts = game:GetService("TweenService") 
        local uis = game:GetService("UserInputService") 
        local hs = game:GetService("HttpService")
        local ws = game:GetService("Workspace")
        local plr = plrs.LocalPlayer
        local cam = ws.CurrentCamera
        -- // indexes
        library.__index = library
        pages.__index = pages
        sections.__index = sections
        multisections.__index = multisections
        mssections.__index = mssections
        toggles.__index = toggles
        buttons.__index = buttons
        sliders.__index = sliders
        dropdowns.__index = dropdowns
        multiboxs.__index = multiboxs
        buttonboxs.__index = buttonboxs
        textboxs.__index = textboxs
        keybinds.__index = keybinds
        colorpickers.__index = colorpickers
        configloaders.__index = configloaders
        watermarks.__index = watermarks
        loaders.__index = loaders
        -- // functions
        utility.new = function(instance,properties) 
        	-- // instance
        	local ins = Instance.new(instance)
        	-- // properties setting
        	for property,value in pairs(properties) do
        		ins[property] = value
        	end
        	-- // return
        	return ins
        end
        --
        utility.dragify = function(ins,touse)
        	local dragging
        	local dragInput
        	local dragStart
        	local startPos
        	--
        	local function update(input)
        		local delta = input.Position - dragStart
        		touse:TweenPosition(UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.1,true)
        	end
        	--
        	ins.InputBegan:Connect(function(input)
        		if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
        			dragging = true
        			dragStart = input.Position
        			startPos = touse.Position
        
        			input.Changed:Connect(function()
        				if input.UserInputState == Enum.UserInputState.End then
        					dragging = false
        				end
        			end)
        		end
        	end)
        	--
        	ins.InputChanged:Connect(function(input)
        		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
        			dragInput = input
        		end
        	end)
        	--
        	uis.InputChanged:Connect(function(input)
        		if input == dragInput and dragging then
        			update(input)
        		end
        	end)
        end
        --
        utility.round = function(n,d)
        	return tonumber(string.format("%."..(d or 0).."f",n))
        end
        --
        utility.zigzag = function(X)
        	return math.acos(math.cos(X*math.pi))/math.pi
        end
        --
        utility.capatalize = function(s)
        	local l = ""
        	for v in s:gmatch('%u') do
        		l = l..v
        	end
        	return l
        end
        --
        utility.splitenum = function(enum)
        	local s = tostring(enum):split(".")
        	return s[#s]
        end
        --
        utility.from_hex = function(h)
        	local r,g,b = string.match(h,"^#?(%w%w)(%w%w)(%w%w)$")
        	return Color3.fromRGB(tonumber(r,16), tonumber(g,16), tonumber(b,16))
        end
        --
        utility.to_hex = function(c)
        	return string.format("#%02X%02X%02X",c.R *255,c.G *255,c.B *255)
        end
        --
        utility.removespaces = function(s)
           return s:gsub(" ","")
        end
        -- // main
        function library:new(props)
        	-- // properties
        	local textsize = props.textsize or props.TextSize or props.textSize or props.Textsize or 12
        	local font = props.font or props.Font or "RobotoMono"
        	local name = props.name or props.Name or props.UiName or props.Uiname or props.uiName or props.username or props.Username or props.UserName or props.userName or "new ui"
        	local color = props.color or props.Color or props.mainColor or props.maincolor or props.MainColor or props.Maincolor or props.Accent or props.accent or Color3.fromRGB(225, 58, 81)
        	-- // variables
        	local window = {}
        	-- // main
        	local screen = utility.new(
        		"ScreenGui",
        		{
        			Name = "Kenei",
        			DisplayOrder = 9999,
        			ResetOnSpawn = false,
        			ZIndexBehavior = "Global",
        			Parent = cre
        		}
        	)
        	-- 1
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = color,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,541,0,341),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = screen
        		}
        	)
        	-- 2
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = outline
        		}
        	)
        	-- 3
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = outline2
        		}
        	)
        	-- 4
        	local main = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-10,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline2
        		}
        	)
        	-- 5
        	local outline3 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	--
        	local titletext = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextXAlignment = "Left",
        			TextSize = textsize,
        			TextStrokeTransparency = 0,
        			Parent = title
        		}
        	)
        	-- 6
        	local holder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-6,1,-6),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	-- 7
        	local holder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-6,1,-6),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	-- 8
        	local tabs = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,-20),
        			Position = UDim2.new(0.5,0,1,0),
        			Parent = holder
        		}
        	)
        	--
        	local tabsbuttons = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,21),
        			Position = UDim2.new(0.5,0,0,0),
        			ZIndex = 2,
        			Parent = holder
        		}
        	)
        	-- 9
        	local outline4 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabs
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Horizontal",
        			Padding = UDim.new(0,2),
        			Parent = tabsbuttons
        		}
        	)
        	--
        	utility.dragify(title,outline)
        	-- // window tbl
        	window = {
        		["screen"] = screen,
        		["holder"] = holder,
        		["labels"] = {},
        		["tabs"] = outline4,
        		["tabsbuttons"] = tabsbuttons,
        		["outline"] = outline,
        		["pages"] = {},
        		["pointers"] = {},
        		["dropdowns"] = {},
        		["multiboxes"] = {},
        		["buttonboxs"] = {},
        		["colorpickers"] = {},
        		["x"] = true,
        		["y"] = true,
        		["key"] = Enum.KeyCode.RightShift,
        		["textsize"] = textsize,
        		["font"] = font,
        		["theme"] = {
        			["accent"] = color
        		},
        		["themeitems"] = {
        			["accent"] = {
        				["BackgroundColor3"] = {},
        				["BorderColor3"] = {},
        				["TextColor3"] = {}
        			}
        		}
        	}
        	--
        	table.insert(window.themeitems["accent"]["BackgroundColor3"],outline)
        	--
        	local toggled = true
        	local cooldown = false
        	local saved = UDim2.new(0,0,0,0)
        	--
        	uis.InputBegan:Connect(function(Input)
        		if Input.UserInputType == Enum.UserInputType.Keyboard then
        			if Input.KeyCode == window.key then
        				if cooldown == false then
        					if toggled then
        						cooldown = true
        						toggled = not toggled
        						saved = outline.Position
        						local xx,yy = 0,0
        						local xxx,yyy = 0,0
        						--
        						if (outline.AbsolutePosition.X+(outline.AbsoluteSize.X/2)) < (cam.ViewportSize.X/2) then
        							xx = -3
        						else
        							xx = 3
        						end
        						--
        						if window.y then
        							if (outline.AbsolutePosition.Y+(outline.AbsoluteSize.Y/2)) < (cam.ViewportSize.Y/2) then
        								yy = -3
        							else
        								yy = 3
        							end
        						else
        							yy = saved.Y.Scale
        							yyy = saved.Y.Offset
        						end
        						--
        						if window.x == false and window.y == false then
        							screen.Enabled = false
        						else
        							ts:Create(outline, TweenInfo.new(0.5,Enum.EasingStyle.Quad,Enum.EasingDirection.In), {Position = UDim2.new(xx,xxx,yy,yyy)}):Play()
        						end
        						wait(0.5)
        						cooldown = false
        					else
        						cooldown = true
        						toggled = not toggled
        						if window.x == false and window.y == false then
        							screen.Enabled = true
        						else
        							ts:Create(outline, TweenInfo.new(0.5,Enum.EasingStyle.Quad,Enum.EasingDirection.Out), {Position = saved}):Play()
        						end
        						wait(0.5)
        						cooldown = false
        					end
        				end
        			end
        		end
        	end)
        	--
        	window.labels[#window.labels+1] = titletext
        	-- // metatable indexing + return
        	setmetatable(window, library)
        	return window
        end
        --
        function library:watermark()
        	local watermark = {}
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = self.theme.accent,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,300,0,26),
        			Position = UDim2.new(1,-10,0,10),
        			ZIndex = 9900,
        			Visible = false,
        			Parent = self.screen
        		}
        	)
        	--
        	table.insert(self.themeitems["accent"]["BackgroundColor3"],outline)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9901,
        			Parent = outline
        		}
        	)
        	--
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9902,
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.font,
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextXAlignment = "Left",
        			TextSize = self.textsize,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local con
        	con = title:GetPropertyChangedSignal("TextBounds"):Connect(function()
        		outline.Size = UDim2.new(0,title.TextBounds.X+20,0,26)
        	end)
        	--
        	watermark = {
        		["outline"] = outline,
        		["outline2"] = outline2,
        		["indent"] = indent,
        		["title"] = title,
        		["connection"] = con
        	}
        	--
        	self.labels[#self.labels+1] = title
        	--
        	setmetatable(watermark,watermarks)
        	return watermark
        end
        --
        function watermarks:update(content)
        	local content = content or {}
        	local watermark = self
        	--
        	local text = ""
        	--
        	for i,v in pairs(content) do
        		text = text..i..": "..v.."  "
        	end
        	--
        	text = text:sub(0, -3)
        	--
        	watermark.title.Text = text
        end
        --
        function watermarks:updateside(side)
        	side = utility.removespaces(tostring(side):lower())
        	--
        	local sides = {
        		topright = {
        			AnchorPoint = Vector2.new(1,0),
        			Position = UDim2.new(1,-10,0,10)
        		},
        		topleft = {
        			AnchorPoint = Vector2.new(0,0),
        			Position = UDim2.new(0,10,0,10)
        		},
        		bottomright = {
        			AnchorPoint = Vector2.new(1,1),
        			Position = UDim2.new(1,-10,1,-10)
        		},
        		bottomleft = {
        			AnchorPoint = Vector2.new(0,1),
        			Position = UDim2.new(0,10,1,-10)
        		}
        	}
        	--
        	if sides[side] then
        		self.outline.AnchorPoint = sides[side].AnchorPoint
        		self.outline.Position = sides[side].Position
        	end
        end
        --
        function library:loader(props)
        	local name = props.name or props.Name or props.LoaderName or props.Loadername or props.loaderName or props.loadername or "Loader"
        	local scriptname = props.scriptname or props.Scriptname or props.ScriptName or props.scriptName or "Universal"
        	local closed = props.close or props.Close or props.closecallback or props.Closecallback or props.CloseCallback or props.closeCallback or function()end
        	local logedin = props.login or props.Login or props.logincallback or props.Logincallback or props.LoginCallback or props.loginCallback or function()end
        	local loader = {}
        	--
        	local screen = utility.new(
        		"ScreenGui",
        		{
        			Name = tostring(math.random(0,999999))..tostring(math.random(0,999999)),
        			DisplayOrder = 9999,
        			ResetOnSpawn = false,
        			ZIndexBehavior = "Global",
        			Parent = cre
        		}
        	)
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(168, 52, 235),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,300,0,90),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9900,
        			Visible = false,
        			Parent = screen
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9901,
        			Parent = outline
        		}
        	)
        	--
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9902,
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = "RobotoMono",
        			Text = name,
        			TextColor3 = Color3.fromRGB(168, 52, 235),
        			TextXAlignment = "Center",
        			TextSize = 12,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local scripttitle = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,20),
        			Font = "RobotoMono",
        			Text = "Script: "..scriptname,
        			TextColor3 = Color3.fromRGB(255, 255, 255),
        			TextXAlignment = "Center",
        			TextSize = 12,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local makebutton = function(name,parent)
        		local button_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 9904,
        				Parent = parent
        			}
        		)
        		--
        		local button_outline = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 9905,
        				Parent = button_holder
        			}
        		)
        		--
        		local button_outline2 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 9906,
        				Parent = button_outline
        			}
        		)
        		--
        		local button_color = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 9907,
        				Parent = button_outline2
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = button_color
        			}
        		)
        		--
        		local button_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = 12,
        				TextStrokeTransparency = 0,
        				Font = "RobotoMono",
        				ZIndex = 9908,
        				Parent = button_holder
        			}
        		)
        		--
        		return {button_holder,button_outline,button_button}
        	end
        	--
        	local close = makebutton("close",indent)
        	local login = makebutton("login",indent)
        	--
        	close[1].AnchorPoint = Vector2.new(0.5,0)
        	close[1].Size = UDim2.new(0.5,0,0,20)
        	close[1].Position = UDim2.new(0.5,0,0,40)
        	--
        	login[1].AnchorPoint = Vector2.new(0.5,0)
        	login[1].Size = UDim2.new(0.5,0,0,20)
        	login[1].Position = UDim2.new(0.5,0,0,62)
        	--
        	close[3].MouseButton1Down:Connect(function()
        		close[2].BorderColor3 = Color3.fromRGB(168, 52, 235)
        		outline:TweenPosition(UDim2.new(-1.5,0,0.5,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.75,true)
        		closed()
        		wait(0.05)
        		close[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait(0.7)
        		screen:Remove()
        	end)
        	--
        	login[3].MouseButton1Down:Connect(function()
        		login[2].BorderColor3 = Color3.fromRGB(168, 52, 235)
        		outline:TweenPosition(UDim2.new(1.5,0,0.5,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.75,true)
        		logedin()
        		wait(0.05)
        		login[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait(0.7)
        		screen:Remove()
        	end)
        	--
        	loader = {
        		["outline"] = outline,
        		["outline2"] = outline2,
        		["indent"] = indent,
        		["title"] = title
        	}
        	--
        	setmetatable(loader,loaders)
        	return loader
        end
        --
        function loaders:toggle()
        	self.outline.Visible = true
        end
        --
        function watermarks:toggle(bool)
        	local watermark = self
        	--
        	watermark.outline.Visible = bool
        end
        --
        function library:saveconfig()
        	local cfg = {}
        	--
        	for i,v in pairs(self.pointers) do
        		cfg[i] = {}
        		for c,d in pairs(v) do
        			cfg[i][c] = {}
        			for x,z in pairs(d) do
        				if typeof(z.current) == "Color3" then
        					cfg[i][c][x] = {z.current.R,z.current.G,z.current.B}
        				else
        					cfg[i][c][x] = z.current
        				end
        			end
        		end
        	end
        	--
        	return hs:JSONEncode(cfg)
        end
        --
        function library:loadconfig(cfg)
        	local cfg = hs:JSONDecode(readfile(cfg))
        	for i,v in pairs(cfg) do
        		for c,d in pairs(v) do
        			for x,z in pairs(d) do
        				if z ~= nil then
        					if self.pointers[i] ~= nil and self.pointers[i][c] ~= nil and self.pointers[i][c][x] ~= nil then
        						self.pointers[i][c][x]:set(z)
        					end
        				end
        			end
        		end
        	end
        end
        --
        function library:settheme(theme,color)
        	local window = self
        	--
        	if window.theme[theme] then
        		window.theme[theme] = color
        	end
        	--
        	if window.themeitems[theme] then
        		for i,v in pairs(window.themeitems[theme]) do
        			for z,x in pairs(v) do
        				x[i] = color
        			end
        		end
        	end
        end
        --
        function library:setkey(key)
        	if typeof(key) == "EnumItem" then
        		local window = self
        		window.key = key
        	end
        end
        --
        function library:settoggle(side,bool)
        	if side == "x" then
        		self.x = bool
        	else
        		self.y = bool
        	end
        end
        --
        function library:setfont(font)
        	if font ~= nil then
        		local window = self
        		for i,v in pairs(window.labels) do
        			if v ~= nil then
        				v.Font = font
        			end
        		end
        	end
        end
        --
        function library:settextsize(size)
        	if size ~= nil then
        		local window = self
        		for i,v in pairs(window.labels) do
        			if v ~= nil then
        				v.TextSize = size
        			end
        		end
        	end
        end
        --
        function library:page(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	-- // variables
        	local page = {}
        	-- // main
        	local tabbutton = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,75,1,0),
        			Parent = self.tabsbuttons
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabbutton
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = tabbutton
        		}
        	)
        	--
        	local r_line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(1,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local l_line = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(0,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local label = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.textsize,
        			TextStrokeTransparency = 0,
        			Parent = outline
        		}
        	)
        	--
        	local pageholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,-20),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Visible = false,
        			Parent = self.tabs
        		}
        	)
        	--
        	local left = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(0,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = true,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,10),
        			Parent = left
        		}
        	)
        	--
        	local right = utility.new(
        		"ScrollingFrame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(1,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = true,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,10),
        			Parent = right
        		}
        	)
        	-- // page tbl
        	page = {
        		["library"] = self,
        		["outline"] = outline,
        		["r_line"] = r_line,
        		["l_line"] = l_line,
        		["line"] = line,
        		["page"] = pageholder,
        		["left"] = left,
        		["right"] = right,
        		["open"] = false,
        		["pointers"] = {}
        	}
        	--
        	table.insert(self.pages,page)
        	--
        	button.MouseButton1Down:Connect(function()
        		if page.open == false then
        			for i,v in pairs(self.pages) do
        				if v ~= page then
        					if v.open then
        						v.page.Visible = false
        						v.open = false
        						v.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        						v.line.Size = UDim2.new(1,0,0,2)
        						v.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        					end
        				end
        			end
        			--
        			self:closewindows()
        			--
        			page.page.Visible = true
        			page.open = true
        			page.outline.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			page.line.Size = UDim2.new(1,0,0,3)
        			page.line.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		self.pointers[tostring(pointer)] = page.pointers
        	end
        	--
        	self.labels[#self.labels+1] = label
        	-- // metatable indexing + return
        	setmetatable(page, pages)
        	return page
        end
        --
        function pages:openpage()
        	local page = self
        	--
        	if page.open == false then
        		for i,v in pairs(page.library.pages) do
        			if v ~= page then
        				if v.open then
        					v.page.Visible = false
        					v.open = false
        					v.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        					v.line.Size = UDim2.new(1,0,0,2)
        					v.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        				end
        			end
        		end
        		--
        		page.page.Visible = true
        		page.open = true
        		page.outline.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        		page.line.Size = UDim2.new(1,0,0,3)
        		page.line.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        	end
        end
        --
        function pages:section(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local side = props.side or props.Side or props.sectionside or props.Sectionside or props.SectionSide or props.sectionSide or "left"
        	local size = props.size or props.Size or props.yaxis or props.yAxis or props.YAxis or props.Yaxis or 200
        	side = side:lower()
        	-- // variables
        	local section = {}
        	-- // main
        	local sectionholder = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,size),
        			Parent = self[side]
        		}
        	)
        
        	--[[BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(0,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = false,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}]]
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = sectionholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	--[[local content = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-12,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			Parent = outline
        		}
        	)]]
        
        	local content = utility.new(
        		'Frame',
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-12,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-5,0,20),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,5),
        			Parent = content
        		}
        	)
        	-- // section tbl
        	section = {
        		["library"] = self.library,
        		["sectionholder"] = sectionholder,
        		["color"] = color,
        		["content"] = content,
        		["pointers"] = {}
        	}
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = section.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(section, sections)
        	return section
        end
        --
        function pages:multisection(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local side = props.side or props.Side or props.sectionside or props.Sectionside or props.SectionSide or props.sectionSide or "left"
        	local size = props.size or props.Size or props.yaxis or props.yAxis or props.YAxis or props.Yaxis or 200
        	side = side:lower()
        	-- // variables
        	local multisection = {}
        	-- // main
        	local sectionholder = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,size),
        			Parent = self[side]
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = sectionholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local tabsholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,-15),
        			Position = UDim2.new(0,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-5,0,20),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = outline
        		}
        	)
        	--
        	local buttons = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-6,0,20),
        			Position = UDim2.new(0.5,0,0,5),
        			Parent = tabsholder
        		}
        	)
        	--
        	local tabs = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-6,1,-27),
        			Position = UDim2.new(0.5,0,1,-3),
        			Parent = tabsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Horizontal",
        			Padding = UDim.new(0,2),
        			Parent = buttons
        		}
        	)
        	--
        	local tabs_outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabs
        		}
        	)
        	-- // section tbl
        	multisection = {
        		["library"] = self.library,
        		["sectionholder"] = sectionholder,
        		["color"] = color,
        		["tabsholder"] = tabsholder,
        		["mssections"] = {},
        		["buttons"] = buttons,
        		["tabs"] = tabs,
        		["tabs_outline"] = tabs_outline,
        		["pointers"] = {}
        	}
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = multisection.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(multisection,multisections)
        	return multisection
        end
        --
        function multisections:section(props)
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	-- // variables
        	local mssection = {}
        	-- // main
        	local tabbutton = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,60,0,20),
        			Parent = self.buttons
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabbutton
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = tabbutton
        		}
        	)
        	--
        	local r_line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(1,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local l_line = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(0,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local label = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Parent = outline
        		}
        	)
        	--
        	local content = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-6,1,-27),
        			Position = UDim2.new(0.5,0,1,-3),
        			Parent = self.tabs_outline
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,5),
        			Parent = content
        		}
        	)
        	-- // mssection tbl
        	mssection = {
        		["library"] = self.library,
        		["outline"] = outline,
        		["r_line"] = r_line,
        		["l_line"] = l_line,
        		["line"] = line,
        		["content"] = content,
        		["open"] = false,
        		["pointers"] = {}
        	}
        	--
        	table.insert(self.mssections,mssection)
        	--
        	button.MouseButton1Down:Connect(function()
        		if mssection.open == false then
        			for i,v in pairs(self.mssections) do
        				if v ~= mssection then
        					if v.open then
        						v.page.Visible = false
        						v.open = false
        						v.outline.BackgroundColor3 = Color3.fromRGB(31, 31 ,31)
        						v.line.Size = UDim2.new(1,0,0,2)
        						v.line.BackgroundColor3 = Color3.fromRGB(31, 31 ,31)
        					end
        				end
        			end
        			--
        			mssection.library:closewindows()
        			--
        			mssection.content.Visible = true
        			mssection.open = true
        			mssection.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        			mssection.line.Size = UDim2.new(1,0,0,3)
        			mssection.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = mssection.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = label
        	-- // metatable indexing + return
        	setmetatable(mssection,mssections)
        	return mssection
        end
        --
        function sections:toggle(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or props.toggle or props.Toggle or props.toggled or props.Toggled or false
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local toggle = {}
        	-- // main
        	local toggleholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,15,0,15),
        			Parent = toggleholder
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = toggleholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,20,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = toggleholder
        		}
        	)
        	--
        	local col = Color3.fromRGB(20, 20, 20)
        	if def then
        		col = self.library.theme.accent
        	end
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = col,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	if def then
        		table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	end
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	-- // toggle tbl
        	toggle = {
        		["library"] = self.library,
        		["toggleholder"] = toggleholder,
        		["title"] = title,
        		["color"] = color,
        		["callback"] = callback,
        		["current"] = def
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		if toggle.current then
        			toggle.callback(false)
        			toggle.color.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			local find = table.find(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BackgroundColor3"],find)
        			end
        			toggle.current = false
        		else
        			toggle.callback(true)
        			toggle.color.BackgroundColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			toggle.current = true
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = toggle
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(toggle, toggles)
        	return toggle
        end
        --
        function toggles:set(bool)
        	if bool ~= nil then
        		local toggle = self
        		toggle.callback(bool)
        		toggle.current = bool
        		if bool then
        			toggle.color.BackgroundColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        		else
        			toggle.color.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			local find = table.find(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BackgroundColor3"],find)
        			end
        		end
        	end
        end
        --
        function sections:button(props)
        	-- // properties
        	local name = props.name or props.Name or "new button"
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local button = {}
        	-- // main
        	local buttonholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = buttonholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	local gradient = utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local buttonpress = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = buttonholder
        		}
        	)
        	--
        	buttonpress.MouseButton1Down:Connect(function()
        		callback()
        		outline.BorderColor3 = self.library.theme.accent
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        		wait(0.05)
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end)
        	-- // button tbl
        	button = {
        		["library"] = self.library
        	}
        	--
        	self.library.labels[#self.library.labels+1] = buttonpress
        	-- // metatable indexing + return
        	setmetatable(button, buttons)
        	return button
        end
        --
        function sections:slider(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or 0
        	local max = props.max or props.Max or props.maximum or props.Maximum or 100
        	local min = props.min or props.Min or props.minimum or props.Minimum or 0
        	local rounding = props.rounding or props.Rounding or props.round or props.Round or props.decimals or props.Decimals or false
        	local ticking = props.tick or props.Tick or props.ticking or props.Ticking or false
        	local measurement = props.measurement or props.Measurement or props.digit or props.Digit or props.calc or props.Calc or ""
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	def = math.clamp(def,min,max)
        	-- // variables
        	local slider = {}
        	-- // main
        	local sliderholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,25),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,12),
        			Position = UDim2.new(0,0,0,15),
        			Parent = sliderholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)	
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,0.5,0),
        			Font = self.library.font,
        			Text = def..measurement.."/"..max..measurement,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			ZIndex = 3,
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local slide = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new((1 / color.AbsoluteSize.X) * (color.AbsoluteSize.X / (max - min) * (def - min)),0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],slide)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = slide
        		}
        	)
        	--
        	local sliderbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = sliderholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = sliderholder
        		}
        	)
        	-- // slider tbl
        	slider = {
        		["library"] = self.library,
        		["outline"] = outline,
        		["sliderbutton"] = sliderbutton,
        		["title"] = title,
        		["value"] = value,
        		["slide"] = slide,
        		["color"] = color,
        		["max"] = max,
        		["min"] = min,
        		["current"] = def,
        		["measurement"] = measurement,
        		["tick"] = ticking,
        		["rounding"] = rounding,
        		["callback"] = callback
        	}
        	--
        	local function slide()
        		local size = math.clamp(plr:GetMouse().X - slider.color.AbsolutePosition.X ,0 ,slider.color.AbsoluteSize.X)
        		local result = (slider.max - slider.min) / slider.color.AbsoluteSize.X * size + slider.min
        		if slider.rounding then
        			local newres = math.floor(result)
        			value.Text = newres..slider.measurement.."/"..slider.max..slider.measurement
        			slider.current = newres
        			slider.callback(newres)
        			if slider.tick then
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * (slider.color.AbsoluteSize.X / (slider.max - slider.min) * (newres - slider.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			else
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			end
        		else
        			local newres = utility.round(result ,2)
        			value.Text = newres..slider.measurement.."/"..slider.max..slider.measurement
        			slider.current = newres
        			slider.callback(newres)
        			if slider.tick then
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * (slider.color.AbsoluteSize.X / (slider.max - slider.min) * (newres - slider.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			else
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			end
        		end
        	end
        	--
        	sliderbutton.MouseButton1Down:Connect(function()
        		slider.holding = true
        		slide()
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        		outline.BorderColor3 = self.library.theme.accent
        	end)
        	--
        	uis.InputChanged:Connect(function()
        		if slider.holding then
        			slide()
        		end
        	end)
        	--
        	uis.InputEnded:Connect(function(Input)
        		if Input.UserInputType.Name == 'MouseButton1' and slider.holding then
        			slider.holding = false
        			outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        			local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        			end
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = slider
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(slider, sliders)
        	return slider
        end
        --
        function sliders:set(value)
        	local size = math.clamp((self.color.AbsoluteSize.X / (self.max - self.min) * (value - self.min)) ,0 ,self.color.AbsoluteSize.X)
        	local result = value
        	if self.rounding then
        		local newres = math.floor(result)
        		self.value.Text = newres..self.measurement.."/"..self.max..self.measurement
        		self.current = newres
        		self.callback(newres)
        		if self.tick then
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * (self.color.AbsoluteSize.X / (self.max - self.min) * (newres - self.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		else
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		end
        	else
        		local newres = utility.round(result ,2)
        		self.value.Text = newres..self.measurement.."/"..self.max..self.measurement
        		self.current = newres
        		self.callback(newres)
        		if self.tick then
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * (self.color.AbsoluteSize.X / (self.max - self.min) * (newres - self.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		else
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		end
        	end
        end
        --
        function library:closewindows(ignore)
        	local window = self
        	--
        	for i,v in pairs(window.dropdowns) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.multiboxes) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.buttonboxs) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.colorpickers) do
        		if v ~= ignore then
        			if v.open then
        				v.cpholder.Visible = false
        				v.open = false
        			end
        		end
        	end
        end
        --
        function sections:dropdown(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local dropdown = {}
        	-- // main
        	local dropdownholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = dropdownholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = def,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = dropdownholder
        		}
        	)
        	--
        	local dropdownbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = dropdownholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = dropdownholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // dropdown tbl
        	dropdown = {
        		["library"] = self.library,
        		["optionsholder"] = optionsholder,
        		["indicator"] = indicator,
        		["options"] = options,
        		["title"] = title,
        		["value"] = value,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(dropdown.library.dropdowns,dropdown)
        	--
        	for i,v in pairs(options) do
        		local ddoptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local ddoptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = ddoptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = ddoptiontitle
        		--
        		table.insert(dropdown.titles,ddoptiontitle)
        		--
        		if v == dropdown.current then ddoptiontitle.TextColor3 = self.library.theme.accent end
        		--
        		ddoptionbutton.MouseButton1Down:Connect(function()
        			optionsholder.Visible = false
        			dropdown.open = false
        			indicator.Text = "+"
        			for z,x in pairs(dropdown.titles) do
        				if x.TextColor3 == self.library.theme.accent then
        					x.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        			end
        			dropdown.current = v
        			dropdown.value.Text = v
        			ddoptiontitle.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],ddoptiontitle)
        			dropdown.callback(v)
        		end)
        	end
        	--
        	dropdownbutton.MouseButton1Down:Connect(function()
        		dropdown.library:closewindows(dropdown)
        		for i,v in pairs(dropdown.titles) do
        			if v.Text == dropdown.current then
        				v.TextColor3 = dropdown.library.theme.accent
        			else
        				v.TextColor3 = Color3.fromRGB(255,255,255)
        			end
        		end
        		optionsholder.Visible = not dropdown.open
        		dropdown.open = not dropdown.open
        		if dropdown.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = dropdown
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(dropdown, dropdowns)
        	return dropdown
        end
        --
        function sections:buttonbox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local buttonbox = {}
        	-- // main
        	local buttonboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local buttonboxbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // buttonbox tbl
        	buttonbox = {
        		["library"] = self.library,
        		["optionsholder"] = optionsholder,
        		["indicator"] = indicator,
        		["options"] = options,
        		["title"] = title,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(buttonbox.library.buttonboxs,buttonbox)
        	--
        	for i,v in pairs(options) do
        		local bboptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local bboptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = bboptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = bboptiontitle
        		--
        		table.insert(buttonbox.titles,bboptiontitle)
        		--
        		bboptionbutton.MouseButton1Down:Connect(function()
        			optionsholder.Visible = false
        			buttonbox.open = false
        			indicator.Text = "+"
        			buttonbox.current = v
        			buttonbox.callback(v)
        		end)
        	end
        	--
        	buttonboxbutton.MouseButton1Down:Connect(function()
        		buttonbox.library:closewindows(buttonbox)
        		optionsholder.Visible = not buttonbox.open
        		buttonbox.open = not buttonbox.open
        		if buttonbox.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = buttonbox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(buttonbox, buttonboxs)
        	return buttonbox
        end
        --
        function dropdowns:set(value)
        	if value ~= nil then
        		local dropdown = self
        		if table.find(dropdown.options,value) then
        			self.current = tostring(value)
        			self.value.Text = tostring(value)
        			self.callback(tostring(value))
        			for z,x in pairs(dropdown.titles) do
        				if x.Text == value then
        					x.TextColor3 = dropdown.library.theme.accent
        				else
        					x.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        			end
        		end
        	end
        end
        --
        function sections:multibox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or {}
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	local defstr = ""
        	if #def > 1 then
        		for i,v in pairs(def) do
        			if i == #def then
        				defstr = defstr..v
        			else
        				defstr = defstr..v..", "
        			end
        		end
        	else
        		for i,v in pairs(def) do
        			defstr = defstr..v
        		end
        	end
        	-- // variables
        	local multibox = {}
        	-- // main
        	local multiboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = multiboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = defstr,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = multiboxholder
        		}
        	)
        	--
        	local dropdownbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = multiboxholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = multiboxholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // dropdown tbl
        	multibox = {
        		["library"] = self.library,
        		["indicator"] = indicator,
        		["optionsholder"] = optionsholder,
        		["options"] = options,
        		["value"] = value,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(multibox.library.multiboxes,multibox)
        	--
        	for i,v in pairs(options) do
        		local ddoptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local ddoptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = ddoptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = ddoptiontitle
        		--
        		table.insert(multibox.titles,ddoptiontitle)
        		--
        		for c,b in pairs(def) do if v == b then ddoptiontitle.TextColor3 = self.library.theme.accent end end
        		--
        		ddoptionbutton.MouseButton1Down:Connect(function()
        			local find = table.find(multibox.current,v)
        			if find == nil then
        				table.insert(multibox.current,v)
        				local str = ""
        				if #multibox.current > 1 then
        					for i,v in pairs(multibox.current) do
        						if i == #multibox.current then
        							str = str..v
        						else
        							str = str..v..", "
        						end
        					end
        				else
        					for i,v in pairs(multibox.current) do
        						str = str..v
        					end
        				end
        				value.Text = str
        				ddoptiontitle.TextColor3 = self.library.theme.accent
        				table.insert(self.library.themeitems["accent"]["TextColor3"],ddoptiontitle)
        				multibox.callback(multibox.current)
        			else
        				table.remove(multibox.current,find)
        				local str = ""
        				if #multibox.current > 1 then
        					for i,v in pairs(multibox.current) do
        						if i == #multibox.current then
        							str = str..v
        						else
        							str = str..v..", "
        						end
        					end
        				else
        					for i,v in pairs(multibox.current) do
        						str = str..v
        					end
        				end
        				value.Text = str
        				ddoptiontitle.TextColor3 = Color3.fromRGB(255,255,255)
        				multibox.callback(multibox.current)
        			end
        		end)
        	end
        	--
        	dropdownbutton.MouseButton1Down:Connect(function()
        		multibox.library:closewindows(multibox)
        		for i,v in pairs(multibox.titles) do
        			if v.TextColor3 ~= Color3.fromRGB(255,255,255) then
        				v.TextColor3 = self.library.theme.accent
        			end
        		end
        		optionsholder.Visible = not multibox.open
        		multibox.open = not multibox.open
        		if multibox.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = multibox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = value
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(multibox, multiboxs)
        	return multibox
        end
        --
        function buttonboxs:set(value)
        	if value ~= nil then
        		local dropdown = self
        		if table.find(dropdown.options,value) then
        			self.current = tostring(value)
        			self.callback(tostring(value))
        		end
        	end
        end
        --
        function multiboxs:set(tbl)
        	if tbl then
        		local multibox = self
        		if typeof(tbl) == "table" then
        			multibox.current = {}
        			for i,v in pairs(tbl) do
        				if table.find(multibox.options,v) then
        					table.insert(multibox.current,v)
        				end
        			end
        			--
        			for i,v in pairs(multibox.titles) do
        				if v.TextColor3 == multibox.library.theme.accent then
        					v.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        				if table.find(tbl,v.Text) then
        					v.TextColor3 = multibox.library.theme.accent
        				end
        			end
        			--
        			local str = ""
        			if #multibox.current > 1 then
        				for i,v in pairs(multibox.current) do
        					if i == #multibox.current then
        						str = str..v
        					else
        						str = str..v..", "
        					end
        				end
        			else
        				for i,v in pairs(multibox.current) do
        					str = str..v
        				end
        			end
        			--
        			multibox.value.Text = str
        		end
        	end
        end
        --
        function sections:textbox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local placeholder = props.placeholder or props.Placeholder or props.placeHolder or props.PlaceHolder or props.placeholdertext or props.PlaceHolderText or props.PlaceHoldertext or props.placeHolderText or props.placeHoldertext or props.Placeholdertext or props.PlaceholderText or props.placeholderText or ""
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local textbox = {}
        	-- // main
        	local textboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = textboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	local gradient = utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = textboxholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = textboxholder
        		}
        	)
        	--
        	local tbox = utility.new(
        		"TextBox",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,15),
        			PlaceholderText = placeholder,
        			Text = def,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextTruncate = "AtEnd",
        			Font = self.library.font,
        			Parent = textboxholder
        		}
        	)
        	-- // textbox tbl
        	textbox = {
        		["library"] = self.library,
        		["tbox"] = tbox,
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		tbox:CaptureFocus()
        	end)
        	--
        	tbox.Focused:Connect(function()
        		outline.BorderColor3 = self.library.theme.accent
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        	end)
        	--
        	tbox.FocusLost:Connect(function(enterPressed)
        		textbox.current = tbox.Text
        		callback(tbox.Text)
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = textbox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = tbox
        	-- // metatable indexing + return
        	setmetatable(textbox, textboxs)
        	return textbox
        end
        --
        function textboxs:set(value)
        	self.tbox.Text = value
        	self.current = value
        	self.callback(value)
        end
        --
        function sections:keybind(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or nil
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	local allowed = props.allowed or props.Allowed or 1
        	--
        	local default = ".."
        	local typeis = nil
        	--
        	if typeof(def) == "EnumItem" then
        		if def == Enum.UserInputType.MouseButton1 then
        			if allowed == 1 then
        				default = "MB1"
        				typeis = "UserInputType"
        			end
        		elseif def == Enum.UserInputType.MouseButton2 then
        			if allowed == 1 then
        				default = "MB2"
        				typeis = "UserInputType"
        			end
        		elseif def == Enum.UserInputType.MouseButton3 then
        			if allowed == 1 then
        				default = "MB3"
        				typeis = "UserInputType"
        			end
        		else
        			local capd = utility.capatalize(def.Name)
        			if #capd > 1 then
        				default = capd
        			else
        				default = def.Name
        			end
        			typeis = "KeyCode"
        		end
        	end
        	-- // variables
        	local keybind = {}
        	-- // main
        	local keybindholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,17),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,40,1,0),
        			Position = UDim2.new(1,0,0,0),
        			Parent = keybindholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = default,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = keybindholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = keybindholder
        		}
        	)
        	-- // keybind tbl
        	keybind = {
        		["library"] = self.library,
        		["down"] = false,
        		["outline"] = outline,
        		["value"] = value,
        		["allowed"] = allowed,
        		["current"] = {typeis,utility.splitenum(def)},
        		["pressed"] = false,
        		["callback"] = callback
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		if keybind.down == false then
        			outline.BorderColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        			wait()
        			keybind.down = true
        		end
        	end)
        	--
        	button.MouseButton2Down:Connect(function()
        		keybind.down = false
        		keybind.current = {nil,nil}
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        		value.Text = ".."
        		outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        	end)
        	--
        	local function turn(typeis,current)
        		outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        		keybind.down = false
        		keybind.current = {typeis,utility.splitenum(current)}
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end
        	--
        	uis.InputBegan:Connect(function(Input)
        		if keybind.down then
        			if Input.UserInputType == Enum.UserInputType.Keyboard then
        				local capd = utility.capatalize(Input.KeyCode.Name)
        				if #capd > 1 then
        					value.Text = capd
        				else
        					value.Text = Input.KeyCode.Name
        				end
        				turn("KeyCode",Input.KeyCode)
        				callback(Input.KeyCode)
        			end
        			if allowed == 1 then
        				if Input.UserInputType == Enum.UserInputType.MouseButton1 then
        					value.Text = "MB1"
        					turn("UserInputType",Input)
        					callback(Input)
        				elseif Input.UserInputType == Enum.UserInputType.MouseButton2 then
        					value.Text = "MB2"
        					turn("UserInputType",Input)
        					callback(Input)
        				elseif Input.UserInputType == Enum.UserInputType.MouseButton3 then
        					value.Text = "MB3"
        					turn("UserInputType",Input)
        					callback(Input)
        				end
        			end
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = keybind
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(keybind, keybinds)
        	return keybind
        end
        --
        function keybinds:set(key)
        	if key then
        		if typeof(key) == "EnumItem" or typeof(key) == "table" then
        			if typeof(key) == "table" then
        				if key[1] and key[2] then
        					key = Enum[key[1]][key[2]]
        				else
        					return
        				end
        			end
        			local keybind = self
        			local typeis = ""
        			--
        			local default = ".."
        			--
        			if key == Enum.UserInputType.MouseButton1 then
        				if keybind.allowed == 1 then
        					default = "MB1"
        					typeis = "UserInputType"
        				end
        			elseif key == Enum.UserInputType.MouseButton2 then
        				if keybind.allowed == 1 then
        					default = "MB2"
        					typeis = "UserInputType"
        				end
        			elseif key == Enum.UserInputType.MouseButton3 then
        				if keybind.allowed == 1 then
        					default = "MB3"
        					typeis = "UserInputType"
        				end
        			else
        				local capd = utility.capatalize(key.Name)
        				if #capd > 1 then
        					default = capd
        				else
        					default = key.Name
        				end
        				typeis = "KeyCode"
        			end
        			--
        			keybind.value.Text = default
        			keybind.current = {typeis,utility.splitenum(key)}
        			keybind.callback(keybind.current)
        			keybind.outline.Size = UDim2.new(0,keybind.value.TextBounds.X+20,1,0)
        			--
        			if keybind.down then
        				keybind.down = false
        				keybind.outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        				local find = table.find(self.library.themeitems["accent"]["BorderColor3"],keybind.outline)
        				if find then
        					table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        				end
        			end
        		end
        	end
        end
        --
        function sections:colorpicker(props)
        	-- // properties
        	local name = props.name or props.Name or "new colorpicker"
        	local cpname = props.cpname or props.Cpname or props.CPname or props.CPName or props.cPname or props.cpName or props.colorpickername or nil
        	local def = props.def or props.Def or props.default or props.Default or Color3.fromRGB(255,255,255)
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	--
        	local h,s,v = def:ToHSV()
        	-- // variables
        	local colorpicker = {}
        	-- // main
        	local colorpickerholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,30,1,0),
        			Position = UDim2.new(1,0,0,0),
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local cpcolor = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = def,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = cpcolor
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local cpholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,230),
        			Position = UDim2.new(0,0,1,5),
        			Visible = false,
        			ZIndex = 5,
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = cpholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local cptitle = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = cpname or name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local cpholder2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0.875,0,0,150),
        			Position = UDim2.new(0,5,0,20),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local outline3 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromHSV(h,1,1),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = cpholder2
        		}
        	)
        	--
        	local cpimage = utility.new(
        		"ImageButton",
        		{
        			AutoButtonColor = false,
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Image = "rbxassetid://7074305282",
        			Parent = outline3
        		}
        	)
        	--
        	local cpcursor = utility.new(
        		"ImageLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,6,0,6),
        			Position = UDim2.new(s,0,1-v,0),
        			ZIndex = 5,
        			Image = "rbxassetid://7074391319",
        			Parent = cpimage
        		}
        	)
        	--
        	local huepicker = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0.05,0,0,150),
        			Position = UDim2.new(1,-5,0,20),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local outline4 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(255, 255, 255),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = huepicker
        		}
        	)
        	--
        	local huebutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			ZIndex = 5,
        			Parent = huepicker
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(0.10, Color3.fromRGB(255, 153, 0)), ColorSequenceKeypoint.new(0.20, Color3.fromRGB(209, 255, 0)), ColorSequenceKeypoint.new(0.30, Color3.fromRGB(55, 255, 0)), ColorSequenceKeypoint.new(0.40, Color3.fromRGB(0, 255, 102)), ColorSequenceKeypoint.new(0.50, Color3.fromRGB(0, 255, 255)), ColorSequenceKeypoint.new(0.60, Color3.fromRGB(0, 102, 255)), ColorSequenceKeypoint.new(0.70, Color3.fromRGB(51, 0, 255)), ColorSequenceKeypoint.new(0.80, Color3.fromRGB(204, 0, 255)), ColorSequenceKeypoint.new(0.90, Color3.fromRGB(255, 0, 153)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 4))},
        			Rotation = 90,
        			Parent = outline4
        		}
        	)
        	--
        	local huecursor = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(255, 255, 255),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,12,0,6),
        			Position = UDim2.new(0.5,0,h,0),
        			ZIndex = 5,
        			Parent = outline4
        		}
        	)
        	--
        	local huecursor_inline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromHSV(h,1,1),
        			BorderColor3 = Color3.fromRGB(255, 255, 255),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			ZIndex = 5,
        			Parent = huecursor
        		}
        	)
        	--
        	local function textbox(parent,size,position)
        		local textbox_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				Position = position,
        				Size = size,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local outline5 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local outline6 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = outline5
        			}
        		)
        		--
        		local color2 = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = outline6
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = color2
        			}
        		)
        		--
        		local tbox = utility.new(
        			"TextBox",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				PlaceholderColor3 = Color3.fromRGB(255,255,255),
        				PlaceholderText = "",
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local tbox_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		tbox_button.MouseButton1Down:Connect(function()
        			tbox:CaptureFocus()
        		end)
        		--
        		return {textbox_holder,tbox,outline5}
        	end
        	--
        	local red = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	local green = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	green[1].AnchorPoint = Vector2.new(0.5,0)
        	green[1].Position = UDim2.new(0.5,0,0,175)
        	local blue = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	blue[1].AnchorPoint = Vector2.new(1,0)
        	blue[1].Position = UDim2.new(1,-5,0,175)
        	local hex = textbox(outline2,UDim2.new(1,-10,0,20),UDim2.new(0,5,0,200))
        	hex[2].Size = UDim2.new(1,-12,1,0)
        	hex[2].TextXAlignment = "Left"
        	-- // colorpicker tbl
        	colorpicker = {
        		["library"] = self.library,
        		["cpholder"] = cpholder,
        		["cpcolor"] = cpcolor,
        		["huecursor"] = huecursor,
        		["outline3"] = outline3,
        		["huecursor_inline"] = huecursor_inline,
        		["cpcursor"] = cpcursor,
        		["current"] = def,
        		["open"] = false,
        		["cp"] = false,
        		["hue"] = false,
        		["hsv"] = {h,s,v},
        		["red"] = red[2],
        		["green"] = green[2],
        		["blue"] = blue[2],
        		["hex"] = hex[2],
        		["callback"] = callback
        	}
        	--
        	table.insert(self.library.colorpickers,colorpicker)
        	--
        	local function updateboxes()
        		colorpicker.red.PlaceholderText = "R: "..tostring(math.floor(colorpicker.current.R*255))
        		colorpicker.green.PlaceholderText = "G: "..tostring(math.floor(colorpicker.current.G*255))
        		colorpicker.blue.PlaceholderText = "B: "..tostring(math.floor(colorpicker.current.B*255))
        		colorpicker.hex.PlaceholderText = "Hex: "..utility.to_hex(colorpicker.current)
        	end
        	--
        	updateboxes()
        	--
        	local function movehue()
        		local posy = math.clamp(plr:GetMouse().Y-outline3.AbsolutePosition.Y,0,outline3.AbsoluteSize.Y)
        		local resy = (1/outline3.AbsoluteSize.Y)*posy
        		outline3.BackgroundColor3 = Color3.fromHSV(resy,1,1)
        		huecursor_inline.BackgroundColor3 = Color3.fromHSV(resy,1,1)
        		colorpicker.hsv[1] = resy
        		colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        		cpcolor.BackgroundColor3 = colorpicker.current
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        		huecursor:TweenPosition(UDim2.new(0.5,0,resy,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        	end
        	--
        	local function movecp()
        		local posx,posy = math.clamp(plr:GetMouse().X-outline3.AbsolutePosition.X,0,outline3.AbsoluteSize.X),math.clamp(plr:GetMouse().Y-outline3.AbsolutePosition.Y,0,outline3.AbsoluteSize.Y)
        		local resx,resy = (1/outline3.AbsoluteSize.X)*posx,(1/outline3.AbsoluteSize.Y)*posy
        		colorpicker.hsv[2] = resx
        		colorpicker.hsv[3] = 1-resy
        		colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        		cpcolor.BackgroundColor3 = colorpicker.current
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        		cpcursor:TweenPosition(UDim2.new(resx,0,resy,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        	end
        	--
        	button.MouseButton1Down:Connect(function()
        		self.library:closewindows(colorpicker)
        		cpholder.Visible = not colorpicker.open
        		colorpicker.open = not colorpicker.open
        	end)
        	--
        	huebutton.MouseButton1Down:Connect(function()
        		colorpicker.hue = true
        		movehue()
        	end)
        	--
        	cpimage.MouseButton1Down:Connect(function()
        		colorpicker.cp = true
        		movecp()
        	end)
        	--
        	uis.InputChanged:Connect(function()
        		if colorpicker.cp then
        			movecp()
        		end
        		if colorpicker.hue then
        			movehue()
        		end
        	end)
        	--
        	uis.InputEnded:Connect(function(Input)
        		if Input.UserInputType.Name == 'MouseButton1'  then
        			if colorpicker.cp then
        				colorpicker.cp = false
        			end
        			if colorpicker.hue then
        				colorpicker.hue = false
        			end
        		end
        	end)
        	--
        	red[2].Focused:Connect(function()
        		red[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	red[2].FocusLost:Connect(function()
        		local saved = red[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			red[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					red[2].PlaceholderText = "R: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(tonumber(saved),colorpicker.current.G*255,colorpicker.current.B*255))
        				red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			red[2].Text = ""
        			red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	green[2].Focused:Connect(function()
        		green[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	green[2].FocusLost:Connect(function()
        		local saved = green[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			green[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					green[2].PlaceholderText = "G: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(colorpicker.current.R*255,tonumber(saved),colorpicker.current.B*255))
        				green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			green[2].Text = ""
        			green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	blue[2].Focused:Connect(function()
        		blue[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	blue[2].FocusLost:Connect(function()
        		local saved = blue[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			blue[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					blue[2].PlaceholderText = "B: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(colorpicker.current.R*255,colorpicker.current.G*255,tonumber(saved)))
        				blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			blue[2].Text = ""
        			blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	hex[2].Focused:Connect(function()
        		hex[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	hex[2].FocusLost:Connect(function()
        		local saved = hex[2].Text
        		if #saved >= 6 and #saved <= 7 then
        			local e,s = pcall(function()
        				utility.from_hex(saved)
        			end)
        			if e == true then
        				local hexcolor = utility.from_hex(saved)
        				if hexcolor then
        					colorpicker:set(hexcolor)
        					hex[2].Text = ""
        					hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        				else
        					hex[2].Text = ""
        					hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        				end
        			else
        				hex[2].Text = ""
        				hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			hex[2].Text = ""
        			hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = colorpicker
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = hex[2]
        	self.library.labels[#self.library.labels+1] = red[2]
        	self.library.labels[#self.library.labels+1] = green[2]
        	self.library.labels[#self.library.labels+1] = blue[2]
        	self.library.labels[#self.library.labels+1] = cptitle
        	-- // metatable indexing + return
        	setmetatable(colorpicker, colorpickers)
        	return colorpicker
        end
        --
        function colorpickers:set(color)
        	if color then
        		if typeof(color) == "table" then
        			color = Color3.fromRGB(color[1]*255,color[2]*255,color[3]*255)
        		end
        		local colorpicker = self
        		local h,s,v = color:ToHSV()
        		--
        		local function updateboxes()
        			colorpicker.red.PlaceholderText = "R: "..tostring(math.floor(colorpicker.current.R*255))
        			colorpicker.green.PlaceholderText = "G: "..tostring(math.floor(colorpicker.current.G*255))
        			colorpicker.blue.PlaceholderText = "B: "..tostring(math.floor(colorpicker.current.B*255))
        			colorpicker.hex.PlaceholderText = "Hex: "..utility.to_hex(colorpicker.current)
        		end
        		--
        		local function movehue()
        			colorpicker.outline3.BackgroundColor3 = Color3.fromHSV(h,1,1)
        			colorpicker.huecursor_inline.BackgroundColor3 = Color3.fromHSV(h,1,1)
        			colorpicker.hsv[1] = h
        			colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        			colorpicker.cpcolor.BackgroundColor3 = colorpicker.current
        			colorpicker.huecursor:TweenPosition(UDim2.new(0.5,0,h,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        		end
        		--
        		local function movecp()
        			colorpicker.hsv[2] = s
        			colorpicker.hsv[3] = v
        			colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        			colorpicker.cpcolor.BackgroundColor3 = colorpicker.current
        			colorpicker.cpcursor:TweenPosition(UDim2.new(s,0,1-v,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        		end
        		--
        		movehue()
        		movecp()
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        	end
        end
        --
        function sections:configloader(props)
        	-- // properties
        	local folder = props.folder or props.Folder
        	-- // variables
        	local configloader = {}
        	-- // main
        	local clholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,222),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = clholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,3),
        			Font = self.library.font,
        			Text = "configs",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	self.library.labels[#self.library.labels+1] = title
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-6,0,1),
        			Position = UDim2.new(0.5,0,0,19),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local buttonsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,64),
        			Position = UDim2.new(0,0,0,150),
        			Parent = outline
        		}
        	)
        	--
        	local configsholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-10,0,120),
        			Position = UDim2.new(0.5,0,0,25),
        			Parent = outline
        		}
        	)
        	--
        	local outline3 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = configsholder
        		}
        	)
        	--
        	local outline4 = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			Parent = outline3
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,0),
        			Parent = outline4
        		}
        	)
        	--
        	local createdbuttons = {}
        	local selected
        	--
        	local makebutton = function(name,toggled)
        		local createdbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				Parent = outline4
        			}
        		)
        		--
        		local grey = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundColor3 = Color3.fromRGB(125, 125, 125),
        				BackgroundTransparency = 0.9,
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,-4,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Visible = false,
        				Parent = createdbutton
        			}
        		)
        		--
        		local createdtitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,	
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				Parent = createdbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = createdtitle
        		--
        		local createdb = {
        			["button"] = createdbutton,
        			["grey"] = grey,
        			["title"] = createdtitle,
        			["name"] = name
        		}
        		--
        		table.insert(createdbuttons,createdb)
        		--
        		if toggled then
        			createdb.grey.Visible = true
        			createdb.title.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],createdb.title)
        			selected = createdb
        		end
        		--
        		createdbutton.MouseButton1Down:Connect(function()
        			for i,v in pairs(createdbuttons) do
        				if v ~= createdb then
        					v.grey.Visible = false
        					v.title.TextColor3 = Color3.fromRGB(255,255,255)
        					local find = table.find(self.library.themeitems["accent"]["TextColor3"],v.title)
        					if find then
        						table.remove(self.library.themeitems["accent"]["TextColor3"],find)
        					end
        				end
        			end
        			--
        			createdb.grey.Visible = true
        			createdb.title.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],createdb.title)
        			selected = createdb
        		end)
        	end
        	--
        	local newbutton = function(parent,name)
        		local button_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local button_outline = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = button_holder
        			}
        		)
        		--
        		local button_outline2 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = button_outline
        			}
        		)
        		--
        		local button_color = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = button_outline2
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = button_color
        			}
        		)
        		--
        		local button_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = button_holder
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = button_button
        		--
        		return {button_holder,button_outline,button_button}
        	end
        	--
        	local function textbox(parent)
        		local textbox_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local outline5 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local outline6 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = outline5
        			}
        		)
        		--
        		local color2 = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = outline6
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = color2
        			}
        		)
        		--
        		local tbox = utility.new(
        			"TextBox",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				PlaceholderColor3 = Color3.fromRGB(178, 178, 178),
        				PlaceholderText = "",
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local tbox_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		tbox_button.MouseButton1Down:Connect(function()
        			tbox:CaptureFocus()
        		end)
        		--
        		return {textbox_holder,tbox,outline5}
        	end
        	--
        	local refresh = function()
        		for i,v in pairs(createdbuttons) do
        			v.button:Remove()
        			v.grey:Remove()
        			v.title:Remove()
        		end
        		createdbuttons = {}
        		for i,v in pairs(listfiles(folder)) do
        			if v:sub(-4) == ".cfg" then
        				if i == 1 then 
        					makebutton(v:sub(#tostring(folder)+2, -5),true)
        				else
        					makebutton(v:sub(#tostring(folder)+2, -5),false)
        				end
        			end
        		end
        	end
        	--
        	refresh()
        	--
        	local name = textbox(buttonsholder)
        	local load = newbutton(buttonsholder,"Load")
        	local delete = newbutton(buttonsholder,"Delete")
        	local save = newbutton(buttonsholder,"Save")
        	local create = newbutton(buttonsholder,"Create")
        	--
        	name[1].Size = UDim2.new(1,-10,0,20)
        	load[1].Size = UDim2.new(0.5,-6,0,20)
        	delete[1].Size = UDim2.new(0.5,-6,0,20)
        	save[1].Size = UDim2.new(0.5,-6,0,20)
        	create[1].Size = UDim2.new(0.5,-6,0,20)
        	--
        	name[1].Position = UDim2.new(0.5,0,0,0)
        	name[1].AnchorPoint = Vector2.new(0.5,0)
        	--
        	load[1].Position = UDim2.new(0,5,0,22)
        	load[1].AnchorPoint = Vector2.new(0,0)
        	--
        	delete[1].Position = UDim2.new(1,-5,0,22)
        	delete[1].AnchorPoint = Vector2.new(1,0)
        	--
        	save[1].Position = UDim2.new(0,5,0,44)
        	save[1].AnchorPoint = Vector2.new(0,0)
        	--
        	create[1].Position = UDim2.new(1,-5,0,44)
        	create[1].AnchorPoint = Vector2.new(1,0)
        	--
        	name[2].PlaceholderText = "Name"
        	--
        	local currentname = nil
        	--
        	name[2].Focused:Connect(function()
        		name[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	name[2].FocusLost:Connect(function()
        		local saved = name[2].Text
        		if #saved >= 3 and #saved <= 15 then
        			currentname = saved
        		else
        			name[2].Text = ""
        			currentname = nil
        		end
        		name[3].BorderColor3 = Color3.fromRGB(12,12,12)
        	end)
        	--
        	load[3].MouseButton1Down:Connect(function()
        		self.library:loadconfig(folder..selected.name..".cfg")
        		load[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		load[2].BorderColor3 = Color3.fromRGB(12,12,12)
        	end)
        	--
        	delete[3].MouseButton1Down:Connect(function()
        		delfile(folder..selected.name..".cfg")
        		delete[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		delete[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	--
        	save[3].MouseButton1Down:Connect(function()
        		writefile(folder..selected.name..".cfg", self.library:saveconfig())
        		save[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		save[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	--
        	create[3].MouseButton1Down:Connect(function()
        		writefile(folder..currentname..".cfg", self.library:saveconfig())
        		create[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		create[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	-- // button tbl
        	configloader = {
        		["library"] = self.library
        	}
        	-- // metatable indexing + return
        	setmetatable(configloader, configloaders)
        	return configloader 
        end
        
        
        local window = library:new({textsize = 13.5,font = Enum.Font.RobotoMono,name = "Winnable Hub / Fishing Simulator",color = Color3.fromRGB(255,135,0)})
        
        local Main_1_Page = window:page({name = "Main"})
        
        local farm = Main_1_Page:section({name = "Main",side = "left",size = 250})
        
        farm:toggle({name = "Auto Fish",def = false,callback = function(vu)
            _G.Auto_Fish = vu
        end})
        
        farm:toggle({name = "Auto Collect Chest",def = false,callback = function(vu)
            _G.Auto_Collect_Chest = vu
        end})
        
        farm:dropdown({name = "Spear Selected",def = "</>",max = 20,options = spear,callback = function(vu)
           _G.SpearSel = vu
        end})
        
        farm:toggle({name = "Auto Farm [OP]",def = false,callback = function(vu)
            _G.Auto_Farm = vu
        end})
        
        farm:toggle({name = "Auto Pick + Sell",def = false,callback = function(vu)
            _G.Auto_Pick = vu
        end})
        
        farm:toggle({name = "Auto Sell",def = false,callback = function(vu)
            _G.Auto_Sell = vu
        end})
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                if _G.Auto_Fish then
                    game:GetService("ReplicatedStorage").CloudFrameShared.DataStreams.FishCaught:FireServer()
                end
                end)
               end
            end)
        
            spawn(function()
               while wait(.2) do
                pcall(function()
                if _G.Auto_Fish then
                    game:GetService("ReplicatedStorage").CloudFrameShared.DataStreams.FishBiting:InvokeServer()
                end
                end)
               end
            end)
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                if _G.Auto_Collect_Chest then
                    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if string.find(v.Name, "Ship") then
            for i,v3 in pairs(v:GetChildren()) do
            if string.find(v3.Name, "Chest") then
        totargetv2(v3.HumanoidRootPart)
            wait(2)
            game:GetService("VirtualInputManager"):SendKeyEvent(true,"E",false,game)
        task.wait(.3)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"E",false,game)
            end
            end
            end
        end
                end
                end)
               end)
            end)
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                if _G.Auto_Farm then
                    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                if game.Players.LocalPlayer.Character.Humanoid.Health >= 1 then
                        if v.Name == "NeonGreatWhiteShark" or v.Name == "GreatWhiteShark" or v.Name == "KillerWhale" or v.Name == "BigGreatWhiteShark" then
                            totarget(v.HumanoidRootPart)
        local args = {
            [1] = v,
            [2] = _G.SpearSel,
            [3] = true
        }
        
        game:GetService("ReplicatedStorage").CloudFrameShared.DataStreams.MonsterHit:FireServer(unpack(args))
                    end
                    end
        end
                    end
                end)
               end)
            end)
        
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Farm or _G.Auto_Pick or _G.Auto_Collect_Chest then 
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                            local Noclip = Instance.new("BodyVelocity")
                            Noclip.Name = "BodyClip"
                            Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            Noclip.MaxForce = Vector3.new(100000,100000,100000)
                            Noclip.Velocity = Vector3.new(0,0,0)
                        end
                    else
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                    end
                end)
            end
        end)
        
        spawn(function()
            pcall(function()
                game:GetService("RunService").Stepped:Connect(function()
                    if _G.Auto_Farm or _G.Auto_Pick or _G.Auto_Collect_Chest then
                        for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                            if v:IsA("BasePart") then
                                v.CanCollide = false    
                            end
                        end
                    end
                end)
            end)
        end)
            
                spawn(function()
               while wait(.2) do
                pcall(function()
                if _G.Auto_Sell or _G.Auto_Pick then
            local args = {
            [1] = "SellEverything"
        }
        
        game:GetService("ReplicatedStorage").CloudFrameShared.DataStreams.processGameItemSold:InvokeServer(unpack(args))
        
                end
        end)
        end
        end)
            
                spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                if _G.Auto_Pick then
            for i,v2 in pairs(game:GetService("Workspace").DroppedItems:GetChildren()) do
                for i,v3 in pairs(v2:GetChildren()) do
                    if v3.Name == "Ring" then
        totargetv2(v2.Handle)
        end
                end
        end
                    end
                end)
               end)
                end)
        
                spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                if _G.Auto_Pick2 then
            for i,v2 in pairs(game:GetService("Workspace").DroppedItems:GetChildren()) do
                for i,v3 in pairs(v2:GetChildren()) do
                    if v3.Name == "Ring" then
        totargetv2(v2.Handle)
        
        end
                end
        end
                    end
                end)
               end)
                end)
        
            elseif placeId == 2753915549 or placeId == 4442272183 or placeId == 7449423635 then -- Aimbot
            if _G.Mode == "Aimbot" then
                    if not game:IsLoaded()then 
                local a=Instance.new("Message",workspace);
                a.Text='Waiting game to loaded before scripts is getting executed by Winnable Hub';
                game.Loaded:Wait();
                a:Destroy();
                wait(10);
            end;
            
                pcall(function()
            	repeat wait()
            		if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
            			if _G.Team == "Pirate" then
                            for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportQFrame.TextButton.Activated)) do                                                                                                
                                v.Function()
                            end
                        elseif _G.Team == "Marine" then
                            for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
                                v.Function()
                            end
                        else
                            for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do                                                                                                
                                v.Function()
                            end
                        end
            		end
            	until game.Players.LocalPlayer.Team ~= nil and game:IsLoaded()
            end)
        
        local DiscordLib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/discord%20lib.txt")()
        
        local win = DiscordLib:Window("Winnable Hub")
        
        local serv = win:Server("Main", "")
        
        local ca = serv:Channel("Auto Bounty")
        
        local tgls = serv:Channel("Aimbot Closet")
        
        local adsadsa = serv:Channel("Aimbot Select")
        
        function tween_cancel()
            local Distance2 = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                        local tween_s = game:service"TweenService"
                        local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
                        local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame})
                        tween:Play()
        end
        
        ca:Dropdown("Select Weapon", {"Melee","Sword","Gun","Blox Fruit","All"}, function(bool)
        _G.Weapon = bool
        end)
        
        ca:Toggle("Auto Bounty", _G.Auto_Bounty_A, function(bool)
        _G.Auto_Bounty = bool
        tween_cancel()
        end)
        
        ca:Toggle("Auto Bounty Hop", _G.Auto_Bounty_Hop_A, function(bool)
        _G.Auto_Bounty_Hop = bool
        end)
        
        tgls:Slider("Height", -20, 20, 0, function(tool)
        _G.higher2 = tool
        end)
        
        tgls:Toggle("Aimbot [Moblie]",false, function(bool)
        _G.Aimbot = bool
        end)
        
        tgls:Toggle("Aimbot [PC] Press G",false, function(bool)
        _G.Aimbot3 = bool
        end)
        
        local Playersss = {}
        
        for i,v in pairs(game.Players:GetChildren()) do
            table.insert(Playersss, v.Name)
        end
        
        local drop = adsadsa:Dropdown("Select Players", Playersss, function(bool)
        _G.SelPlayers = bool
        end)
        
        adsadsa:Button("Refresh Players", function(bool)
        drop:Clear(Playersss)
        for i,v in pairs(game.Players:GetChildren()) do
            table.insert(Playersss, v.Name)
        drop:Add(v.Name)
        end
        end)
        
        adsadsa:Slider("Height", -20, 20, 0, function(tool)
        _G.higher3 = tool
        end)
        
        adsadsa:Toggle("Aimbot [Moblie]",false, function(bool)
        _G.Aimbot7 = bool
        end)
        
        adsadsa:Toggle("Aimbot [PC] Press G",false, function(bool)
        _G.Aimbot4 = bool
        end)
        
        _G.Aimbot2 = false
        
        _G.Aimbot6 = false
        
        spawn(function()
            game:GetService("RunService").RenderStepped:Connect(function()
            pcall(function()
                if _G.Aimbot4 then
            local userInputService = game:GetService("UserInputService")
            userInputService.InputBegan:Connect(function(input, gameProcessedEvent)
                if input.UserInputType == Enum.UserInputType.Keyboard then
                    if _G.Aimbot6 == false and input.KeyCode == Enum.KeyCode.G then
        _G.Aimbot7 = true
        _G.Aimbot6 = true
        elseif _G.Aimbot6 == true and input.KeyCode == Enum.KeyCode.G then
            _G.Aimbot7 = false
            _G.Aimbot6 = false
                    end
                end
            end)  
                end
        end)
        end)
        end)
        
        spawn(function()
            while task.wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then 
        for i,v2 in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v2.ToolTip == _G.Weapon then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v2.Name))
            end
        end
        end
        end)
        end
        end)
        
        spawn(function()
            while task.wait(0.7) do
                pcall(function()
                    if _G.Auto_Bounty then 
        for i,v2 in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if _G.Weapon == "All" then
            if v2.ClassName == "Tool" then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v2.Name))
            end
        end
        end
        end
        end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "All" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "All" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"V",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"V",false,game)
                        end
                end
                end)
        end
        end)
        
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "All" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "All" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
                        end
                end
                end)
        end
        end)
        
        spawn(function()
            while task.wait(30) do
                pcall(function()
                    if _G.Auto_Bounty then 
        for i, v in pairs(game.Players:GetChildren()) do
                            if v.Name ~= game.Players.LocalPlayer.Name then
        if v.Character.Humanoid.Health >= 1 then
            local Distance2 = (v.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            if Distance2 <= 100 then
                wait(1)
        if v.Character.Humanoid.Health == v.Character.Humanoid.MaxHealth then
            v.Character.Humanoid.Health = 0
        end
        end
        end
        end
        end
        end
        end)
        end
        end)
        
                    spawn(function()
                       game:GetService("RunService").RenderStepped:Connect(function()
                        pcall(function()
                            if _G.Auto_Bounty then
                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                        local args = {
                    	[1] = "Buso"
                    	}
                    	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    end
                    end
                    end)
                    end)
                    end)
        
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Bounty or _G.Auto_Bounty_Hop then 
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                            local Noclip = Instance.new("BodyVelocity")
                            Noclip.Name = "BodyClip"
                            Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            Noclip.MaxForce = Vector3.new(100000,100000,100000)
                            Noclip.Velocity = Vector3.new(0,0,0)
                        end
                    else
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                    end
                end)
            end
        end)
        
        spawn(function()
            pcall(function()
                game:GetService("RunService").Stepped:Connect(function()
                    if _G.Auto_Bounty or _G.Auto_Bounty_Hop then
                        for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                            if v:IsA("BasePart") then
                                v.CanCollide = false    
                            end
                        end
                    end
                end)
            end)
        end)
        spawn(function()
            game:GetService("RunService").RenderStepped:Connect(function()
            pcall(function()
                if _G.Aimbot3 then
            local userInputService = game:GetService("UserInputService")
            userInputService.InputBegan:Connect(function(input, gameProcessedEvent)
                if input.UserInputType == Enum.UserInputType.Keyboard then
                    if _G.Aimbot2 == false and input.KeyCode == Enum.KeyCode.G then
        _G.Aimbot = true
        _G.Aimbot2 = true
        elseif _G.Aimbot2 == true and input.KeyCode == Enum.KeyCode.G then
            _G.Aimbot = false
            _G.Aimbot2 = false
                    end
                end
            end)  
                end
        end)
        end)
        end)
        
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Melee" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
                        end
                end
                end)
        end
        end)
        
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Melee" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Melee" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
        	
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Gun" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
                        end
                end
                end)
        end
        end)
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Gun" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
                        end
                end
                end)
        end
        end)
        
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Sword" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Sword" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Blox Fruit" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
        task.wait(2)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Blox Fruit" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
                        end
                end
                end)
        end
        end)
        
                    spawn(function()
                        game:GetService("RunService").Heartbeat:Connect(function()
                            if _G.Auto_Bounty_Hop then
                                if secondsea then
                                if not game:GetService("Workspace"):FindFirstChild("LOL") then
                                    local LOL = Instance.new("Part")
                                    LOL.Name = "LOL"
                                    LOL.Parent = game.Workspace
                                    LOL.Anchored = true
                                    LOL.Transparency = 1
                                    LOL.Size = Vector3.new(7,-0.2,7)
                                    LOL.Material = "Neon"
                                elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                                    game.Workspace["LOL"].CFrame = CFrame.new(-494.843536, 335.572388, 592.490784, -0.999687791, 6.43416058e-08, -0.0249856878, 6.51830092e-08, 1, -3.28611165e-08, 0.0249856878, -3.44794984e-08, -0.999687791)
                                end
                                end
                            end
                        end)
                    end)
        
                    spawn(function()
                        game:GetService("RunService").Heartbeat:Connect(function()
                            if _G.Auto_Bounty_Hop then
                                if thirdsea then
                                if not game:GetService("Workspace"):FindFirstChild("LOL") then
                                    local LOL = Instance.new("Part")
                                    LOL.Name = "LOL"
                                    LOL.Parent = game.Workspace
                                    LOL.Anchored = true
                                    LOL.Transparency = 1
                                    LOL.Size = Vector3.new(7,-0.2,7)
                                    LOL.Material = "Neon"
                                elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                                    game.Workspace["LOL"].CFrame = CFrame.new(-5017.65186, 314.843872, -2813.82446, -0.180542171, 4.55594957e-08, -0.983567238, 3.42272983e-08, 1, 4.00379569e-08, 0.983567238, -2.64363109e-08, -0.180542171)
                                end
                                end
                            end
                        end)
                    end)
                    
        spawn(function()
        	while wait(1) do
        			pcall(function()
        			    if _G.Auto_Bounty then
        			                for i,v2 in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v2.ToolTip == _G.Weapon then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v2.Name))
            end
        			                end
                    end
                end)
            end
        end)
        
        spawn(function()
        	while wait(1) do
        			pcall(function()
        			    if _G.UseGunKillPlayer then
        			 game:GetService'VirtualUser':CaptureController()
                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
        	     end
                end)
            end
        end)
        
        spawn(function()
        	game:GetService("RunService").RenderStepped:Connect(function()
                if _G.UseGunKillPlayer then
        			pcall(function()
        	 for i,v2 in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v2.ToolTip == _G.Weapon then
                        for i,v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
                            if v.Name ~= game.Players.LocalPlayer.Name then
               if v.Humanoid.Health >= 1 then
                                local args = {
                                    [1] = v.HumanoidRootPart.Position,
                                    [2] = v.HumanoidRootPart
                                }
                                game:GetService("Players").LocalPlayer.Character[v2.Name].RemoteFunctionShoot:InvokeServer(unpack(args))
               end
                            end
           end
                        end
                        end
                    end)
                end
            end)
        end)
        
                        local placeId = game.PlaceId
                    if placeId == 2753915549 then
                        firstsea = true
                    elseif placeId == 4442272183 then
                        secondsea = true
                    elseif placeId == 7449423635 then
                        thirdsea = true
                    end
        
        if thirdsea then
            spawn(function()
               while wait(90) do
                pcall(function()
                    if _G.Auto_Bounty_Hop then
                        _G.Auto_Bounty = false
                        wait(.5)
                        local Distance2 = (game:GetService("Workspace").LOL.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                        local tween_s = game:service"TweenService"
                        local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
                        local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game:GetService("Workspace").LOL.CFrame})
                        tween:Play()
                    wait(30)    
            local PlaceID = 7449423635
        local AllIDs = {}
        local foundAnything = ""
        local actualHour = os.date("!*t").hour
        local Deleted = false
        local File = pcall(function()
            AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
        end)
        if not File then
            table.insert(AllIDs, actualHour)
            writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
        end
        function TPReturner()
            local Site;
            if foundAnything == "" then
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
            else
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
            end
            local ID = ""
            if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                foundAnything = Site.nextPageCursor
            end
            local num = 0;
            for i,v in pairs(Site.data) do
                local Possible = true
                ID = tostring(v.id)
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    delfile("NotSameServers.json")
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        wait()
                        pcall(function()
                            writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                            wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
        
        function Teleport()
            while wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
        
        -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
        Teleport()
                    end
                end)
        end
        end)
        end
        
        if secondsea then
            spawn(function()
               while wait(90) do
                pcall(function()
                    if _G.Auto_Bounty_Hop then
                        _G.Auto_Bounty = false
                        wait(.5)
                        local Distance2 = (game:GetService("Workspace").LOL.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                        local tween_s = game:service"TweenService"
                        local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
                        local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game:GetService("Workspace").LOL.CFrame})
                        tween:Play()
                    wait(30)    
            local PlaceID = 4442272183
        local AllIDs = {}
        local foundAnything = ""
        local actualHour = os.date("!*t").hour
        local Deleted = false
        local File = pcall(function()
            AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
        end)
        if not File then
            table.insert(AllIDs, actualHour)
            writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
        end
        function TPReturner()
            local Site;
            if foundAnything == "" then
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
            else
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
            end
            local ID = ""
            if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                foundAnything = Site.nextPageCursor
            end
            local num = 0;
            for i,v in pairs(Site.data) do
                local Possible = true
                ID = tostring(v.id)
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    delfile("NotSameServers.json")
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        wait()
                        pcall(function()
                            writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                            wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
        
        function Teleport()
            while wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
        
        -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
        Teleport()
                    end
                end)
        end
        end)
        end
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Blox Fruit" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"V",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"V",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               while wait(.1) do
                pcall(function()
                    if _G.Auto_Bounty then
                        if _G.Weapon == "Blox Fruit" then
        game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
        task.wait(.1)
        game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
                        end
                end
                end)
        end
        end)
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.Auto_Bounty then
                        for i, v in pairs(game.Players:GetChildren()) do
                            if v.Name ~= game.Players.LocalPlayer.Name then
               if v.Character.Humanoid.Health >= 1 then
            local Distance2 = (v.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            if Distance2 <= 50000 then
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = v.Character.HumanoidRootPart.CFrame * CFrame.new(0,45,25)})
            tween:Play()
        local camera = game.Workspace.CurrentCamera
        camera.CFrame = CFrame.new(camera.CFrame.Position,v.Character.HumanoidRootPart.Position)
            end
            end
                            end
                        end
                    end
                end)
        end)
        end)
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.Aimbot7 then
                        local camera = game.Workspace.CurrentCamera
        camera.CFrame = CFrame.new(camera.CFrame.Position,game.Players[_G.SelPlayers].Character.HumanoidRootPart.Position) * CFrame.new(0,_G.higher3,0)
                end
                end)
        end)
        end)
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.Aimbot then
                        local camera = game.Workspace.CurrentCamera
        local localplayer = game:GetService("Players").LocalPlayer
        function closestplayer()
                        local dist = math.huge -- math.huge means a really large number, 1M+.
                        local target = nil --- nil means no value
                        for i,v in pairs (game:GetService("Players"):GetPlayers()) do
                            if v ~= localplayer then
                                if v.Character and v.Character:FindFirstChild("Head") and v.Character.Humanoid.Health > 0 then --- creating the checks
                                    local magnitude = (v.Character.HumanoidRootPart.Position - localplayer.Character.HumanoidRootPart.Position).magnitude
                                    if magnitude < dist then
                                        dist = magnitude
                                        target = v
                                    end
         
                                end
                            end
                        end
                        return target
                    end
        camera.CFrame = CFrame.new(camera.CFrame.Position,closestplayer().Character.HumanoidRootPart.Position) * CFrame.new(0,_G.higher2,0)
                    end
                end)
        end)
        end)
            end)
            end
    if _G.Mode == "NextWorld" then -- next world
        loadstring(game:HttpGet("https://raw.githubusercontent.com/xlostpexz/nextworldbf/Fps/Love.lua"))()
        end
                if _G.Mode == nil or _G.Mode == "" or _G.Mode == "Normal" then -- blox fruits  
    		loadstring(game:HttpGet("https://raw.githubusercontent.com/xlostpexz/bfawww/Fps/heart.lua"))()
    
    end
            elseif placeId == 5931540094 or placeId == 6381829480 or placeId == 4520749081  or placeId == 6596144663 then -- King Legacy
                if not game:IsLoaded()then 
                    local a=Instance.new("Message",workspace);
                    a.Text='Waiting game to loaded before scripts is getting executed by Winnable Hub';
                    game.Loaded:Wait();
                    a:Destroy();
                    wait(10);
                end;
            
            if Mode_Value == nil then Mode_Value = "Above" end
            if Distance_Value == nil then Distance_Value = 9 end
            
                local placeId = game.PlaceId
            	if placeId == 4520749081 then
            		First = true
                elseif placeId == 6381829480 then
            		Second = true
            	elseif placeId == 5931540094 then
            		Raid = true
            	elseif placeId == 6596144663 then
                    Awakeworld = true
            	end
            	
            	    function CheckLevel()
                	local MyLevel = game.Players.LocalPlayer.PlayerStats.lvl.Value
                	if First then
                    	   if MyLevel == 1 or MyLevel <= 9 then
                		  CFrameQuest = CFrame.new(-1962.25513, 48.167244, -4498.12402, 0.681326449, 3.14344142e-08, -0.731979728, 2.6569742e-08, 1, 6.76754865e-08, 0.731979728, -6.55576073e-08, 0.681326449)
                		  CFrameMon = CFrame.new(-1878.2135, 48.2099533, -4395.56689, 0.737461627, 6.4809953e-08, 0.675389051, -7.38304351e-08, 1, -1.53435078e-08, -0.675389051, -3.85490182e-08, 0.737461627)
                		  NameMon = "Soldier"
                		  Ms = "Soldier [Lv. 1]"
                		  levelquest = 1
                	   elseif MyLevel == 10 or MyLevel <= 19 then
                		  CFrameQuest = CFrame.new(-1892.62646, 48.3253822, -4522.58789, -0.631278634, -7.78868525e-08, 0.775556087, -1.31972451e-08, 1, 8.96849528e-08, -0.775556087, 4.63809897e-08, -0.631278634)
                		  CFrameMon = CFrame.new(-1710.06152, 60.6180878, -4415.66113, 0.831968367, 7.46319131e-08, -0.554823101, -8.58878551e-08, 1, 5.72423087e-09, 0.554823101, 4.28901856e-08, 0.831968367)
                		  NameMon = "Clown Pirate"
                		  Ms = "Clown Pirate [Lv. 10]"
                		  levelquest = 10
                	   elseif MyLevel == 20 or MyLevel <= 29 then
                		  CFrameQuest = CFrame.new(-1964.54871, 48.3253822, -4616.43359, 0.732624233, -5.67917368e-07, 0.680633366, 2.03967417e-07, 1, 6.1484775e-07, -0.680633366, -3.11625314e-07, 0.732624233)
                		  CFrameMon = CFrame.new(-1886.16638, 57.5959396, -4651.24072, 0.976776063, 1.03591475e-07, -0.214262754, -1.00981012e-07, 1, 2.31288109e-08, 0.214262754, -9.55199808e-10, 0.976776063)
                		  NameMon = "Smoky"
                		  Ms = "Smoky [Lv. 20]"
                		  levelquest = 20
                	   elseif MyLevel == 30 or MyLevel <= 49 then
                		  CFrameQuest = CFrame.new(-2272.65137, 48.3253746, -4680.40283, 0.728982508, -4.22769464e-09, -0.684532285, -4.38285741e-10, 1, -6.64277966e-09, 0.684532285, 5.14249088e-09, 0.728982508)
                		  CFrameMon = CFrame.new(-2143.95874, 48.3253822, -4807.61865, 0.726590991, -1.90278122e-08, -0.687070251, -3.58665986e-08, 1, -6.56238015e-08, 0.687070251, 7.23245321e-08, 0.726590991)
                		  NameMon = "Tashi"
                		  Ms = "Tashi [Lv. 30]"
                		  levelquest = 30
                	   elseif MyLevel == 50 or MyLevel <= 74 then
                		  CFrameQuest = CFrame.new(-681.385864, 37.8180923, -3463.90674, -0.163140774, -4.4636522e-08, 0.986602783, 4.4160462e-09, 1, 4.59728646e-08, -0.986602783, 1.18569323e-08, -0.163140774)
                		  CFrameMon = CFrame.new(-532.341736, 78.0751953, -3368.21191, -0.622933567, 5.67032785e-08, -0.782274723, 1.07946443e-08, 1, 6.38892317e-08, 0.782274723, 3.1354368e-08, -0.622933567)
                		  NameMon = "Clown Swordman"
                		  Ms = "Clown Swordman [Lv. 50]"
                		  levelquest = 50
                	   elseif MyLevel == 75 or MyLevel <= 144 then
                		  CFrameQuest = CFrame.new(-390.785431, 68.7723846, -3491.50415, 0.900946379, 4.73066031e-08, 0.433930397, -1.56576228e-08, 1, -7.65097923e-08, -0.433930397, 6.21369054e-08, 0.900946379)
                		  CFrameMon = CFrame.new(-394.170593, 68.7723846, -3531.94995, 0.998563409, -1.93020711e-08, 0.0535827242, 1.44820369e-08, 1, 9.03432849e-08, -0.0535827242, -8.94375134e-08, 0.998563409)
                		  NameMon = "The Clown"
                		  Ms = "The Clown [Lv. 75]"
                		  levelquest = 75
                	   elseif MyLevel == 145 or MyLevel <= 179 then
                		  CFrameQuest = CFrame.new(-2462.37036, 68.6313477, -2541.44678, 0.990872145, -1.97332888e-08, -0.134805188, 7.12626003e-09, 1, -9.40028784e-08, 0.134805188, 9.21841732e-08, 0.990872145)
                		  CFrameMon = CFrame.new(-2354.74023, 68.6122513, -2384.00342, 0.998905063, -9.32452893e-10, 0.0467835106, 2.67321654e-09, 1, -3.714635e-08, -0.0467835106, 3.72307412e-08, 0.998905063)
                		  NameMon = "The Barbaric"
                		  Ms = "The Barbaric [Lv. 145]"
                		  levelquest = 145
                	   elseif MyLevel == 180 or MyLevel <= 229 then
                		  CFrameQuest = CFrame.new(-960.657349, 10.5658875, -1367.1908, 0.733786941, 2.2709461e-09, -0.679379702, -1.448623e-08, 1, -1.23036656e-08, 0.679379702, 1.8869919e-08, 0.733786941)
                		  CFrameMon = CFrame.new(-919.743713, 10.5658884, -1372.67236, -0.330581278, 5.96692686e-08, -0.943777502, -2.61544368e-08, 1, 7.23851059e-08, 0.943777502, 4.86131313e-08, -0.330581278)
                		  NameMon = "Fighter Fishman"
                		  Ms = "Fighter Fishman [Lv. 180]"
                		  levelquest = 180
                	   elseif MyLevel == 230 or MyLevel <= 249 then
                		  CFrameQuest = CFrame.new(-552.46106, 10.5159292, -1373.34521, -0.775945306, 3.82098158e-08, 0.630800188, 6.04673787e-08, 1, 1.38071696e-08, -0.630800188, 4.88564424e-08, -0.775945306)
                		  CFrameMon = CFrame.new(-454.314117, 10.4897604, -1392.70435, 0.600633144, -4.74826711e-09, -0.799524724, -6.68660789e-08, 1, -5.61711815e-08, 0.799524724, 8.71993606e-08, 0.600633144)
                		  NameMon = "Shark Man"
                		  Ms = "Shark Man [Lv. 230]"
                		  levelquest = 230
                	   elseif MyLevel == 250 or MyLevel <= 299 then
                		  CFrameQuest = CFrame.new(-4095.40186, 64.0833893, -3017.72388, -0.673433542, -3.49600532e-06, 0.739247739, -8.8055242e-07, 1, 3.92698075e-06, -0.739247739, 1.99361421e-06, -0.673433542)
                		  CFrameMon = CFrame.new(-4113.0415, 15.5986032, -3081.23657, 0.846352518, -7.12484294e-08, -0.532623112, 5.02949469e-08, 1, -5.38489147e-08, 0.532623112, 1.87869134e-08, 0.846352518)
                		  NameMon = "Trainer Chef"
                		  Ms = "Trainer Chef [Lv. 250]"
                		  levelquest = 250
                	   elseif MyLevel == 300 or MyLevel <= 349 then
                		  CFrameQuest = CFrame.new(-4196.39893, 64.0833817, -3026.42896, 0.876318574, 1.64075189e-08, -0.481732011, 1.06010656e-09, 1, 3.59878705e-08, 0.481732011, -3.20475273e-08, 0.876318574)
                		  CFrameMon = CFrame.new(-4270.94775, 64.5096741, -3069.67969, 0.998697221, 4.77111257e-08, 0.0510283262, -4.6003187e-08, 1, -3.4644895e-08, -0.0510283262, 3.22522951e-08, 0.998697221)
                		  NameMon = "Dark Leg"
                		  Ms = "Dark Leg [Lv. 300]"
                		  levelquest = 300
                	   elseif MyLevel == 350 or MyLevel <= 399 then
                		  CFrameQuest = CFrame.new(-4403.09912, 64.9662781, -2942.81079, 0.834608436, 0.000712737092, -0.550843239, 0.000422198646, 0.999998033, 0.00193359237, 0.550843537, -0.00184635771, 0.834606469)
                		  CFrameMon = CFrame.new(-4309.7207, 70.4149017, -2734.12036, -0.894527912, -6.34367936e-08, 0.447012067, -4.57524578e-08, 1, 5.03564515e-08, -0.447012067, 2.45933496e-08, -0.894527912)
                		  NameMon = "Dory"
                		  Ms = "Dory [Lv. 350]"
                		  levelquest = 350
                	   elseif MyLevel == 400 or MyLevel <= 449 then
                		  CFrameQuest = CFrame.new(-5461.64258, 18.3136292, -1345.08533, -0.0806987882, -1.82112303e-09, 0.996738553, -4.43264803e-08, 1, -1.76171588e-09, -0.996738553, -4.43240786e-08, -0.0806987882)
                		  CFrameMon = CFrame.new(-5431.19873, 18.6365395, -1264.57922, -0.816107988, 5.74519943e-09, -0.577899456, 6.43413074e-08, 1, -8.09210974e-08, 0.577899456, -1.03223158e-07, -0.816107988   )
                		  NameMon = "Snow Soldier"
                		  Ms = "Snow Soldier [Lv. 400]"
                		  levelquest = 400
                	   elseif MyLevel == 450 or MyLevel <= 524 then
                		  CFrameQuest = CFrame.new(-5538.59033, 18.3135986, -1479.54114, 0.0500373207, 1.28449665e-05, -0.998747349, -1.12371015e-06, 1, 1.28047786e-05, 0.998747349, 4.81585687e-07, 0.0500373207)
                		  CFrameMon = CFrame.new(-5531.04541, 18.3136292, -1559.91504, 0.99390012, 5.55644739e-08, 0.110284157, -6.56912178e-08, 1, 8.8190653e-08, -0.110284157, -9.48974019e-08, 0.99390012)
                		  NameMon = "King Snow"
                		  Ms = "King Snow [Lv. 450]"
                		  levelquest = 450
                	   elseif MyLevel == 525 or MyLevel <= 624 then
                		  CFrameQuest = CFrame.new(-2731.64697, 12.8652372, -597.278259, 0.764146745, -8.27880342e-09, -0.645042419, -3.93044104e-08, 1, -5.93963101e-08, 0.645042419, 7.07405121e-08, 0.764146745)
                		  CFrameMon = CFrame.new(-2711.70215, 12.8652411, -611.894958, 0.590994716, 1.65899845e-08, -0.806675434, -1.07753566e-08, 1, 1.26715216e-08, 0.806675434, 1.20341326e-09, 0.590994716)
                		  NameMon = "Candle Man"
                		  Ms = "Candle Man [Lv. 525]"
                		  levelquest = 525
                	   elseif MyLevel == 625 or MyLevel <= 724 then
                		  CFrameQuest = CFrame.new(-2944.26025, 12.9749279, -806.078308, 0.846702397, -5.65881741e-08, -0.532066822, 6.845152e-08, 1, 2.57466426e-09, 0.532066822, -3.86007564e-08, 0.846702397)
                		  CFrameMon = CFrame.new(-2940.72534, 12.8652372, -815.800659, 0.934226215, 6.06554522e-08, -0.356681108, -4.64675622e-08, 1, 4.83463829e-08, 0.356681108, -2.85923552e-08, 0.934226215)
                		  NameMon = "Bomb Man"
                		  Ms = "Bomb Man [Lv. 625]"
                		  levelquest = 625
                	   elseif MyLevel == 725 or MyLevel <= 799 then
                		  CFrameQuest = CFrame.new(-2952.05322, 43.0035782, -700.910095, -0.859289944, -1.56604187e-08, -0.511488795, -4.37448033e-09, 1, -2.3268294e-08, 0.511488795, -1.77567134e-08, -0.859289944)
                		  CFrameMon = CFrame.new(-3028.81787, 92.3630295, -564.624207, -0.704288006, -4.78162541e-08, 0.709914386, -2.48226009e-08, 1, 4.27290914e-08, -0.709914386, 1.24716646e-08, -0.704288006)
                		  NameMon = "King of Sand"
                		  Ms = "King of Sand [Lv. 725]"
                		  levelquest = 725
                	   elseif MyLevel == 800 or MyLevel <= 849 then
                		  CFrameQuest = CFrame.new(-4483.23682, 200.713303, 1038.57812, -0.829204917, 9.2099639e-05, -0.558944702, -3.16375736e-05, 1, 0.000211709063, 0.558944702, 0.000193233849, -0.829204917)
                		  CFrameMon = CFrame.new(-4665.99365, 250.107971, 1157.57776, -0.178683862, 6.96002331e-08, -0.983906567, -6.19530738e-08, 1, 8.19897465e-08, 0.983906567, 7.56062803e-08, -0.178683862)
                		  NameMon = "Sky Soldier"
                		  Ms = "Sky Soldier [Lv. 800]"
                		  levelquest = 800
                	   elseif MyLevel == 850 or MyLevel <= 899 then
                		  CFrameQuest = CFrame.new(-4046.40869, 386.567383, 1207.90979, -0.723364234, 1.0201834e-07, 0.690466642, 3.51497569e-08, 1, -1.10928262e-07, -0.690466642, -5.59718032e-08, -0.723364234)
                		  CFrameMon = CFrame.new(-4030.83105, 386.497009, 1239.88538, -0.629865825, 1.59832183e-08, -0.776703954, -2.91498488e-08, 1, 4.42172485e-08, 0.776703954, 5.04917388e-08, -0.629865825)
                		  NameMon = "Ball Man"
                		  Ms = "Ball Man [Lv. 850]"
                		  levelquest = 850
                	   elseif MyLevel == 900 or MyLevel <= 999 then
                		  CFrameQuest = CFrame.new(-4093.05322, 386.444641, 1339.92334, 0.512696981, 7.65733432e-09, 0.858569622, 1.60188196e-09, 1, -9.87527926e-09, -0.858569622, 6.43835296e-09, 0.512696981)
                		  CFrameMon = CFrame.new(-4123.6626, 386.444611, 1411.17566, -0.92930603, -7.19894366e-09, 0.369310558, -5.2059077e-09, 1, 6.39316244e-09, -0.369310558, 4.01860767e-09, -0.92930603)
                		  NameMon = "Rumble Man"
                		  Ms = "Rumble Man [Lv. 900]"
                		  levelquest = 900
                	   elseif MyLevel == 1000 or MyLevel <= 1099 then
                		  CFrameQuest = CFrame.new(1738.04211, 11.8708391, 713.633423, 0.922079504, -2.6277279e-08, -0.387000501, -8.0878042e-09, 1, -8.71701147e-08, 0.387000501, 8.35077572e-08, 0.922079504)
                		  CFrameMon = CFrame.new(1832.69104, 18.5599995, 934.964539, 0.854102731, -8.39842897e-08, -0.520104349, 5.99362053e-08, 1, -6.30500665e-08, 0.520104349, 2.26781545e-08, 0.854102731)
                		  NameMon = "Elite Soldier"
                		  Ms = "Elite Soldier [Lv. 1000]"
                		  levelquest = 1000
                	   elseif MyLevel == 1100 or MyLevel <= 1149 then
                		  CFrameQuest = CFrame.new(1726.5697, 17.418705, 655.899841, -0.998600543, 4.69847627e-08, 0.052886311, 4.43294184e-08, 1, -5.13815479e-08, -0.052886311, -4.89652194e-08, -0.998600543)
                		  CFrameMon = CFrame.new(1931.4823, 54.662529, 645.181824, 0.350004643, -3.3933063e-09, 0.936747968, 2.57171333e-08, 1, -5.98646643e-09, -0.936747968, 2.61857647e-08, 0.350004643)
                		  NameMon = "Leader"
                		  Ms = "Leader [Lv. 1100]"
                		  levelquest = 1100
                	   elseif MyLevel == 1150 or MyLevel <= 1249 then
                		  CFrameQuest = CFrame.new(1539.41357, 11.8708391, 981.810059, 0.437861592, 6.37178061e-08, 0.899042368, 3.31661418e-08, 1, -8.70259171e-08, -0.899042368, 6.79230752e-08, 0.437861592)
                		  CFrameMon = CFrame.new(1496.15344, 12.2744045, 1045.21997, -0.87622267, 4.6983434e-08, 0.481906474, 2.31220536e-08, 1, -5.54534338e-08, -0.481906474, -3.74468883e-08, -0.87622267)
                		  NameMon = "Pasta"
                		  Ms = "Pasta [Lv. 1150]"
                		  levelquest = 1150
                	   elseif MyLevel == 1250 or MyLevel <= 1324 then
                		  CFrameQuest = CFrame.new(-1247.32385, 13.0547819, 2180.64941, 0.0845803842, -9.24201089e-08, -0.996416688, 5.04045623e-08, 1, -8.84739038e-08, 0.996416688, -4.27407905e-08, 0.0845803842)
                		  CFrameMon = CFrame.new(-1310.047, 13.1146116, 2236.08496, -0.200146377, -8.81010322e-08, 0.979766011, -7.57137553e-09, 1, 8.83738096e-08, -0.979766011, 1.02695203e-08, -0.200146377)
                		  NameMon = "Wolf"
                		  Ms = "Wolf [Lv. 1250]"
                		  levelquest = 1250
                	   elseif MyLevel == 1325 or MyLevel <= 1399 then
                		  CFrameQuest = CFrame.new(-1188.72314, 13.3749895, 2215.34985, -0.0538746268, 3.80817511e-08, 0.998547733, 1.80948554e-08, 1, -3.71608664e-08, -0.998547733, 1.6066549e-08, -0.0538746268)
                		  CFrameMon = CFrame.new(-1094.78442, 13.1146116, 2233.44434, -0.0413781144, -2.98871008e-08, -0.999143541, 2.70651745e-09, 1, -3.00248075e-08, 0.999143541, -3.94656929e-09, -0.0413781144)
                		  NameMon = "Giraffe"
                		  Ms = "Giraffe [Lv. 1325]"
                		  levelquest = 1325
                	   elseif MyLevel == 1400 or MyLevel <= 1499 then
                		  CFrameQuest = CFrame.new(-1116.98035, 14.4115582, 2845.29248, -0.842971325, 1.64206195e-08, -0.537958503, 5.08918863e-09, 1, 2.25492833e-08, 0.537958503, 1.62706275e-08, -0.842971325)
                		  CFrameMon = CFrame.new(-1151.94812, 13.0450315, 2889.77661, -0.995078206, 1.02150338e-07, 0.0990927666, 9.82406618e-08, 1, -4.43341541e-08, -0.0990927666, -3.438101e-08, -0.995078206)
                		  NameMon = "Leo"
                		  Ms = "Leo [Lv. 1400]"
                		  levelquest = 1400
                	   elseif MyLevel == 1500 or MyLevel <= 1599 then
                		  CFrameQuest = CFrame.new(-2733.54761, 15.775178, 4085.68604, 0.942427754, 2.77530781e-08, -0.334409833, -3.50647333e-08, 1, -1.58275864e-08, 0.334409833, 2.66423488e-08, 0.942427754)
                		  CFrameMon = CFrame.new(-2684.49048, 15.7611723, 3998.31616, -0.912651837, 5.75279664e-08, 0.408737808, 2.37540991e-08, 1, -8.77059705e-08, -0.408737808, -7.03358154e-08, -0.912651837)
                		  NameMon = "Zombie"
                		  Ms = "Zombie [Lv. 1500]"
                		  levelquest = 1500
                	   elseif MyLevel == 1600 or MyLevel <= 1699 then
                		  CFrameQuest = CFrame.new(-2795.48169, 19.6245041, 4230.78613, -0.991855383, 2.44628904e-08, 0.127368927, 1.89357454e-08, 1, -4.46056099e-08, -0.127368927, -4.18304893e-08, -0.991855383)
                		  CFrameMon = CFrame.new(-2826.11743, 20.0110397, 4251.40967, -0.858602881, 8.08960152e-08, 0.512641251, 1.71525638e-08, 1, -1.29074238e-07, -0.512641251, -1.02030398e-07, -0.858602881)
                		  NameMon = "Shadow Master"
                		  Ms = "Shadow Master [Lv. 1600]"
                		  levelquest = 1600
                	   elseif MyLevel == 1700 or MyLevel <= 1799 then
                		  CFrameQuest = CFrame.new(2391.32837, 49.60606, -1781.85205, 0.531621397, -9.81316806e-09, -0.846982121, -3.80857408e-08, 1, -3.54911407e-08, 0.846982121, 5.1125788e-08, 0.531621397)
                		  CFrameMon = CFrame.new(2368.45532, 49.60606, -1756.1532, -0.931334078, 8.21754256e-08, 0.364165902, 7.65207844e-08, 1, -2.9956162e-08, -0.364165902, -3.29330903e-11, -0.931334078)
                		  NameMon = "New World Pirate"
                		  Ms = "New World Pirate [Lv. 1700]"
                		  levelquest = 1750
                	   elseif MyLevel == 1800 or MyLevel <= 1924 then
                		  CFrameQuest = CFrame.new(2398.89941, 49.5735512, -2238.47705, 0.329593182, -0.207405761, 0.921059787, 0.0420333594, 0.977828026, 0.205147654, -0.943186879, -0.0289000347, 0.331003428)
                		  CFrameMon = CFrame.new(2337.87915, 49.6260185, -2059.31665, 0.999965727, -3.7506851e-08, 0.00827745907, 3.72158979e-08, 1, 3.5304474e-08, -0.00827745907, -3.49952103e-08, 0.999965727)
                		  NameMon = "Rear Admiral"
                		  Ms = "Rear Admiral [Lv. 1800]"
                		  levelquest = 1800
                	   elseif MyLevel == 1925 or MyLevel <= 1999 then
                		  CFrameQuest = CFrame.new(2115.89575, 49.9948997, -2117.60303, -0.99753505, 9.8106645e-10, 0.0701696351, 8.24894553e-09, 1, 1.03286077e-07, -0.0701696351, 1.03610311e-07, -0.99753505)
                		  CFrameMon = CFrame.new(2121.01855, 51.4794235, -2088.82935, -0.875889122, -2.25446417e-08, -0.482512414, -2.37332463e-11, 1, -4.66803627e-08, 0.482512414, -4.08753706e-08, -0.875889122)
                		  NameMon = "Quake Woman"
                		  Ms = "Quake Woman [Lv. 1925]"
                		  levelquest = 1925
                	   elseif MyLevel == 2000 or MyLevel <= 2049 then
                		  CFrameQuest = CFrame.new(-1467.802, 41.8205376, 6223.92578, -0.885435164, 9.11779008e-09, -0.464762866, -2.25316317e-08, 1, 6.25439114e-08, 0.464762866, 6.58504504e-08, -0.885435164)
                		  CFrameMon = CFrame.new(-1477.32434, 40.2694321, 6211.20996, 0.811786592, 1.85708182e-09, 0.583954215, -2.38483033e-09, 1, 1.35098738e-10, -0.583954215, -1.50230306e-09, 0.811786592)
                		  NameMon = "Fishman"
                		  Ms = "Fishman [Lv. 2000]"
                		  levelquest = 2000
                	   elseif MyLevel == 2050 or MyLevel <= 2099 then
                		  CFrameQuest = CFrame.new(-1927.26917, 40.2722054, 6264.8667, 0.186216667, 1.78145072e-08, 0.982508719, 2.17757563e-08, 1, -2.22588525e-08, -0.982508719, 2.55398405e-08, 0.186216667)
                		  CFrameMon = CFrame.new(-1950.00586, 53.8602066, 6234.3208, 0.945748627, -1.44060852e-08, 0.324899316, -1.70462329e-08, 1, 9.395999e-08, -0.324899316, -9.44008391e-08, 0.945748627)
                		  NameMon = "Combat Fishman"
                		  Ms = "Combat Fishman [Lv. 2050]"
                		  levelquest = 2050
                	   elseif MyLevel == 2100 or MyLevel <= 2149 then
                		  CFrameQuest = CFrame.new(-1414.35876, 40.3944893, 6436.60156, -0.754716575, 3.19714708e-08, -0.65605098, 8.44040997e-08, 1, -4.83646936e-08, 0.65605098, -9.18750303e-08, -0.754716575)
                		  CFrameMon = CFrame.new(-1469.90649, 40.2663803, 6550.47754, -0.942791998, -4.23316919e-08, 0.333381534, -1.23792283e-08, 1, 9.19686656e-08, -0.333381534, 8.25803141e-08, -0.942791998)
                		  NameMon = "Sword Fishman"
                		  Ms = "Sword Fishman [Lv. 2100]"
                		  levelquest = 2100
                	   elseif MyLevel == 2150 or MyLevel <= 2199 then
                		  CFrameQuest = CFrame.new(-1774.896, 40.2981453, 6490.1499, -0.996065557, 4.52866438e-08, 0.0886197463, 4.38683578e-08, 1, -1.79517787e-08, -0.0886197463, -1.39935459e-08, -0.996065557)
                		  CFrameMon = CFrame.new(-1811.5874, 45.1747131, 6507.38135, -0.963738322, -3.03469179e-08, 0.266849101, -7.12806925e-09, 1, 8.79797781e-08, -0.266849101, 8.28873681e-08, -0.963738322)
                		  NameMon = "Soldier Fishman"
                		  Ms = "Soldier Fishman [Lv. 2150]"
                		  levelquest = 2150
                	   elseif MyLevel >= 2200 then
                		  CFrameQuest = CFrame.new(-1921.29211, 40.2950401, 6474.16064, -0.469070762, -2.70893619e-08, 0.883160591, 1.86789091e-08, 1, 4.0594081e-08, -0.883160591, 3.55379726e-08, -0.469070762)
                		  CFrameMon = CFrame.new(-1835.35229, 45.1747131, 6602.80518, -0.974699438, 7.14299508e-09, 0.223519564, 2.01830597e-09, 1, -2.31557067e-08, -0.223519564, -2.21187229e-08, -0.974699438)
                		  NameMon = "Seasoned Fishman"
                		  Ms = "Seasoned Fishman [Lv. 2200]"
                		  levelquest = 2200
                		  end
                		  end
                		  if Second then
                	   if MyLevel >= 2250 and MyLevel <= 2299 then
                		  Ms = "Beast Pirate [Lv. 2250]"
                		  CFrameQuest = CFrame.new(-3848.85205, 57.2931862, 133.001282, -0.931727767, 0.003111572, 0.363144189, 0.00222482509, 0.999993443, -0.00286007696, -0.363150716, -0.00185688084, -0.931728542)
                		  NameMon = "Beast Pirate"
                		  CFrameMon = CFrame.new(-3853.22144, 85.8306274, 109.570305, 0.465366155, 2.54748356e-09, 0.885118246, 9.62900444e-08, 1, -5.35042766e-08, -0.885118246, 1.10127154e-07, 0.465366155)
                		  levelquest = 2250
                	   elseif MyLevel >= 2300 and MyLevel <= 2349 then
                		  Ms = "Beast Swordman [Lv. 2300]"
                		  CFrameQuest = CFrame.new(-4223.98535, 98.3996277, -299.376312, -0.198194712, -4.79691842e-08, 0.98016268, -1.23131926e-07, 1, 2.40420164e-08, -0.98016268, -1.15924315e-07, -0.198194712)
                		  NameMon = "Beast Swordman"
                		  CFrameMon = CFrame.new(-4204.20703, 123.384987, -293.970581, 0.328679204, -4.21236379e-08, -0.944441617, 5.70756775e-10, 1, -4.44030022e-08, 0.944441617, 1.40552965e-08, 0.328679204)
                		  levelquest = 2300
                	   elseif MyLevel >= 2350 and MyLevel <= 2399 then
                		  Ms = "Gazelle Man [Lv. 2350]"
                		  CFrameQuest = CFrame.new(-4460.98145, 57.9729996, 141.293106, 0.994238675, -7.26222936e-07, -0.107188955, 7.82422944e-07, 1, 4.82253199e-07, 0.107188955, -5.63341871e-07, 0.994238675)
                		  NameMon = "Gazelle Man"
                		  CFrameMon = CFrame.new(-4404.16699, 78.7712021, 154.715683, -0.824920774, -2.58292996e-08, -0.565248311, -7.09305183e-08, 1, 5.78201842e-08, 0.565248311, 8.77904327e-08, -0.824920774)
                		  levelquest = 2350
                	   elseif MyLevel >= 2400 and MyLevel <= 2449 then
                		  Ms = "Bandit Beast Pirate [Lv. 2400]"
                		  CFrameQuest = CFrame.new(-4542.80811, 135.854019, -919.252075, -0.997260153, 0.000201361312, -0.0739743263, 0.000195363449, 1, 8.83161774e-05, 0.0739743486, 7.36223228e-05, -0.997260153)
                		  NameMon = "Bandit Beast Pirate"
                		  CFrameMon = CFrame.new(-4526.9917, 164.039322, -937.318909, 0.999999344, 1.07452198e-08, 0.00112135592, -1.06861568e-08, 1, -5.26766293e-08, -0.00112135592, 5.2664614e-08, 0.999999344)
                		  levelquest = 2400
                	   elseif MyLevel >= 2450 and MyLevel <= 2499 then
                		  Ms = "Powerful Beast Pirate [Lv. 2450]"
                		  CFrameQuest = CFrame.new(-4565.77832, 135.883545, -858.554565, 0.997523487, 9.21371281e-08, 0.0703338608, -8.86712783e-08, 1, -5.23993506e-08, -0.0703338608, 4.60329908e-08, 0.997523487)
                		  NameMon = "Powerful Beast Pirate"
                		  CFrameMon = CFrame.new(-4581.7207, 166.189194, -834.960083, -0.847955644, 3.46563098e-08, 0.530067205, 9.33227629e-09, 1, -5.04520017e-08, -0.530067205, -3.78343259e-08, -0.847955644)
                		  levelquest = 2450
                	   elseif MyLevel >= 2500 and MyLevel <= 2549 then
                		  Ms = "Violet Samurai [Lv. 2500]"
                		  CFrameQuest = CFrame.new(-5188.1875, 85.3521881, -882.862793, -0.997630298, -1.30848994e-08, -0.0688023344, -1.29800162e-08, 1, -1.9714701e-09, 0.0688023344, -1.07374298e-09, -0.997630298)
                		  NameMon = "Violet Samurai"
                		  CFrameMon = CFrame.new(-5155.43115, 101.109268, -913.710693, 0.945549548, 5.16686463e-08, -0.325478137, -4.38803553e-08, 1, 3.12696748e-08, 0.325478137, -1.52849324e-08, 0.945549548)
                		  levelquest = 2500
                	   elseif MyLevel >= 2550 and MyLevel <= 2599 then
                		  Ms = "Duke [Lv. 2550]"
                		  CFrameQuest = CFrame.new(-5411.13428, 99.7886658, -112.822998, -0.998630106, -7.69353574e-05, -0.0523244925, -8.41799774e-05, 1, 0.000136251911, 0.0523244813, 0.000140469929, -0.998630106)
                		  NameMon = "Duke"
                		  CFrameMon = CFrame.new(-5632.71289, 113.984253, -247.125961, 0.30131799, -6.24960208e-08, -0.953523695, 2.6271044e-08, 1, -5.72404062e-08, 0.953523695, -7.80249909e-09, 0.30131799)
                		  levelquest = 2550
                	   elseif MyLevel >= 2600 and MyLevel <= 2649 then
                		  Ms = "Magician [Lv. 2600]"
                		  CFrameQuest = CFrame.new(-4986.68164, 57.2847176, 50.8841896, -0.0310178436, 3.57503231e-05, -0.999518812, -7.48737921e-06, 1, 3.59998885e-05, 0.999518812, 8.60041564e-06, -0.0310178436)
                		  NameMon = "Magician"
                		  CFrameMon = CFrame.new(-5037.91406, 105.178223, -121.740501, -0.582394421, 8.39546317e-08, -0.812906325, 1.00019143e-07, 1, 3.16199262e-08, 0.812906325, -6.28909262e-08, -0.582394421)
                		  levelquest = 2600
                	   elseif MyLevel >= 2650 and MyLevel <= 2699 then
                		  Ms = "Kitsune Samurai [Lv. 2650]"
                		  CFrameQuest = CFrame.new(-5263.54248, 99.788887, 171.181122, 0.999842882, -7.33984535e-08, 0.0177273583, 7.40180539e-08, 1, -3.42953825e-08, -0.0177273583, 3.56021381e-08, 0.999842882)
                		  NameMon = "Kitsune Samurai"
                		  CFrameMon = CFrame.new(-5424.13916, 131.688141, 154.705612, 0.995510459, -9.96049678e-08, 0.0946518034, 1.02818646e-07, 1, -2.90756894e-08, -0.0946518034, 3.86771219e-08, 0.995510459)
                		  levelquest = 2650
                	   elseif MyLevel >= 2700 and MyLevel <= 2749 then
                		  Ms = "Elite Beast Pirate [Lv. 2700]"
                		  CFrameQuest = CFrame.new(-4716.62646, 29.2054806, 1160.79858, 0.995985806, 2.06220729e-08, -0.0895113423, -1.7108178e-08, 1, 4.00236466e-08, 0.0895113423, -3.83316099e-08, 0.995985806)
                		  NameMon = "Elite Beast Pirate"
                		  CFrameMon = CFrame.new(-4541.68066, 73.4863281, 1361.06641, 0.999288738, -2.97574143e-09, 0.0377090126, 4.32395852e-09, 1, -3.56716185e-08, -0.0377090126, 3.58093004e-08, 0.999288738)
                		  levelquest = 2700
                	   elseif MyLevel >= 2750 and MyLevel <= 2799 then
                		  Ms = "Bear Man [Lv. 2750]"
                		  CFrameQuest = CFrame.new(-4693.36084, 29.2054806, 1039.28101, -0.149775684, -4.1443073e-08, -0.98872, -4.69713213e-10, 1, -4.18447286e-08, 0.98872, -5.80290838e-09, -0.149775684)
                		  NameMon = "Bear Man"
                		  CFrameMon = CFrame.new(-4579.22314, 70.4768066, 901.551636, -0.130586311, -7.93420654e-08, -0.991436958, -4.07730694e-09, 1, -7.94903059e-08, 0.991436958, -6.33795327e-09, -0.130586311)
                		  levelquest = 2750
                	   elseif MyLevel >= 2800 and MyLevel <= 2849 then
                		  Ms = "Bean [Lv. 2800]"
                		  CFrameQuest = CFrame.new(-4183.52344, 29.2053852, 1300.20947, 0.997841239, 1.18413607e-06, -0.065672718, 1.30719604e-06, 1, 3.78926015e-05, 0.065672718, -3.7896647e-05, 0.997841239)
                		  NameMon = "Bean"
                		  CFrameMon = CFrame.new(-3891.14111, 178.040375, 1105.0874, -0.445667028, 2.53755132e-08, 0.895198822, -4.64731675e-09, 1, -3.06598587e-08, -0.895198822, -1.78243607e-08, -0.445667028)
                		  levelquest = 2800 
                	   elseif MyLevel >= 2850 and MyLevel <= 2899 then
                		  Ms = "Meji [Lv. 2850]"
                		  CFrameQuest = CFrame.new(-5497.05371, 58.2798157, 962.49884, -0.99999547, 6.25887508e-10, -0.00301082525, 6.16092954e-10, 1, 3.25403526e-09, 0.00301082525, 3.25216565e-09, -0.99999547)
                		  NameMon = "Meji"
                		  CFrameMon = CFrame.new(-5381.60938, 80.1047516, 1198.03455, 0.875362039, -1.1155711e-08, -0.483467966, -3.40050228e-08, 1, -8.46434887e-08, 0.483467966, 9.05340372e-08, 0.875362039)
                		  levelquest = 2850
                	   elseif MyLevel >= 2900 and MyLevel <= 2949 then
                		  Ms = "Pachy Woman [Lv. 2900]"
                		  CFrameQuest = CFrame.new(-5519.28223, 57.2847939, 1179.46741, 0.0185451955, -4.25258371e-08, 0.999828041, 1.52745319e-08, 1, 4.22498339e-08, -0.999828041, 1.44883741e-08, 0.0185451955)
                		  NameMon = "Pachy Woman"
                		  CFrameMon = CFrame.new(-5854.49609, 80.562561, 1307.71936, 0.384227991, -4.96963892e-09, -0.923238218, -4.33990976e-09, 1, -7.1889934e-09, 0.923238218, 6.76898315e-09, 0.384227991)
                		  levelquest = 2900
                	   elseif MyLevel >= 2950 and MyLevel <= 2999 then
                		  Ms = "Kappa [Lv. 2950]"
                		  CFrameQuest = CFrame.new(-5110.59521, 57.3348389, 1888.76257, -0.120027594, -4.31698339e-08, 0.992770553, 3.68587427e-09, 1, 4.39298269e-08, -0.992770553, 8.93201957e-09, -0.120027594)
                		  NameMon = "Kappa"
                		  CFrameMon = CFrame.new(-4867.6001, 107.785645, 1929.43677, -0.719507813, -1.19876864e-08, -0.694484353, 1.25003119e-08, 1, -3.02119965e-08, 0.694484353, -3.0419038e-08, -0.719507813)
                		  levelquest = 2950
                	   elseif MyLevel >= 3000 and MyLevel <= 3024 then
                		  Ms = "Joey [Lv. 3000]"
                		  CFrameQuest = CFrame.new(-5157.09521, 57.3348389, 1878.33569, 0.0893014595, -1.1613297e-08, -0.996004641, 2.80153278e-09, 1, -1.14086971e-08, 0.996004641, -1.77152626e-09, 0.0893014595)
                		  NameMon = "Joey"
                		  CFrameMon = CFrame.new(-5167.18994, 107.27552, 2249.62842, 0.934725642, 9.39269569e-08, 0.355370194, -9.93821061e-08, 1, -2.90388469e-09, -0.355370194, -3.26031042e-08, 0.934725642)
                		  levelquest = 3000
                	   elseif MyLevel >= 3025 and MyLevel <= 3074 then
                		  Ms = "Skull Pirate [Lv. 3050]"
                		  CFrameQuest = CFrame.new(-6177.64746, 57.7061729, 6895.72705, 0.144290283, -1.22720292e-06, -0.989535391, 1.83615657e-06, 1, -9.7243958e-07, 0.989535391, -1.67662836e-06, 0.144290283)
                		  NameMon = "Skull Pirate"
                		  CFrameMon = CFrame.new(-6367.95068, 57.7564583, 7038.27197, -0.69726634, -2.0455003e-08, 0.716812134, -2.41681892e-08, 1, 5.02689312e-09, -0.716812134, -1.38189682e-08, -0.69726634)
                		  levelquest = 3025
                	   elseif MyLevel >= 3075 and MyLevel <= 3099 then
                		  Ms = "Elite Skeleton [Lv. 3100]"
                		  CFrameQuest = CFrame.new(-6040.38135, 158.240204, 7226.19189, -0.743768156, 6.60973001e-08, -0.66843766, -1.89540494e-09, 1, 1.00992274e-07, 0.66843766, 7.63818022e-08, -0.743768156)
                		  NameMon = "Elite Skeleton"
                		  CFrameMon = CFrame.new(-5977.66992, 159.611298, 7240.16406, -0.0595243759, -6.52750103e-08, -0.998226881, -4.92027352e-09, 1, -6.50975593e-08, 0.998226881, 1.03665754e-09, -0.0595243759)
                		  levelquest = 3075
                	   elseif MyLevel >= 3100 and MyLevel <= 3124 then
                		  Ms = "Desert Thief [Lv.3125]"
                		  CFrameQuest = CFrame.new(1552.64941, 14.3847094, 1328.57507, -0.231841326, -9.8319175e-09, 0.972753644, 2.86659532e-08, 1, 1.69394063e-08, -0.972753644, 3.18121636e-08, -0.231841326)
                		  NameMon = "Desert Thief"
                		  CFrameMon = CFrame.new(1538.53003, 27.8345203, 1625.54199, 0.328910112, -1.05163437e-07, 0.94436121, 4.45309105e-08, 1, 9.58497282e-08, -0.94436121, 1.05273177e-08, 0.328910112)
                		  levelquest = 3100
                	   elseif MyLevel >= 3125 and MyLevel <= 3149 then
                		  Ms = "Anubis [Lv.3150]"
                		  CFrameQuest = CFrame.new(1848.59448, 14.3847094, 986.632263, -0.889564037, -4.03097822e-08, 0.456810504, -2.88585406e-10, 1, 8.76798296e-08, -0.456810504, 7.78649962e-08, -0.889564037)
                		  NameMon = "Anubis"
                		  CFrameMon = CFrame.new(2118.77246, 51.1627464, 949.955139, -0.0272442698, -8.35391845e-08, -0.999628782, -5.72328807e-09, 1, -8.34142213e-08, 0.999628782, 3.44860407e-09, -0.0272442698)
                		  levelquest = 3125
                	   elseif MyLevel >= 3150  and MyLevel <= 3174 then
                		  Ms = "Pharaoh [Lv.3175]"
                		  CFrameQuest = CFrame.new(2260.80273, 14.385663, 1471.92749, 0.259048581, -5.33923883e-09, 0.965864301, -2.18660712e-09, 1, 6.11439521e-09, -0.965864301, -3.69589115e-09, 0.259048581)
                		  NameMon = "Pharaoh"
                		  CFrameMon = CFrame.new(2043.01599, 48.8272209, 1632.80444, -0.505436718, 1.27903474e-08, 0.86286366, 6.55359944e-09, 1, -1.09842579e-08, -0.86286366, 1.03015325e-10, -0.505436718)
                		  levelquest = 3150
                	   elseif MyLevel >= 3175 and MyLevel <= 3224 then
                		  Ms = "Flame User [Lv. 3200]"
                		  CFrameQuest = CFrame.new(2562.16064, 14.3856649, 1600.80457, 0.102587134, -8.50545678e-09, 0.994724035, 5.66441694e-09, 1, 7.9663911e-09, -0.994724035, 4.81728257e-09, 0.102587134)
                		  NameMon = "Flame User"
                		  CFrameMon = CFrame.new(2844.49609, 59.8116188, 1680.96509, -0.999964893, 1.12312946e-07, -0.00838283077, 1.12403882e-07, 1, -1.03769482e-08, 0.00838283077, -1.13188463e-08, -0.999964893)
                		  levelquest = 3175
                	   elseif MyLevel >= 3225 and MyLevel <= 3249 then
                		  Ms = "Sunken Vessel [Lv. 3225]"
                		  CFrameQuest = CFrame.new(-930.557983, 28.6452389, 7952.36719, 0.696157753, 7.83307925e-08, -0.717888832, -8.60623075e-08, 1, 2.56555808e-08, 0.717888832, 4.39228351e-08, 0.696157753)
                		  NameMon = "Sunken Vessel"
                		  CFrameMon = CFrame.new(-996.367126, 83.6457291, 8156.66846, -0.727139473, 2.63911701e-08, 0.686489761, 3.10548494e-08, 1, -5.54992052e-09, -0.686489761, 1.72832699e-08, -0.727139473)
                		  levelquest = 3225
                	   elseif MyLevel >= 3250 and MyLevel <= 3299 then
                		  Ms = "Biscuit Man [Lv. 3250]"
                		  CFrameQuest = CFrame.new(-1297.59827, 202.274536, 8820.98633, -0.241041139, 7.04643721e-09, -0.970514894, -7.65216779e-09, 1, 9.16103815e-09, 0.970514894, 9.63472946e-09, -0.241041139)
                		  NameMon = "Biscuit Man"
                		  CFrameMon = CFrame.new(-1323.39709, 270.800171, 8938.99707, -0.149939895, -8.96195385e-09, 0.988695085, -3.30864736e-09, 1, 8.56265547e-09, -0.988695085, -1.98735983e-09, -0.149939895)
                		  levelquest = 3250
                       elseif MyLevel == 3300 or MyLevel <= 3324 then
                		  Ms = "Azlan [Lv. 3300]"
                		  CFrameQuest = CFrame.new(-550.085815, 56.9380112, -2590.99121, 0.834728837, 6.35233155e-09, 0.550661206, -3.84734093e-08, 1, 4.67847272e-08, -0.550661206, -6.02383778e-08, 0.834728837)
                		  NameMon = "Azlan"
                		  CFrameMon = CFrame.new(-738.901489, 56.8957367, -2730.4939, -0.955690086, 1.36468925e-09, 0.294374704, -1.09130038e-09, 1, -8.17880785e-09, -0.294374704, -8.13765677e-09, -0.955690086)
                		  levelquest = 3300
                    elseif MyLevel == 3325 or MyLevel <= 3399 then
                		  Ms = "The Volcano [Lv. 3325]"
                		  CFrameQuest = CFrame.new(-219.277756, 119.89669, -3489.7981, 0.876947224, 1.83696329e-08, 0.480586678, -1.38066181e-09, 1, -3.5703998e-08, -0.480586678, 3.06469943e-08, 0.876947224)
                		  NameMon = "The Volcano"
                		  CFrameMon = CFrame.new(72.8537445, 131.709091, -3642.72412, -0.00701107178, -3.32165833e-08, -0.999975443, -7.35169881e-09, 1, -3.31658541e-08, 0.999975443, 7.11898984e-09, -0.00701107178)
                		  levelquest = 3325
                    elseif MyLevel == 3400 or MyLevel <= 3424 then
                		  Ms = "Dark Beard Servant [Lv. 3400]"
                		  CFrameQuest = CFrame.new(-9269.40137, 57.7262154, -4993.9209, 0.992959023, 6.71528211e-09, 0.118458271, 1.01484976e-09, 1, -6.51958416e-08, -0.118458271, 6.48570122e-08, 0.992959023)
                		  NameMon = "Dark Beard Servant"
                		  CFrameMon = CFrame.new(-9254.66797, 59.2397766, -4646.43164, 0.356971204, -7.44977484e-08, -0.93411541, 2.61466688e-08, 1, -6.97602687e-08, 0.93411541, 4.78401485e-10, 0.356971204)
                		  levelquest = 3400
                    elseif MyLevel == 3425 or MyLevel <= 3449 then
                		  Ms = "Supreme Swordman [Lv. 3425]"
                		  CFrameQuest = CFrame.new(-9260.03223, 68.2773361, -5128.54736, -0.451508075, 2.28242616e-08, -0.892267048, 4.51957298e-08, 1, 2.70997957e-09, 0.892267048, -3.91030817e-08, -0.451508075)
                		  NameMon = "Supreme Swordman"
                		  CFrameMon = CFrame.new(-9611.25098, 199.778931, -4455.82959, 0.927582622, -4.29958469e-08, -0.373618096, 3.60890873e-08, 1, -2.54812011e-08, 0.373618096, 1.01523829e-08, 0.927582622)
                		  levelquest = 3425
                    elseif MyLevel == 3450 or MyLevel <= 3499 then
                		  Ms = "Sally [Lv. 3450]"
                		  CFrameQuest = CFrame.new(-9533.22168, 59.2438889, -4856.15381, -0.718156815, -7.64927037e-08, -0.695881307, -8.5479293e-08, 1, -2.17065228e-08, 0.695881307, 4.38947581e-08, -0.718156815)
                		  NameMon = "Sally"
                		  CFrameMon = CFrame.new(-9565.66309, 153.698364, -5231.95996, -0.74133116, -7.96226587e-08, -0.671139419, -8.64044924e-09, 1, -1.09093911e-07, 0.671139419, -7.50757678e-08, -0.74133116)
                		  levelquest = 3450
                    elseif MyLevel == 3500 or MyLevel <= 3524 then
                		  Ms = "Vice Admiral [Lv. 3500]"
                		  CFrameQuest = CFrame.new(-9849.0625, 37.8444176, 933.248413, -0.999790311, 2.18565457e-10, -0.0204764586, 2.59504263e-09, 1, -1.16032417e-07, 0.0204764586, -1.1606123e-07, -0.999790311)
                		  NameMon = "Vice Admiral"
                		  CFrameMon = CFrame.new(-10036.1797, 37.7377281, 512.030579, 0.764925539, -2.39236613e-08, 0.644118726, 7.44247552e-09, 1, 2.83033561e-08, -0.644118726, -1.68561218e-08, 0.764925539)
                		  levelquest = 3500
                    elseif MyLevel == 3525 or MyLevel <= 3549 then
                		  Ms = "Pondere [Lv. 3525]"
                		  CFrameQuest = CFrame.new(-9925.26855, 37.8444252, 1133.68909, -0.42892912, -7.72130875e-08, -0.903338134, -7.07548793e-08, 1, -5.18789776e-08, 0.903338134, 4.16631778e-08, -0.42892912)
                		  NameMon = "Pondere"
                		  CFrameMon = CFrame.new(-10134.5439, 100.180031, 1303.3938, -0.82913965, 4.5222798e-08, -0.55904156, -1.58612234e-08, 1, 1.04417943e-07, 0.55904156, 9.54441362e-08, -0.82913965)
                		  levelquest = 3525
                    elseif MyLevel == 3550 or MyLevel <= 3599 then
                		  Ms = "Hefty [Lv. 3550]"
                		  CFrameQuest = CFrame.new(-10311.208, 88.3293304, 997.455444, 0.953057289, -5.18099164e-08, 0.302790105, 2.25388934e-08, 1, 1.00165288e-07, -0.302790105, -8.86386999e-08, 0.953057289)
                		  NameMon = "Hefty"
                		  CFrameMon = CFrame.new(-10869.4326, 135.132233, 1136.11304, 0.727532685, 7.42246131e-09, -0.686073005, -3.33636097e-09, 1, 7.28078398e-09, 0.686073005, -3.00802117e-09, 0.727532685)
                		  levelquest = 3550
                	elseif MyLevel == 3600 or MyLevel <= 3624 then
                		  Ms = "Fiore Gladiator [Lv. 3600]"
                		  CFrameQuest = CFrame.new(5514.20703, 71.7241364, -2740.82471, 0.359261751, 5.34356452e-08, -0.933236837, 6.15748519e-08, 1, 8.09624439e-08, 0.933236837, -8.6550628e-08, 0.359261751)
                		  NameMon = "Fiore Gladiator"
                		  CFrameMon = CFrame.new(5319.03174, 95.4122543, -3107.75854, -0.969186664, -4.86176575e-08, 0.24632746, -2.59446775e-08, 1, 9.52895007e-08, -0.24632746, 8.59624265e-08, -0.969186664)
                		  levelquest = 3600
                	elseif MyLevel == 3625 or MyLevel <= 3649 then
                		  Ms = "Fiore Fighter [Lv. 3625]"
                		  CFrameQuest = CFrame.new(5510.6084, 72.4639053, -2593.34326, 0.831986964, 5.25152075e-07, -0.554795206, 7.59649856e-06, 1, 1.2338498e-05, 0.554795206, -1.44799706e-05, 0.831986964)
                		  NameMon = "Fiore Fighter"
                		  CFrameMon = CFrame.new(5275.52197, 118.649101, -2538.55249, -0.765334845, -5.32980131e-08, -0.643632352, -6.93096069e-08, 1, -3.93012817e-10, 0.643632352, 4.43091182e-08, -0.765334845)
                		  levelquest = 3625
                	elseif MyLevel == 3650 or MyLevel <= 3674 then
                		  Ms = "Fiore Pirate [Lv. 3650]"
                		  CFrameQuest = CFrame.new(5932.47314, 106.830025, -2853.17554, 0.996856332, 2.17219858e-05, -0.0792302936, -3.19435057e-05, 1, -0.000127742809, 0.0792302862, 0.000129872118, 0.996856332)
                		  NameMon = "Fiore Pirate"
                		  CFrameMon = CFrame.new(5961.93701, 118.739044, -3252.61792, -0.736821055, 4.39215064e-08, -0.676087856, 3.54753702e-08, 1, 2.63020663e-08, 0.676087856, -4.60455141e-09, -0.736821055)
                		  levelquest = 3650
                    elseif MyLevel == 3675 or MyLevel <= 3699 then
                		  Ms = "Lomeo [Lv. 3675]"
                		  CFrameQuest = CFrame.new(6284.05908, 71.9746628, -2158.42041, 0.964704156, 3.05130818e-08, 0.263336122, -9.96056571e-09, 1, -7.93817563e-08, -0.263336122, 7.3956933e-08, 0.964704156)
                		  NameMon = "Lomeo"
                		  CFrameMon = CFrame.new(6455.7373, 125.550575, -2005.67786, 0.226222843, 7.29846406e-08, -0.974075556, -4.66241312e-09, 1, 7.38442694e-08, 0.974075556, -1.21637171e-08, 0.226222843)
                		  levelquest = 3675
                	elseif MyLevel == 3700 or MyLevel <= 3724 then
                		  Ms = "Prince Aria [Lv. 3700]"
                		  CFrameQuest = CFrame.new(6819.2915, 106.599648, -3101.41235, -0.990944564, 2.64022848e-08, 0.134271756, 3.69659858e-08, 1, 7.61809957e-08, -0.134271756, 8.04546261e-08, -0.990944564)
                		  NameMon = "Prince Aria"
                		  CFrameMon = CFrame.new(6950.97266, 149.687698, -3505.50806, 0.901983023, -4.40049348e-08, 0.431771517, 4.9596423e-08, 1, -1.69116576e-09, -0.431771517, 2.29397266e-08, 0.901983023)
                		  levelquest = 3700
                	elseif MyLevel == 3725 or MyLevel <= 3749 then
                		  Ms = "Devastate [Lv. 3725]"
                		  CFrameQuest = CFrame.new(6819.7915, 106.876122, -2829.87573, -0.594472826, 2.02341059e-08, 0.804115713, -3.48131479e-08, 1, -5.09001055e-08, -0.804115713, -5.82525281e-08, -0.594472826)
                		  NameMon = "Devastate"
                		  CFrameMon = CFrame.new(7273.14062, 151.007462, -2315.17529, 0.513332188, 6.88698449e-08, -0.85819, -7.29349949e-08, 1, 3.6623554e-08, 0.85819, 4.37920349e-08, 0.513332188)
                		  levelquest = 3725
                	elseif MyLevel >= 3750 then
                		  Ms = "Physicus [Lv. 3750]"
                		  CFrameQuest = CFrame.new(8122.11035, 178.128525, -4137.75342, 0.887918532, -8.71234462e-08, 0.460000753, 6.97887899e-08, 1, 5.46883605e-08, -0.460000753, -1.64559122e-08, 0.887918532)
                		  NameMon = "Physicus"
                		  CFrameMon = CFrame.new(8006.67383, 176.900192, -4120.43945, 0.993575335, 4.30188329e-09, -0.11317265, -7.73356046e-09, 1, -2.98834735e-08, 0.11317265, 3.05667101e-08, 0.993575335)
                		  levelquest = 3750
                    end
                		  end
            end
            
            do  local ui =  game:GetService("CoreGui"):FindFirstChild("Ui Native Hub")  if ui then ui:Destroy() end end
            
            local UserInputService = game:GetService("UserInputService")
            local TweenService = game:GetService("TweenService")
            local RunService = game:GetService("RunService")
            local LocalPlayer = game:GetService("Players").LocalPlayer
            local Mouse = LocalPlayer:GetMouse()
            
            
            
            local function Tween(instance, properties,style,wa)
            	if style == nil or "" then
            		return Back
            	end
            	tween:Create(instance,TweenInfo.new(wa,Enum.EasingStyle[style]),{properties}):Play()
            end
            
            local ActualTypes = {
            	RoundFrame = "ImageLabel",
            	Shadow = "ImageLabel",
            	Circle = "ImageLabel",
            	CircleButton = "ImageButton",
            	Frame = "Frame",
            	Label = "TextLabel",
            	Button = "TextButton",
            	SmoothButton = "ImageButton",
            	Box = "TextBox",
            	ScrollingFrame = "ScrollingFrame",
            	Menu = "ImageButton",
            	NavBar = "ImageButton"
            }
            
            local Properties = {
            	RoundFrame = {
            		BackgroundTransparency = 1,
            		Image = "http://www.roblox.com/asset/?id=5554237731",
            		ScaleType = Enum.ScaleType.Slice,
            		SliceCenter = Rect.new(3,3,297,297)
            	},
            	SmoothButton = {
            		AutoButtonColor = false,
            		BackgroundTransparency = 1,
            		Image = "http://www.roblox.com/asset/?id=5554237731",
            		ScaleType = Enum.ScaleType.Slice,
            		SliceCenter = Rect.new(3,3,297,297)
            	},
            	Shadow = {
            		Name = "Shadow",
            		BackgroundTransparency = 1,
            		Image = "http://www.roblox.com/asset/?id=5554236805",
            		ScaleType = Enum.ScaleType.Slice,
            		SliceCenter = Rect.new(23,23,277,277),
            		Size = UDim2.fromScale(1,1) + UDim2.fromOffset(30,30),
            		Position = UDim2.fromOffset(-15,-15)
            	},
            	Circle = {
            		BackgroundTransparency = 1,
            		Image = "http://www.roblox.com/asset/?id=5554831670"
            	},
            	CircleButton = {
            		BackgroundTransparency = 1,
            		AutoButtonColor = false,
            		Image = "http://www.roblox.com/asset/?id=5554831670"
            	},
            	Frame = {
            		BackgroundTransparency = 1,
            		BorderSizePixel = 0,
            		Size = UDim2.fromScale(1,1)
            	},
            	Label = {
            		BackgroundTransparency = 1,
            		Position = UDim2.fromOffset(5,0),
            		Size = UDim2.fromScale(1,1) - UDim2.fromOffset(5,0),
            		TextSize = 14,
            		TextXAlignment = Enum.TextXAlignment.Left
            	},
            	Button = {
            		BackgroundTransparency = 1,
            		Position = UDim2.fromOffset(5,0),
            		Size = UDim2.fromScale(1,1) - UDim2.fromOffset(5,0),
            		TextSize = 14,
            		TextXAlignment = Enum.TextXAlignment.Left
            	},
            	Box = {
            		BackgroundTransparency = 1,
            		Position = UDim2.fromOffset(5,0),
            		Size = UDim2.fromScale(1,1) - UDim2.fromOffset(5,0),
            		TextSize = 14,
            		TextXAlignment = Enum.TextXAlignment.Left
            	},
            	ScrollingFrame = {
            		BackgroundTransparency = 1,
            		ScrollBarThickness = 0,
            		CanvasSize = UDim2.fromScale(0,0),
            		Size = UDim2.fromScale(1,1)
            	},
            	Menu = {
            		Name = "More",
            		AutoButtonColor = false,
            		BackgroundTransparency = 1,
            		Image = "http://www.roblox.com/asset/?id=5555108481",
            		Size = UDim2.fromOffset(20,20),
            		Position = UDim2.fromScale(1,0.5) - UDim2.fromOffset(25,10)
            	},
            	NavBar = {
            		Name = "SheetToggle",
            		Image = "http://www.roblox.com/asset/?id=5576439039",
            		BackgroundTransparency = 1,
            		Size = UDim2.fromOffset(20,20),
            		Position = UDim2.fromOffset(5,5),
            		AutoButtonColor = false
            	}
            }
            
            local Types = {
            	"RoundFrame",
            	"Shadow",
            	"Circle",
            	"CircleButton",
            	"Frame",
            	"Label",
            	"Button",
            	"SmoothButton",
            	"Box",
            	"ScrollingFrame",
            	"Menu",
            	"NavBar"
            }
            
            function FindType(String)
            	for _, Type in next, Types do
            		if Type:sub(1, #String):lower() == String:lower() then
            			return Type
            		end
            	end
            	return false
            end
            
            local Objects = {}
            
            function Objects.new(Type)
            	local TargetType = FindType(Type)
            	if TargetType then
            		local NewImage = Instance.new(ActualTypes[TargetType])
            		if Properties[TargetType] then
            			for Property, Value in next, Properties[TargetType] do
            				NewImage[Property] = Value
            			end
            		end
            		return NewImage
            	else
            		return Instance.new(Type)
            	end
            end
            
            local function GetXY(GuiObject)
            	local Max, May = GuiObject.AbsoluteSize.X, GuiObject.AbsoluteSize.Y
            	local Px, Py = math.clamp(Mouse.X - GuiObject.AbsolutePosition.X, 0, Max), math.clamp(Mouse.Y - GuiObject.AbsolutePosition.Y, 0, May)
            	return Px/Max, Py/May
            end
            
            local function CircleAnim(GuiObject, EndColour, StartColour)
            	local PX, PY = GetXY(GuiObject)
            	local Circle = Objects.new("Circle")
            	Circle.Size = UDim2.fromScale(0,0)
            	Circle.Position = UDim2.fromScale(PX,PY)
            	Circle.ImageColor3 = StartColour or GuiObject.ImageColor3
            	Circle.ZIndex = 200
            	Circle.Parent = GuiObject
            	local Size = GuiObject.AbsoluteSize.X
            	TweenService:Create(Circle, TweenInfo.new(0.4), {Position = UDim2.fromScale(PX,PY) - UDim2.fromOffset(Size/2,Size/2), ImageTransparency = 1, ImageColor3 = EndColour, Size = UDim2.fromOffset(Size,Size)}):Play()
            	spawn(function()
            		wait(0.4)
            		Circle:Destroy()
            	end)
            end
            
            
            local function MakeDraggable(topbarobject, object)
                local Dragging = nil
                local DragInput = nil	
                local DragStart = nil
                local StartPosition = nil
            
                local function Update(input)
                    local Delta = input.Position - DragStart
                    local pos =
                        UDim2.new(
                            StartPosition.X.Scale,
                            StartPosition.X.Offset + Delta.X,
                            StartPosition.Y.Scale,
                            StartPosition.Y.Offset + Delta.Y
                        )
                    local Tween = TweenService:Create(object, TweenInfo.new(0.2), {Position = pos})
                    Tween:Play()
                end
            
                topbarobject.InputBegan:Connect(
                    function(input)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                            Dragging = true
                            DragStart = input.Position
                            StartPosition = object.Position
            
                            input.Changed:Connect(
                                function()
                                    if input.UserInputState == Enum.UserInputState.End then
                                        Dragging = false
                                    end
                                end
                            )
                        end
                    end
                )
            
                topbarobject.InputChanged:Connect(
                    function(input)
                        if
                            input.UserInputType == Enum.UserInputType.MouseMovement or
                            input.UserInputType == Enum.UserInputType.Touch
                        then
                            DragInput = input
                        end
                    end
                )
            
                UserInputService.InputChanged:Connect(
                    function(input)
                        if input == DragInput and Dragging then
                            Update(input)
                        end
                    end
                )
            end
            
            
            local Lib = {}
            
            function Lib:Window(text)
                local UiNativeHub = Instance.new("ScreenGui")
                local Main = Instance.new("Frame")
                local UICornerMain = Instance.new("UICorner")
                local Top = Instance.new("Frame")
                local UICornerTop = Instance.new("UICorner")
                local logo = Instance.new("ImageLabel")
                local Tab = Instance.new("Frame")
                local ScrollingTab = Instance.new("ScrollingFrame")
                local TabList = Instance.new("UIListLayout")
                local UIPadding = Instance.new("UIPadding")
                local NameReal = Instance.new("TextLabel")
                local ImageTab = Instance.new("ImageLabel")
                local MainPage = Instance.new("Frame")
                local UICornerPage = Instance.new("UICorner")
                local PageFolder = Instance.new("Folder")
                local UIPageLayout = Instance.new("UIPageLayout")
                local Tabtoggle = false
                local abc = false
            
                UiNativeHub.Name = "Ui Native Hub"
                UiNativeHub.Parent = game.CoreGui
                UiNativeHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                
                Main.Name = "Main"
                Main.Parent = UiNativeHub
                Main.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
                Main.BorderSizePixel = 0
                Main.ClipsDescendants = true
                Main.Position = UDim2.new(0.240740746, 0, 0.286585361, 0)
                Main.Size = UDim2.new(0, 0, 0, 0)
            
                pcall(Main:TweenSize(UDim2.new(0, 700, 0, 380),"Out","Back",0.4,true))
            
                UICornerMain.CornerRadius = UDim.new(0, 4)
                UICornerMain.Name = "UICornerMain"
                UICornerMain.Parent = Main
                
                Top.Name = "Top"
                Top.Parent = Main
                Top.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
                Top.BorderSizePixel = 0
                Top.Size = UDim2.new(0, 700, 0, 38)
                
                UICornerTop.CornerRadius = UDim.new(0, 4)
                UICornerTop.Name = "UICornerTop"
                UICornerTop.Parent = Top
                
                logo.Name = "logo"
                logo.Parent = Top
                logo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                logo.BackgroundTransparency = 1.000
                logo.Position = UDim2.new(0.0157142859, 0, 0, 0)
                logo.Size = UDim2.new(0, 43, 0, 38)
                logo.Image = "rbxassetid://11634040122"
                
                NameReal.Name = "NameReal"
                NameReal.Parent = Top
                NameReal.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                NameReal.BackgroundTransparency = 1.000
                NameReal.Position = UDim2.new(0.0900000036, 0, 0, 0)
                NameReal.Size = UDim2.new(0, 170, 0, 38)
                NameReal.Font = Enum.Font.GothamBold
                NameReal.Text = text
                NameReal.TextColor3 = Color3.fromRGB(255,255,255)
                NameReal.TextSize = 16.000
                NameReal.TextXAlignment = Enum.TextXAlignment.Left
                
                ImageTab.Name = "ImageTab"
                ImageTab.Parent = Top
                ImageTab.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                ImageTab.BackgroundTransparency = 1.000
                ImageTab.Position = UDim2.new(0.940000057, 0, 0.105263151, 0)
                ImageTab.Size = UDim2.new(0, 30, 0, 30)
                ImageTab.Image = "http://www.roblox.com/asset/?id=11271966220"
                
                local TabButtonnnn = Instance.new("TextButton")
                TabButtonnnn.Parent = ImageTab
                TabButtonnnn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                TabButtonnnn.BackgroundTransparency = 1.000
                TabButtonnnn.Size = UDim2.new(0, 30, 0, 30)
                TabButtonnnn.Font = Enum.Font.SourceSans
                TabButtonnnn.Text = ""
                TabButtonnnn.TextColor3 = Color3.fromRGB(0, 0, 0)
                TabButtonnnn.TextSize = 14.000
                
                Tab.Name = "Tab"
                Tab.Parent = Main
                Tab.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
                Tab.BorderSizePixel = 0
                Tab.ClipsDescendants = true
                Tab.Position = UDim2.new(0, 0, 0.100000001, 0)
                Tab.Size = UDim2.new(0, 0, 0, 342)
                Tab.ZIndex = 2
            
                ScrollingTab.Name = "ScrollingTab"
                ScrollingTab.Parent = Tab
                ScrollingTab.Active = true
                ScrollingTab.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                ScrollingTab.BackgroundTransparency = 1.000
                ScrollingTab.BorderSizePixel = 0
                ScrollingTab.Size = UDim2.new(0, 247, 0, 342)
                ScrollingTab.ScrollBarThickness = 4
                ScrollingTab.CanvasSize = UDim2.new(0, 0, 0, 0)
                ScrollingTab.ClipsDescendants = true
            
                TabList.Name = "TabList"
                TabList.Parent = ScrollingTab
                TabList.SortOrder = Enum.SortOrder.LayoutOrder
                TabList.Padding = UDim.new(0, 3)
            
            
            
                UIPadding.Parent = ScrollingTab
                UIPadding.PaddingTop = UDim.new(0, 5)
                
                MainPage.Name = "MainPage"
                MainPage.Parent = Main
                MainPage.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
                MainPage.BorderSizePixel = 0
                MainPage.Position = UDim2.new(0.0157142859, 0, 0.126315787, 0)
                MainPage.Size = UDim2.new(0, 677, 0, 318)
                MainPage.ClipsDescendants = true
                
                UICornerPage.CornerRadius = UDim.new(0, 4)
                UICornerPage.Name = "UICornerPage"
                UICornerPage.Parent = MainPage
                
                PageFolder.Name = "PageFolder"
                PageFolder.Parent = MainPage
                
                UIPageLayout.Parent = PageFolder
                UIPageLayout.SortOrder = Enum.SortOrder.LayoutOrder
                UIPageLayout.EasingDirection = Enum.EasingDirection.InOut
                UIPageLayout.EasingStyle = Enum.EasingStyle.Quad
                UIPageLayout.GamepadInputEnabled = false
                UIPageLayout.ScrollWheelInputEnabled = false
                UIPageLayout.TouchInputEnabled = false
                UIPageLayout.TweenTime = 0.300
            
            
            
                local Black = Instance.new("Frame")
                Black.Name = "Black"
                Black.Parent = Main
                Black.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                Black.BackgroundTransparency = .3
                Black.BorderSizePixel = 0
                Black.Position = UDim2.new(0, 0, 0.086585361, 0)
                Black.Size = UDim2.new(0, 0, 0, 342)
                
                
                UserInputService.InputBegan:Connect(function(input)
            		if input.KeyCode == Enum.KeyCode.RightControl then
            			if uihide == false then
            				uihide = true
                            pcall(Main:TweenSize(UDim2.new(0, 0, 0, 0),"In","Quad",0.4,true))
            			else
            				uihide = false
            				pcall(Main:TweenSize(UDim2.new(0, 700, 0, 380),"Out","Back",0.4,true))
            			end
            		end
            	end)
                
                TabButtonnnn.MouseButton1Click:Connect(function()
                    if Tabtoggle == false then
                        Tabtoggle = true
                        TweenService:Create(
                            Tab,
                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                            {Size = UDim2.new(0, 247, 0, 342)}
                        ):Play()
                        TweenService:Create(
                            Black,
                            TweenInfo.new(0.1,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {Size = UDim2.new(0, 700, 0, 342)}
                        ):Play()
                        TweenService:Create(
                            ImageTab,
                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {ImageColor3 = Color3.fromRGB(255, 135, 0)}
                        ):Play()
                    else
                        Tabtoggle = false
                        TweenService:Create(
                            Tab,
                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {Size = UDim2.new(0, 0, 0, 342)}
                        ):Play()
                        TweenService:Create(
                            Black,
                            TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {Size = UDim2.new(0, 0, 0, 342)}
                        ):Play()
                        TweenService:Create(
                            ImageTab,
                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {ImageColor3 = Color3.fromRGB(255, 255, 255)}
                        ):Play()
                    end
                end)
            
                local Ui = {}
            
                function Ui:Tab(text)
                    local TabFrame = Instance.new("Frame")
                    local Tabb = Instance.new("Frame")
                    local UICornerTabb = Instance.new("UICorner")
                    local UIGradientTabb = Instance.new("UIGradient")
                    local TextTab = Instance.new("TextLabel")
                    local TextButton = Instance.new("TextButton")
                    local MainFramePage = Instance.new("Frame")
                    local UICornerMainFramePage = Instance.new("UICorner")
            
                    TabFrame.Name = "TabFrame"
                    TabFrame.Parent = ScrollingTab
                    TabFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TabFrame.BackgroundTransparency = 1.000
                    TabFrame.Size = UDim2.new(0, 247, 0, 40)
                    
                    Tabb.Name = "Tabb"
                    Tabb.Parent = TabFrame
                    Tabb.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Tabb.ClipsDescendants = true
                    Tabb.Position = UDim2.new(0.0445344113, 0, 0.125, 0)
                    Tabb.Size = UDim2.new(0, 222, 0, 30)
                    
                    UICornerTabb.CornerRadius = UDim.new(0, 4)
                    UICornerTabb.Name = "UICornerTabb"
                    UICornerTabb.Parent = Tabb
                    
                    UIGradientTabb.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 135, 0)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(160, 212, 255))}
                    UIGradientTabb.Name = "UIGradientTabb"
                    UIGradientTabb.Parent = Tabb
                    
                    TextTab.Name = "TextTab"
                    TextTab.Parent = Tabb
                    TextTab.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TextTab.BackgroundTransparency = 1.000
                    TextTab.Size = UDim2.new(0, 222, 0, 30)
                    TextTab.Font = Enum.Font.GothamBold
                    TextTab.Text = text
                    TextTab.TextColor3 = Color3.fromRGB(255, 255, 255)
                    TextTab.TextSize = 15.000
                    
                    TextButton.Parent = TabFrame
                    TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TextButton.BackgroundTransparency = 1.000
                    TextButton.Size = UDim2.new(0, 247, 0, 40)
                    TextButton.Font = Enum.Font.SourceSans
                    TextButton.Text = ""
                    TextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
                    TextButton.TextSize = 14.000
                    
                    MainFramePage.Name = "MainFramePage"
                    MainFramePage.Parent = PageFolder
                    MainFramePage.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
                    MainFramePage.BorderSizePixel = 0
                    MainFramePage.Position = UDim2.new(0.0925237387, 0, 0.132605091, 0)
                    MainFramePage.Size = UDim2.new(0, 677, 0, 318)
                    MainFramePage.ClipsDescendants = true
                    
                    UICornerMainFramePage.CornerRadius = UDim.new(0, 4)
                    UICornerMainFramePage.Name = "UICornerMainFramePage"
                    UICornerMainFramePage.Parent = MainFramePage
            
                    local ScrollMainPage = Instance.new("ScrollingFrame")
                    local UIListLayoutPage = Instance.new("UIListLayout")
                    
                    ScrollMainPage.Name = "ScrollMainPage"
                    ScrollMainPage.Parent = MainFramePage
                    ScrollMainPage.Active = true
                    ScrollMainPage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ScrollMainPage.BackgroundTransparency = 1.000
                    ScrollMainPage.BorderSizePixel = 0
                    ScrollMainPage.Size = UDim2.new(0, 677, 0, 318)
                    ScrollMainPage.CanvasSize = UDim2.new(0, 0, 0, 0)
                    ScrollMainPage.ScrollBarThickness = 0
                    
                    UIListLayoutPage.Name = "UIListLayoutPage"
                    UIListLayoutPage.Parent = ScrollMainPage
                    UIListLayoutPage.FillDirection = Enum.FillDirection.Horizontal
                    UIListLayoutPage.SortOrder = Enum.SortOrder.LayoutOrder
                    UIListLayoutPage.Padding = UDim.new(0, 7)
            
                    local UIPaddingPage = Instance.new("UIPadding")
                    
                    UIPaddingPage.Name = "UIPaddingPage"
                    UIPaddingPage.Parent = ScrollMainPage
                    UIPaddingPage.PaddingLeft = UDim.new(0, 7)
                    UIPaddingPage.PaddingTop = UDim.new(0, 12)
            
                    MakeDraggable(Top,Main)
            
            
                    TextButton.MouseButton1Click:Connect(function()
                        CircleAnim(Tabb, Color3.fromRGB(255,255,255), Color3.fromRGB(255,255,255))
                        TextTab.TextSize = 0
                        TweenService:Create(
                            TextTab,
                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                            {TextSize = 15}
                        ):Play()
                        for i,v in next, PageFolder:GetChildren() do 
                            if v.Name == "MainFramePage" then
                                currenttab = v.Name
                            end
                            UIPageLayout:JumpTo(MainFramePage)
                            
                        end
            		end)
            
            		if abc == false then
                        UIPageLayout:JumpToIndex(1)
            			abc = true
            		end
            
                    local Tab = {}
            
                    function Tab:Page()
            
                        local MainFramePage_2 = Instance.new("Frame")
                        local UICornerMainFramePage_2 = Instance.new("UICorner")
                        local ScrollingMainFramePage = Instance.new("ScrollingFrame")
                        local UIListLayoutMainFramePage = Instance.new("UIListLayout")
            
            
            
                        MainFramePage_2.Name = "MainFramePage"
                        MainFramePage_2.Parent = ScrollMainPage
                        MainFramePage_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
                        MainFramePage_2.BorderSizePixel = 0
                        MainFramePage_2.ClipsDescendants = true
                        MainFramePage_2.Position = UDim2.new(-0.010447761, 0, -0.00326797389, 0)
                        MainFramePage_2.Size = UDim2.new(0, 328, 0, 296)
            
                        UICornerMainFramePage_2.CornerRadius = UDim.new(0, 4)
                        UICornerMainFramePage_2.Name = "UICornerMainFramePage"
                        UICornerMainFramePage_2.Parent = MainFramePage_2
            
                        ScrollingMainFramePage.Name = "ScrollingMainFramePage"
                        ScrollingMainFramePage.Parent = MainFramePage_2
                        ScrollingMainFramePage.Active = true
                        ScrollingMainFramePage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                        ScrollingMainFramePage.BackgroundTransparency = 1.000
                        ScrollingMainFramePage.BorderSizePixel = 0
                        ScrollingMainFramePage.Size = UDim2.new(0, 328, 0, 296)
                        ScrollingMainFramePage.CanvasSize = UDim2.new(0, 0, 0, 0)
                        ScrollingMainFramePage.ScrollBarThickness = 0
            
                        UIListLayoutMainFramePage.Name = "UIListLayoutMainFramePage"
                        UIListLayoutMainFramePage.Parent = ScrollingMainFramePage
                        UIListLayoutMainFramePage.SortOrder = Enum.SortOrder.LayoutOrder
                        UIListLayoutMainFramePage.Padding = UDim.new(0, 8)
            
            
                        local UIPaddingMainFramePage = Instance.new("UIPadding")
            
                        UIPaddingMainFramePage.Name = "UIPaddingMainFramePage"
                        UIPaddingMainFramePage.Parent = ScrollingMainFramePage
                        UIPaddingMainFramePage.PaddingTop = UDim.new(0, 9)
                        
                        
                        game:GetService("RunService").Stepped:Connect(function()
                            pcall(function()
                                ScrollingMainFramePage.CanvasSize = UDim2.new(0,0,0,UIListLayoutMainFramePage.AbsoluteContentSize.Y + 26)
                                ScrollingTab.CanvasSize = UDim2.new(0,0,0,TabList.AbsoluteContentSize.Y + 10)
                            end)
                        end)
            
                        local main = {}
                        function main:Toggle2(text,default,callback)
                            local ToggleFrame2 = Instance.new("Frame")
                            local TextToggle2 = Instance.new("TextLabel")
                            local Toggle_2 = Instance.new("Frame")
                            local UICornerToggle2 = Instance.new("UICorner")
                            local Tgle2 = Instance.new("ImageLabel")
                            local ButtonTgle2 = Instance.new("TextButton")
                            local toggle2 = false
                            local lock2 = false
            
                            ToggleFrame2.Name = "ToggleFrame2"
                            ToggleFrame2.Parent = ScrollingMainFramePage
                            ToggleFrame2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ToggleFrame2.BackgroundTransparency = 1.000
                            ToggleFrame2.ClipsDescendants = true
                            ToggleFrame2.Size = UDim2.new(0, 328, 0, 32)
            
                            TextToggle2.Name = "TextToggle2"
                            TextToggle2.Parent = ToggleFrame2
                            TextToggle2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            TextToggle2.BackgroundTransparency = 1.000
                            TextToggle2.Position = UDim2.new(0.23780489, 0, 0, 0)
                            TextToggle2.Size = UDim2.new(0, 192, 0, 32)
                            TextToggle2.Font = Enum.Font.GothamBold
                            TextToggle2.Text = "Auto Farm Level"
                            TextToggle2.TextColor3 = Color3.fromRGB(255, 255, 255)
                            TextToggle2.TextSize = 14.000
                            TextToggle2.TextXAlignment = Enum.TextXAlignment.Left
            
                            Toggle_2.Name = "Toggle"
                            Toggle_2.Parent = ToggleFrame2
                            Toggle_2.BackgroundColor3 = Color3.fromRGB(39, 39, 39)
                            Toggle_2.BorderSizePixel = 0
                            Toggle_2.Position = UDim2.new(0.103658535, 0, 0.0625, 0)
                            Toggle_2.Size = UDim2.new(0, 28, 0, 28)
            
                            UICornerToggle2.CornerRadius = UDim.new(0, 4)
                            UICornerToggle2.Name = "UICornerToggle2"
                            UICornerToggle2.Parent = Toggle_2
            
                            Tgle2.Name = "Tgle2"
                            Tgle2.Parent = Toggle_2
                            Tgle2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            Tgle2.BackgroundTransparency = 1.000
                            Tgle2.Position = UDim2.new(0.0357142873, 0, 0.0357142873, 0)
                            Tgle2.Size = UDim2.new(0, 26, 0, 26)
                            Tgle2.Image = "rbxassetid://6031068421"
                            Tgle2.ImageColor3 = Color3.fromRGB(255, 135, 0)
            
                            ButtonTgle2.Name = "ButtonTgle2"
                            ButtonTgle2.Parent = ToggleFrame2
                            ButtonTgle2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ButtonTgle2.BackgroundTransparency = 1.000
                            ButtonTgle2.Size = UDim2.new(0, 328, 0, 32)
                            ButtonTgle2.Font = Enum.Font.SourceSans
                            ButtonTgle2.Text = ""
                            ButtonTgle2.TextColor3 = Color3.fromRGB(0, 0, 0)
                            ButtonTgle2.TextSize = 14.000
            
                            
                            if default == false then
                                toggle_lol = false
                                TweenService:Create(
                                    Tgle2,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {ImageTransparency = 1}
                                ):Play()
                                callback(toggle_lol)
                            end
                            if default == true then
                                toggle_lol = true
                                TweenService:Create(
                                    Tgle2,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {ImageTransparency = 0}
                                ):Play()
                                callback(toggle_lol)
                            end
                            ButtonTgle2.MouseButton1Click:Connect(function()
                                if Tabtoggle == false then
                                    if toggle_lol == false and lock2 == false then
                                        toggle_lol = true
                                        TweenService:Create(
                                            Tgle2,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {ImageTransparency = 0}
                                        ):Play()
                                        callback(toggle_lol)
                                    elseif toggle_lol == true and lock2 == false then
                                        toggle_lol = false
                                        TweenService:Create(
                                            Tgle2,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {ImageTransparency = 1}
                                        ):Play()
                                        callback(toggle_lol)
                                    end
                                end
                            end
                            )
                        end
            
                        function main:Button(text,callback)
                            local FrameButton = Instance.new("Frame")
                            local Btn = Instance.new("Frame")
                            local UICornerBtn = Instance.new("UICorner")
                            local UIGradientBtn = Instance.new("UIGradient")
                            
                            local TextLabelBtn = Instance.new("TextLabel")
                            local ButtonBtn = Instance.new("TextButton")
            
                            FrameButton.Name = "FrameButton"
                            FrameButton.Parent = ScrollingMainFramePage
                            FrameButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            FrameButton.BackgroundTransparency = 1.000
                            FrameButton.Size = UDim2.new(0, 328, 0, 32)
                            
                            Btn.Name = "Btn"
                            Btn.Parent = FrameButton
                            Btn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            Btn.BorderSizePixel = 0
                            Btn.Position = UDim2.new(0.0487804897, 0, 0.03125, 0)
                            Btn.Size = UDim2.new(0, 296, 0, 30)
                            Btn.ClipsDescendants = true
            
                            UICornerBtn.CornerRadius = UDim.new(0, 4)
                            UICornerBtn.Name = "UICornerBtn"
                            UICornerBtn.Parent = Btn
                            
            
            
            
                            UIGradientBtn.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 135, 0)), ColorSequenceKeypoint.new(0.50, Color3.fromRGB(101, 185, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 135, 0))}
                            UIGradientBtn.Name = "UIGradientBtn"
                            UIGradientBtn.Parent = Btn
                            
                            TextLabelBtn.Name = "TextLabelBtn"
                            TextLabelBtn.Parent = Btn
                            TextLabelBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            TextLabelBtn.BackgroundTransparency = 1.000
                            TextLabelBtn.Size = UDim2.new(0, 296, 0, 30)
                            TextLabelBtn.Font = Enum.Font.GothamBold
                            TextLabelBtn.Text = text
                            TextLabelBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
                            TextLabelBtn.TextSize = 14.000
                            
                            ButtonBtn.Name = "ButtonBtn"
                            ButtonBtn.Parent = FrameButton
                            ButtonBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ButtonBtn.BackgroundTransparency = 1.000
                            ButtonBtn.Size = UDim2.new(0, 328, 0, 31)
                            ButtonBtn.Font = Enum.Font.SourceSans
                            ButtonBtn.Text = ""
                            ButtonBtn.TextColor3 = Color3.fromRGB(0, 0, 0)
                            ButtonBtn.TextSize = 14.000
                            
                            ButtonBtn.MouseButton1Click:Connect(function()
                                if Tabtoggle == false then
                                    CircleAnim(Btn, Color3.fromRGB(255,255,255), Color3.fromRGB(255,255,255))
                                    TextLabelBtn.TextSize = 0
                                    TweenService:Create(
                                        TextLabelBtn,
                                        TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                        {TextSize = 14}
                                    ):Play()
                                    callback()
                                end
                            end)
                        end
                        function main:Line()
                            local LineFrame = Instance.new("Frame")
            				local Line = Instance.new("Frame")
            				local LineUIGradient = Instance.new("UIGradient")
            
            				LineFrame.Name = "LineFrame"
            				LineFrame.Parent = ScrollingMainFramePage
            				LineFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            				LineFrame.BackgroundTransparency = 1.000
            				LineFrame.Size = UDim2.new(0, 328, 0, 21)
            
            				Line.Name = "LineMain"
            				Line.Parent = LineFrame
            				Line.AnchorPoint = Vector2.new(0.5, 0.5)
            				Line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            				Line.BorderSizePixel = 0
            				Line.Position = UDim2.new(0.5, 0, 0.428571433, 0)
            				Line.Size = UDim2.new(0, 296, 0, 2)
            
            				LineUIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(15, 15, 15)), ColorSequenceKeypoint.new(0.16, Color3.fromRGB(0,90,165)), ColorSequenceKeypoint.new(0.51, Color3.fromRGB(255, 135, 0)), ColorSequenceKeypoint.new(0.85, Color3.fromRGB(0,90,165)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(15, 15, 15))}
            				LineUIGradient.Name = "LineUIGradient"
            				LineUIGradient.Parent = Line
                        end
                        function main:Label(text)
                            local LabelFrame = Instance.new("Frame")
                            local textlabel = Instance.new("TextLabel")
                            local labelfunc = {}
            
            
                            LabelFrame.Name = "LabelFrame"
                            LabelFrame.Parent = ScrollingMainFramePage
                            LabelFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            LabelFrame.BackgroundTransparency = 1.000
                            LabelFrame.ClipsDescendants = true
                            LabelFrame.Size = UDim2.new(0, 328, 0, 32)
            
                            textlabel.Name = "TextToggle"
                            textlabel.Parent = LabelFrame
                            textlabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            textlabel.BackgroundTransparency = 1.000
                            textlabel.Position = UDim2.new(0.090, 0, 0, 0)
                            textlabel.Size = UDim2.new(0, 192, 0, 32)
                            textlabel.Font = Enum.Font.GothamBold
                            textlabel.Text = text
                            textlabel.TextColor3 = Color3.fromRGB(255, 255, 255)
                            textlabel.TextSize = 14.000
                            textlabel.TextXAlignment = Enum.TextXAlignment.Left
            
                            function labelfunc:Refresh(newtext)
                                textlabel.Text = newtext
                            end
            
                            return labelfunc
                        end
                        function main:Toggle(text,default,callback)
                            local ToggleFrame = Instance.new("Frame")
                            local TextToggle = Instance.new("TextLabel")
                            local Toggle = Instance.new("Frame")
                            local UICornerToggle = Instance.new("UICorner")
                            local Tgle = Instance.new("Frame")
                            local UICornerTgle = Instance.new("UICorner")
                            local ButtonToggle = Instance.new("TextButton")
                            default = default or false
                            local toggle = default
                            local RetrunStatsToggle = {}
                            local lock = false
            
                            ToggleFrame.Name = "ToggleFrame"
                            ToggleFrame.Parent = ScrollingMainFramePage
                            ToggleFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ToggleFrame.BackgroundTransparency = 1.000
                            ToggleFrame.ClipsDescendants = true
                            ToggleFrame.Size = UDim2.new(0, 328, 0, 32)
            
                            TextToggle.Name = "TextToggle"
                            TextToggle.Parent = ToggleFrame
                            TextToggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            TextToggle.BackgroundTransparency = 1.000
                            TextToggle.Position = UDim2.new(0.104, 0, 0, 0)
                            TextToggle.Size = UDim2.new(0, 192, 0, 32)
                            TextToggle.Font = Enum.Font.GothamBold
                            TextToggle.Text = text
                            TextToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
                            TextToggle.TextSize = 14.000
                            TextToggle.TextXAlignment = Enum.TextXAlignment.Left
            
                            Toggle.Name = "Toggle"
                            Toggle.Parent = ToggleFrame
                            Toggle.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
                            Toggle.BorderSizePixel = 0
                            Toggle.Position = UDim2.new(0.713414609, 0, 0.09375, 0)
                            Toggle.Size = UDim2.new(0, 56, 0, 25)
            
                            UICornerToggle.CornerRadius = UDim.new(0, 9999)
                            UICornerToggle.Name = "UICornerToggle"
                            UICornerToggle.Parent = Toggle
            
                            Tgle.Name = "Tgle"
                            Tgle.Parent = Toggle
                            Tgle.BackgroundColor3 = Color3.fromRGB(255, 135, 0)
                            Tgle.Position = UDim2.new(0, 1, 0, 2)
                            Tgle.Size = UDim2.new(0, 22, 0, 22)
            
                            UICornerTgle.CornerRadius = UDim.new(0, 9999)
                            UICornerTgle.Name = "UICornerTgle"
                            UICornerTgle.Parent = Tgle
            
                            ButtonToggle.Name = "ButtonToggle"
                            ButtonToggle.Parent = ToggleFrame
                            ButtonToggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ButtonToggle.BackgroundTransparency = 1.000
                            ButtonToggle.Size = UDim2.new(0, 328, 0, 32)
                            ButtonToggle.Font = Enum.Font.SourceSans
                            ButtonToggle.Text = ""
                            ButtonToggle.TextColor3 = Color3.fromRGB(0, 0, 0)
                            ButtonToggle.TextSize = 14.000
            
            
                            if default == false then
                                toggle = false
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Position = UDim2.new(0, 1.5, 0, 2)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Size = UDim2.new(0, 32, 0, 22)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Size = UDim2.new(0, 22, 0, 22)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Position = UDim2.new(0, 1, 0, 2)}
                                ):Play()
                                callback(toggle)
                            end
                            if default == true then
                                toggle = true
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Size = UDim2.new(0, 32, 0, 22)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Position = UDim2.new(0, 30, 0, 2)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Size = UDim2.new(0, 22, 0, 22)}
                                ):Play()
                                wait()
                                TweenService:Create(
                                    Tgle,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                    {Position = UDim2.new(0, 33, 0, 2)}
                                ):Play()
                                callback(toggle)
                            end
            
                            ButtonToggle.MouseButton1Click:Connect(function()
                                if Tabtoggle == false then
                                    if toggle == false and lock == false then
                                        toggle = true
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 32, 0, 22)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Position = UDim2.new(0, 30, 0, 2)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 22, 0, 22)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Position = UDim2.new(0, 33, 0, 2)}
                                        ):Play()
                                        callback(toggle)
                                    elseif toggle == true and lock == false then
                                        toggle = false
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Position = UDim2.new(0, 1.5, 0, 2)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 32, 0, 22)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 22, 0, 22)}
                                        ):Play()
                                        wait()
                                        TweenService:Create(
                                            Tgle,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                            {Position = UDim2.new(0, 1, 0, 2)}
                                        ):Play()
                                        callback(toggle)
                                    end
                                end
                            end
                            )
            
                            local lockerframe = Instance.new("Frame")
            
                            lockerframe.Name = "lockerframe"
                            lockerframe.Parent = ToggleFrame
                            lockerframe.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                            lockerframe.BackgroundTransparency = 1
                            lockerframe.BorderSizePixel = 0
                            lockerframe.Size = UDim2.new(0, 300, 0, 32)
                            lockerframe.Position = UDim2.new(0.5, 0, 0.5, 0)
                            lockerframe.AnchorPoint = Vector2.new(0.5, 0.5)
                
                            local LockerImageLabel = Instance.new("ImageLabel")
                
                            LockerImageLabel.Parent = lockerframe
                            LockerImageLabel.BackgroundTransparency = 1.000
                            LockerImageLabel.BorderSizePixel = 0
                            LockerImageLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
                            LockerImageLabel.AnchorPoint = Vector2.new(0.5, 0.5)
                            LockerImageLabel.Size = UDim2.new(0, 0, 0, 0)
                            LockerImageLabel.Image = "http://www.roblox.com/asset/?id=3926305904"
                            LockerImageLabel.ImageRectOffset = Vector2.new(404, 364)
                            LockerImageLabel.ImageRectSize = Vector2.new(36, 36)
                            LockerImageLabel.ImageColor3 = Color3.fromRGB(255,25,25)
            
                            function RetrunStatsToggle:Lock()
                                TweenService:Create(
                                    lockerframe,
                                    TweenInfo.new(.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                    {BackgroundTransparency = 0.7}
                                ):Play()
                                TweenService:Create(
                                    LockerImageLabel,
                                    TweenInfo.new(.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                    {Size = UDim2.new(0, 30, 0, 30)}
                                ):Play()
                                lock = true
                            end
            
                            function RetrunStatsToggle:ChangeStateTrue()
                                if toggle == false and lock == false then
                                    toggle = true
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Size = UDim2.new(0, 32, 0, 22)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Position = UDim2.new(0, 30, 0, 2)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Size = UDim2.new(0, 22, 0, 22)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Position = UDim2.new(0, 33, 0, 2)}
                                    ):Play()
                                    callback(toggle)
                                end
                            end
            
                            function RetrunStatsToggle:ChangeStateFalse()
                                if toggle == true and lock == false then
                                    toggle = false
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Position = UDim2.new(0, 1.5, 0, 2)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Size = UDim2.new(0, 32, 0, 22)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Size = UDim2.new(0, 22, 0, 22)}
                                    ):Play()
                                    wait()
                                    TweenService:Create(
                                        Tgle,
                                        TweenInfo.new(0.2,Enum.EasingStyle.Back,Enum.EasingDirection.Out),
                                        {Position = UDim2.new(0, 1, 0, 2)}
                                    ):Play()
                                    callback(toggle)
                                end
                            end
                            function RetrunStatsToggle:Unlock()
                                TweenService:Create(
                                    lockerframe,
                                    TweenInfo.new(.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                    {BackgroundTransparency = 1}
                                ):Play()
                                TweenService:Create(
                                    LockerImageLabel,
                                    TweenInfo.new(.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                    {Size = UDim2.new(0, 0, 0, 0)}
                                ):Play()
                                lock = false
                            end
                            return RetrunStatsToggle
                        end
                        function main:Slider(text,min,max,set,callback)
                            local sliderfunc = {}
                            local SliderFrame = Instance.new("Frame")
                            local ClickHere = Instance.new("TextButton")
                            local Bar = Instance.new("Frame")
                            local UICornerBar = Instance.new("UICorner")
                            local BarValue = Instance.new("Frame")
                            local UICornerBarValue = Instance.new("UICorner")
                            local TextSlider = Instance.new("TextLabel")
            
                            
                            SliderFrame.Name = "SliderFrame"
                            SliderFrame.Parent = ScrollingMainFramePage
                            SliderFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            SliderFrame.BackgroundTransparency = 1.000
                            SliderFrame.Position = UDim2.new(0, 0, 0.292682916, 0)
                            SliderFrame.Size = UDim2.new(0, 328, 0, 56)
            
                            ClickHere.Name = "ClickHere"
                            ClickHere.Parent = SliderFrame
                            ClickHere.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ClickHere.BackgroundTransparency = 1.000
                            ClickHere.ClipsDescendants = true
                            ClickHere.Position = UDim2.new(0.0853658542, 0, 0.642857134, 0)
                            ClickHere.Size = UDim2.new(0, 271, 0, 5)
                            ClickHere.Font = Enum.Font.SourceSans
                            ClickHere.Text = ""
                            ClickHere.TextColor3 = Color3.fromRGB(0, 0, 0)
                            ClickHere.TextSize = 14.000
            
                            Bar.Name = "Bar"
                            Bar.Parent = ClickHere
                            Bar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            Bar.ClipsDescendants = true
                            Bar.Size = UDim2.new(0, 271, 0, 5)
            
                            UICornerBar.CornerRadius = UDim.new(0, 99)
                            UICornerBar.Name = "UICornerBar"
                            UICornerBar.Parent = Bar
            
                            BarValue.Name = "BarValue"
                            BarValue.Parent = ClickHere
                            BarValue.BackgroundColor3 = Color3.fromRGB(255, 135, 0)
                            BarValue.Size = UDim2.new((set or 0) / max, 0, 0, 5)
            
                            UICornerBarValue.CornerRadius = UDim.new(0, 99)
                            UICornerBarValue.Name = "UICornerBarValue"
                            UICornerBarValue.Parent = BarValue
            
                            TextSlider.Name = "TextSlider"
                            TextSlider.Parent = SliderFrame
                            TextSlider.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            TextSlider.BackgroundTransparency = 1.000
                            TextSlider.Position = UDim2.new(0.0792682916, 0, 0.196428567, 0)
                            TextSlider.Size = UDim2.new(0, 200, 0, 21)
                            TextSlider.Font = Enum.Font.GothamBold
                            TextSlider.Text = text.." : "..tostring(set and math.floor( (set / max) * (max - min) + min) or 0)
                            TextSlider.TextColor3 = Color3.fromRGB(255, 255, 255)
                            TextSlider.TextSize = 14.000
                            TextSlider.TextXAlignment = Enum.TextXAlignment.Left
            
            
                            
                            local mouse = game.Players.LocalPlayer:GetMouse()
                            local uis = game:GetService("UserInputService")
            
            
                            if Value == nil then
                                Value = set
                                pcall(function()
                                    callback(Value)
                                end)
                            end
            
                            
                            ClickHere.MouseButton1Down:Connect(function()
                                if Tabtoggle == false then
                                    Value = math.floor((((tonumber(max) - tonumber(min)) / 271) * BarValue.AbsoluteSize.X) + tonumber(min)) or 0
                                    TweenService:Create(
                                        BarValue,
                                        TweenInfo.new(0.1,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                        {Size = UDim2.new(0, math.clamp(mouse.X - BarValue.AbsolutePosition.X, 0, 271), 0, 5)}
                                    ):Play()
                                    moveconnection = mouse.Move:Connect(function()
                                        TextSlider.Text = text.." : "..Value
                                        Value = math.floor((((tonumber(max) - tonumber(min)) / 271) * BarValue.AbsoluteSize.X) + tonumber(min))
                                        TweenService:Create(
                                            BarValue,
                                            TweenInfo.new(0.1,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, math.clamp(mouse.X - BarValue.AbsolutePosition.X, 0, 271), 0, 5)}
                                        ):Play()
                                    end)
                                    releaseconnection = uis.InputEnded:Connect(function(Mouse)
                                        if Mouse.UserInputType == Enum.UserInputType.MouseButton1 then
                                            Value = math.floor((((tonumber(max) - tonumber(min)) / 271) * BarValue.AbsoluteSize.X) + tonumber(min))
                                            pcall(function()
                                                callback(Value)
                                                TextSlider.Text = text.." : "..Value
                                            end)
                                            TweenService:Create(
                                                BarValue,
                                                TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                                {Size = UDim2.new(0, math.clamp(mouse.X - BarValue.AbsolutePosition.X, 0, 271), 0, 5)}
                                            ):Play()
                                            moveconnection:Disconnect()
                                            releaseconnection:Disconnect()
                                        end
                                    end)
                                end
                            end)
            
                            function sliderfunc:Update(value)
                                TextSlider.Text = text.." : "..value
                                BarValue:TweenSize(UDim2.new((value or 0) / max, 0, 0, 5), "Out", "Sine", 0.2, true)
                                pcall(function()
                                    callback(value)
                                end)
                            end
                            return sliderfunc
                        end  
                        function main:Dropdown(text,option,set,callback)
                            local DropFrame = Instance.new("Frame")
                            local Text = Instance.new("TextLabel")
                            local DropImage = Instance.new("ImageLabel")
                            local DownFrame = Instance.new("Frame")
                            local ScrollingDown = Instance.new("ScrollingFrame")
                            local ItemList = Instance.new("UIListLayout")
                            local Frame = Instance.new("Frame")
                            local CornerFrae = Instance.new("UICorner")
                            local ButtonDrop = Instance.new("TextButton")
                            local DropToggle = false
                            local RetrunDrop = {}
            
                            DropFrame.Name = "DropFrame"
                            DropFrame.Parent = ScrollingMainFramePage
                            DropFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            DropFrame.BackgroundTransparency = 1.000
                            DropFrame.Position = UDim2.new(0, 0, 0.522648096, 0)
                            DropFrame.Size = UDim2.new(0, 328, 0, 35)
                            
                            Frame.Parent = DropFrame
                            Frame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
                            Frame.BorderSizePixel = 0
                            Frame.Position = UDim2.new(0.0457317084, 0, 0.0285714287, 0)
                            Frame.Size = UDim2.new(0, 296, 0, 32)
                            Frame.ClipsDescendants = true
            
                            DropImage.Name = "DropImage"
                            DropImage.Parent = Frame
                            DropImage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            DropImage.BackgroundTransparency = 1.000
                            DropImage.Position = UDim2.new(0.871374369, 0, -0.012, 0)
                            DropImage.Rotation = 180.000
                            DropImage.Size = UDim2.new(0, 32, 0, 32)
                            DropImage.Image = "rbxassetid://6031094670"
                            
                            Text.Name = "Text"
                            Text.Parent = Frame
                            Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            Text.BackgroundTransparency = 1.000
                            Text.Position = UDim2.new(0.0354317725, 0, -0.012, 0)
                            Text.Size = UDim2.new(0, 221, 0, 32)
                            Text.Font = Enum.Font.GothamBold
                            Text.Text = text.." : "..set
                            Text.TextColor3 = Color3.fromRGB(255, 255, 255)
                            Text.TextSize = 14.000
                            Text.TextXAlignment = Enum.TextXAlignment.Left
                            
                            CornerFrae.CornerRadius = UDim.new(0, 4)
                            CornerFrae.Name = "CornerFrae"
                            CornerFrae.Parent = Frame
            
                            ButtonDrop.Name = "ButtonToggle"
                            ButtonDrop.Parent = DropFrame
                            ButtonDrop.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ButtonDrop.BackgroundTransparency = 1.000
                            ButtonDrop.Size = UDim2.new(0, 328, 0, 40)
                            ButtonDrop.Font = Enum.Font.SourceSans
                            ButtonDrop.Text = ""
                            ButtonDrop.TextColor3 = Color3.fromRGB(0, 0, 0)
                            ButtonDrop.TextSize = 14.000
            
            
                            DownFrame.Name = "DownFrame"
                            DownFrame.Parent = ScrollingMainFramePage
                            DownFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            DownFrame.BackgroundTransparency = 1.000
                            DownFrame.BorderColor3 = Color3.fromRGB(27, 42, 53)
                            DownFrame.ClipsDescendants = true
                            DownFrame.Position = UDim2.new(0, 0, 0.1, 0)
                            DownFrame.Size = UDim2.new(0, 328, 0, 0)
            
                            ScrollingDown.Name = "ScrollingDown"
                            ScrollingDown.Parent = DownFrame
                            ScrollingDown.Active = true
                            ScrollingDown.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                            ScrollingDown.BackgroundTransparency = 1.000
                            ScrollingDown.BorderSizePixel = 0
                            ScrollingDown.Size = UDim2.new(0, 328, 0, 98)
                            ScrollingDown.CanvasSize = UDim2.new(0, 0, 0, 0)
                            ScrollingDown.ScrollBarThickness = 0
                            ScrollingDown.BottomImage = ""
                            ScrollingDown.TopImage = ""
            
                            ItemList.Name = "ItemList"
                            ItemList.Parent = ScrollingDown
                            ItemList.SortOrder = Enum.SortOrder.LayoutOrder
                            ItemList.Padding = UDim.new(0, 3)
            
                            local SelectionScrollingUIPadding = Instance.new("UIPadding")
                            SelectionScrollingUIPadding.Name = "SelectionScrollingUIPadding"
                            SelectionScrollingUIPadding.Parent = ScrollingDown
            
                            if set ~= nil then
                                callback(set)
                            end
            
                            for i,v in pairs(option) do
                                local ItemFrame = Instance.new("Frame")
                                local ItemButton = Instance.new("TextButton")
                                local UICorner = Instance.new("UICorner")
            
            
                                ItemFrame.Name = "ItemFrame"
                                ItemFrame.Parent = ScrollingDown
                                ItemFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                                ItemFrame.BackgroundTransparency = 1.000
                                ItemFrame.Size = UDim2.new(0, 328, 0, 24)
                
                                ItemButton.Name = "ItemButton"
                                ItemButton.Parent = ItemFrame
                                ItemButton.BackgroundColor3 = Color3.fromRGB(255, 135, 0)
                                ItemButton.BorderSizePixel = 0
                                ItemButton.Position = UDim2.new(0.0701219514, 0, 0, 0)
                                ItemButton.Size = UDim2.new(0, 282, 0, 24)
                                ItemButton.AutoButtonColor = false
                                ItemButton.Font = Enum.Font.GothamBold
                                ItemButton.Text = tostring(v)
                                ItemButton.ClipsDescendants = true
                                ItemButton.TextColor3 = Color3.fromRGB(255, 255, 255)
                                ItemButton.TextSize = 14.000
                
                                UICorner.CornerRadius = UDim.new(0, 4)
                                UICorner.Parent = ItemButton
            
                                ItemButton.MouseButton1Down:Connect(function()
                                    if Tabtoggle == false then
                                        ItemButton.TextSize = 0
                                        TweenService:Create(
                                            ItemButton,
                                            TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                            {TextSize = 12}
                                        ):Play()
                                        Text.Text = tostring(text.." : "..v)
                                        CircleAnim(ItemButton,Color3.fromRGB(255,255,255),Color3.fromRGB(255,255,255))
                                        
                                        callback(v)
                                        DropToggle = false
                                        TweenService:Create(
                                            DownFrame,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 328, 0, 0)}
                                        ):Play()
                                        TweenService:Create(
                                            DropImage,
                                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Rotation = 180}
                                        ):Play()
                                    end         
                                end)
                            end 
            
                            ScrollingDown.CanvasSize = UDim2.new(0,0,0,ItemList.AbsoluteContentSize.Y + 10)
                            ButtonDrop.MouseButton1Click:Connect(function()
                                if Tabtoggle == false then
                                    if DropToggle == false then
                                        DropToggle = true
                                        TweenService:Create(
                                            DownFrame,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 328, 0, 98)}
                                        ):Play()
                                        TweenService:Create(
                                            DropImage,
                                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Rotation = 270}
                                        ):Play()
                                        CircleAnim(Frame,Color3.fromRGB(255,255,255),Color3.fromRGB(255,255,255))
                                    elseif DropToggle == true then
                                        DropToggle = false
                                        TweenService:Create(
                                            DownFrame,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 328, 0, 0)}
                                        ):Play()
                                        TweenService:Create(
                                            DropImage,
                                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Rotation = 180}
                                        ):Play()
                                        CircleAnim(Frame,Color3.fromRGB(255,255,255),Color3.fromRGB(255,255,255))
                                    end
                                end
                            end
                            )
            
                            function RetrunDrop:Add(newtext)
                                local ItemFrame = Instance.new("Frame")
                                local ItemButton = Instance.new("TextButton")
                                local UICorner = Instance.new("UICorner")
            
            
                                ItemFrame.Name = "ItemFrame"
                                ItemFrame.Parent = ScrollingDown
                                ItemFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                                ItemFrame.BackgroundTransparency = 1.000
                                ItemFrame.Size = UDim2.new(0, 328, 0, 24)
                
                                ItemButton.Name = "ItemButton"
                                ItemButton.Parent = ItemFrame
                                ItemButton.BackgroundColor3 = Color3.fromRGB(255, 135, 0)
                                ItemButton.BorderSizePixel = 0
                                ItemButton.Position = UDim2.new(0.0701219514, 0, 0, 0)
                                ItemButton.Size = UDim2.new(0, 282, 0, 24)
                                ItemButton.AutoButtonColor = false
                                ItemButton.Font = Enum.Font.GothamBold
                                ItemButton.Text = tostring(newtext)
                                ItemButton.ClipsDescendants = true
                                ItemButton.TextColor3 = Color3.fromRGB(255, 255, 255)
                                ItemButton.TextSize = 14.000
                
                                UICorner.CornerRadius = UDim.new(0, 4)
                                UICorner.Parent = ItemButton
            
                                ItemButton.MouseButton1Down:Connect(function()
                                    if Tabtoggle == false then
                                        ItemButton.TextSize = 0
                                        TweenService:Create(
                                            ItemButton,
                                            TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out,0.1),
                                            {TextSize = 12}
                                        ):Play()
                                        Text.Text = tostring(text.." : "..newtext)
                                        CircleAnim(ItemButton,Color3.fromRGB(255,255,255),Color3.fromRGB(255,255,255))
                                        
                                        callback(newtext)
                                        DropToggle = false
                                        TweenService:Create(
                                            DownFrame,
                                            TweenInfo.new(0.2,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Size = UDim2.new(0, 328, 0, 0)}
                                        ):Play()
                                        TweenService:Create(
                                            DropImage,
                                            TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                            {Rotation = 180}
                                        ):Play()
                                    end
                                end)
            
                                ScrollingDown.CanvasSize = UDim2.new(0,0,0,ItemList.AbsoluteContentSize.Y + 10)
                            end
            
                            function RetrunDrop:Clear()
                                Text.Text = tostring(text).." : "
                                DropToggle = false
                                TweenService:Create(
                                    DownFrame,
                                    TweenInfo.new(0.2,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                    {Size = UDim2.new(0, 328, 0, 0)}
                                ):Play()
                                TweenService:Create(
                                    DropImage,
                                    TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
                                    {Rotation = 180}
                                ):Play()
                                for i, v in next, ScrollingDown:GetChildren() do
                                    if v:IsA("Frame") then
                                        v:Destroy()
                                    end
                                end
                                ScrollingDown.CanvasSize = UDim2.new(0,0,0,ItemList.AbsoluteContentSize.Y + 10)
                            end
                            return RetrunDrop
                        end
                        return main
                    end
                    return Tab
                end
                return Ui
            end
            
            local Win = Lib:Window("WINNABLE HUB NEXT GEN / KING LEGACY [Free Version]")
            local Main = Win:Tab("Auto Farm")
            local Main1 = Win:Tab("Stats")
            local Main2 = Win:Tab("Teleport, Combat")
            local Page1 = Main:Page()
            local Page3 = Main:Page()
            local Page5 = Main:Page()
            local Page2 = Main1:Page()
            local Page4 = Main2:Page()
            local Page6 = Main2:Page()
            
            Page1:Label("|| Menu : Auto Farm ||")
            
            Page1:Toggle('Auto Farm Level', Auto_Farm_Level_Value,function(a)
                _G.Farm1 = a
            end)
            
            Page1:Toggle('Bring Fruits', Bring_Fruits_Value,function(a)
            _G.Bring_Fruits = a
            end)
            
            Page1:Toggle('Auto Dungeon', Auto_Dungeon_Value,function(a)
            _G.Raid = a
            end)
            
            Page1:Toggle('Auto Sea King', Auto_Sea_King_Value,function(a)
            _G.AB = a
            end)
            
            Page1:Toggle('Auto Sea King Hop', Auto_Sea_King_HOP_Value,function(a)
            _G.ABHOP = a
            end)
            
            Page1:Toggle('Auto Ghost Ship', Auto_Ghost_Ship_Value,function(a)
            _G.GS = a
            end)
            
            Page1:Toggle('Auto Ghost Ship Hop', Auto_Ghost_Ship_HOP_Value,function(a)
            _G.GSHOP = a
            end)
            
            Page1:Toggle('Auto Hydra', Auto_Hydra_Value,function(a)
            _G.AUTOHYDRA = a
            end)
            
            Page1:Toggle('Auto Hydra Hop', Auto_Hydra_Hop_Value,function(a)
            _G.AUTOHYDRAHOP = a
            end)
            
            Page1:Toggle('Auto Kris Kringle', Auto_Kris_Kringle_Value,function(a)
            _G.AutoKrisKringle = a
            end)
            
            Page1:Toggle('Auto Kris Kringle Hop', Auto_Kris_Kringle_Hop_Value,function(a)
            _G.AutoKrisKringlehop = a
            end)
            
            if Awakeworld then
            Page1:Toggle('Auto Kill Awake User', Auto_Kill_Awake_User_Value,function(a)
            _G.AutoKillAwakeUser = a
            end)
            end
            
            spawn(function()
                while wait(3) do
                    pcall(function()
                        if _G.AutoKillAwakeUser then
                            game:GetService("Workspace").Rig.Humanoid.Health = 0
                        end
                    end)
                end
            end)
            
            Page3:Label("|| Menu : Settings ||")
            
            Page3:Dropdown('Farm Mode',{"Under","Behind","Above"},Mode_Value,function(a)
                ModeFarm = a
            end)
            
            Page3:Slider('Distance',0,20,Distance_Value,function(a)
                Disc = a
            end)
            
            Page3:Toggle('Auto Buso',true,function(a)
            _G.auto_buso = a
            end)
            
            Page2:Label("|| Menu : Auto Stats ||")
            
            Page2:Toggle('Melee',false,function(a)
            _G.Melee = a
            end)
            
            spawn(function()
                while wait(.1) do
                        pcall(function()
                if _G.Melee then
                local args = {
                    [1] = "Melee",
                    [2] = 1
                }
                
                game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer(unpack(args))
                    end
                end)
                end
                end)
            
            Page2:Toggle('Defense',false,function(a)
            _G.Defense = a
            end)
            
            spawn(function()
                while wait(.1) do
                        pcall(function()
                if _G.Defense then
                local args = {
                    [1] = "Defense",
                    [2] = 1
                }
                
                game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer(unpack(args))
                    end
                end)
                end
                end)
            
            Page2:Toggle('Sword',false,function(a)
            _G.Sword = a
            end)
            
            spawn(function()
                while wait(.1) do
                        pcall(function()
                if _G.Sword then
                
                local args = {
                    [1] = "Sword",
                    [2] = 1
                }
                
                game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer(unpack(args))
                    end
                end)
                end
                end)
            
            Page2:Toggle('Devil Fruits',false,function(a)
            _G.DV = a
            end)
            
            spawn(function()
                while wait(.1) do
                        pcall(function()
                if _G.DV then
                
                local args = {
                    [1] = "Devil Fruit",
                    [2] = 1
                }
                
                game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer(unpack(args))
                    end
                end)
                end
            end)
            
            local plr = game.Players.LocalPlayer.Character
            
            Page4:Label("|| Menu : Teleport ||")
            
            if Second then
            Page4:Button('Floresco',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-3608.646, 57.5826988, 160.000565, 0.0456355102, 1.22325616e-07, -0.99895817, 7.50814699e-09, 1, 1.22796195e-07, 0.99895817, -1.31041915e-08, 0.0456355102)
            end)
            
            Page4:Button('Carcer',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-4175.37646, 29.181221, 728.014282, -0.99993062, -3.01168068e-09, -0.0117809307, -2.48150323e-09, 1, -4.50176358e-08, 0.0117809307, -4.49852777e-08, -0.99993062)
            end)
            
            Page4:Button('Torrefacio',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-5227.55469, 57.2605362, 884.378784, -0.966552854, 1.92205327e-08, 0.256467551, 4.52069955e-08, 1, 9.54289092e-08, -0.256467551, 1.03831212e-07, -0.966552854)
            end)
            
            Page4:Button('Town',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-4893.10889, 57.3135757, 109.934685, -0.00527231488, -4.04450873e-08, -0.999986112, 5.5773576e-08, 1, -4.07397067e-08, 0.999986112, -5.59875915e-08, -0.00527231488)
            end)
            
            Page4:Button('Bibernus Land',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-4547.16016, 135.859268, -882.595276, -0.022397358, 6.57495605e-08, 0.999749124, 8.26872348e-09, 1, -6.55808137e-08, -0.999749124, 6.79781209e-09, -0.022397358)
            end)
            
            Page4:Button('Viridans',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-5128.18896, 57.3105812, 1867.23145, -0.999544501, 8.19426749e-10, 0.0301790796, -4.84270846e-10, 1, -4.31914096e-08, -0.0301790796, -4.31863505e-08, -0.999544501)
            end)
            
            Page4:Button('Loaf Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-503.40979, 31.3806286, 8111.52832, 0.0323876254, -7.63452803e-08, 0.99947536, -1.69292385e-08, 1, 7.69339437e-08, -0.99947536, -1.94120648e-08, 0.0323876254)
            end)
            
            Page4:Button('Pirate Skull Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-9224.66895, 68.2530746, -5142.64697, -0.105733849, -1.26546524e-08, 0.994394481, -1.1601321e-09, 1, 1.26026318e-08, -0.994394481, 1.78895815e-10, -0.105733849)
            end)
            
            Page4:Button('Soldier Headquater',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-9594.72363, 38.0389366, 949.128723, 0.036350973, -1.0084741e-08, -0.999339104, 5.69070346e-09, 1, -9.88441151e-09, 0.999339104, -5.32763433e-09, 0.036350973)
            end)
            
            Page4:Button('Skull Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-6515.68945, 57.7280312, 5887.50391, -0.999794066, -3.18208357e-08, 0.0202925727, -3.38155104e-08, 1, -9.7952622e-08, -0.0202925727, -9.86186492e-08, -0.999794066)
            end)
            
            Page4:Button('Shred Endangering',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-246.855988, 87.4386368, -2642.31543, -0.931596339, 2.21765895e-08, -0.363494515, 2.8494469e-09, 1, 5.37066001e-08, 0.363494515, 4.89971157e-08, -0.931596339)
            end)
            
            Page4:Button('Dead Tundra',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(1191.93616, 14.4119368, 894.651001, -0.796500087, -4.73328148e-11, -0.604638398, 1.16199139e-08, 1, -1.53853854e-08, 0.604638398, -1.92803071e-08, -0.796500087)
            end)
            end
            
            if First then
            Page4:Button('Starter Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-2072.18921, 50.3854713, -4516.56836, -0.654326141, 4.34985115e-09, 0.756212473, 4.03417022e-10, 1, -5.40309086e-09, -0.756212473, -3.23031446e-09, -0.654326141)
            end)
            
            Page4:Button('Pirate Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-704.948608, 37.8912697, -3397.54565, 0.493620813, -3.69503823e-08, -0.869677246, 5.26104804e-09, 1, -3.95013409e-08, 0.869677246, 1.49232697e-08, 0.493620813)
            end)
            
            Page4:Button('Soldier Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-2450.41113, 39.8136711, -2758.32642, -0.535985231, -4.10941903e-09, -0.844227374, -7.5463269e-10, 1, -4.38856551e-09, 0.844227374, -1.71512471e-09, -0.535985231)
            end)
            
            Page4:Button('Shark Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-929.259949, 11.8385868, -1458.98999, -0.56667918, 8.41435934e-08, -0.823938549, 3.65844279e-08, 1, 7.6962003e-08, 0.823938549, 1.34694433e-08, -0.56667918)
            end)
            
            Page4:Button('Chef Ship',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-4178.00342, 108.555962, -2955.41211, 0.926670015, -1.4859457e-09, -0.37587592, -2.45815031e-08, 1, -6.45555787e-08, 0.37587592, 6.90613149e-08, 0.926670015)
            end)
            
            Page4:Button('Snow Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-5395.58643, 19.8804817, -1442.20007, 0.966743171, 3.85389569e-08, 0.255749226, -2.22864944e-08, 1, -6.64465034e-08, -0.255749226, 5.85369477e-08, 0.966743171)
            end)
            
            Page4:Button('Desert Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-2974.81494, 12.8409767, -815.079651, 0.846248925, 1.45274885e-08, -0.532787681, 3.63969939e-08, 1, 8.50778008e-08, 0.532787681, -9.13888698e-08, 0.846248925)
            end)
            
            Page4:Button('Sky Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-4310.24561, 200.702255, 1001.38171, -0.0642776191, 1.20231081e-09, 0.997932076, -1.88011029e-08, 1, -2.41579667e-09, -0.997932076, -1.89175058e-08, -0.0642776191)
            end)
            
            Page4:Button('Bubble Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(1596.59021, 12.2156076, 631.993958, -0.389158368, 2.18212239e-08, -0.92117089, 1.74855175e-09, 1, 2.29498784e-08, 0.92117089, 7.32042249e-09, -0.389158368)
            end)
            
            Page4:Button('Lobby Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-1225.15344, 13.0903521, 2187.74365, -0.995096207, -4.64995198e-09, -0.0989120603, -1.81246662e-09, 1, -2.87768067e-08, 0.0989120603, -2.84564159e-08, -0.995096207)
            end)
            
            Page4:Button('Zombie Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-2560.81616, 26.4420376, 3772.50073, -0.844309807, -2.84365971e-08, 0.535855293, 5.26759858e-10, 1, 5.38976579e-08, -0.535855293, 4.57885889e-08, -0.844309807)
            end)
            
            Page4:Button('War Island',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(2369.16968, 50.846386, -2111.46436, 0.026684491, -6.33284074e-08, 0.999643922, -3.99007263e-08, 1, 6.44160778e-08, -0.999643922, -4.16054284e-08, 0.026684491)
            end)
            
            Page4:Button('Fish Land',function(a)
            plr.HumanoidRootPart.CFrame = CFrame.new(-1209.05737, 7.28109694, 6196.20312, -0.413021326, -5.75245673e-09, 0.910721362, -3.20620891e-10, 1, 6.17096907e-09, -0.910721362, 2.25674546e-09, -0.413021326)
            end)
            end
            
            Page6:Toggle('Auto Bounty', Auto_Bounty_Value,function(a)
            _G.Auto_Bounty = a
            end)
            
            Page6:Toggle('Auto Bounty Hop', Auto_Bounty_Hop_Value,function(a)
            _G.Auto_Bounty_Hop = a
            end)
            
            function attack()
            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
            
            if v.ClassName == "Tool" then
            
            game:GetService("ReplicatedStorage").Remotes.Functions.SkillAction:InvokeServer("SW_" ..v.Name.. "_M1")
            
            end
            end
                
            end
            
            function attack3()
            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
            
            if v.ClassName == "Tool" then
            
            game:GetService("ReplicatedStorage").Remotes.Functions.SkillAction:InvokeServer("FS_" ..v.Name.. "_M1")
            
            end
            end
                
            end
            
            function attack4()
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            
            if v.ClassName == "Tool" then
            
            game:GetService("ReplicatedStorage").Remotes.Functions.SkillAction:InvokeServer("FS_" ..v.Name.. "_M1")
            
            end
            end
                
            end
            
            function attack2()
                
                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            
            if v.ClassName == "Tool" then
            
            game:GetService("ReplicatedStorage").Remotes.Functions.SkillAction:InvokeServer("SW_" ..v.Name.. "_M1")
            
            end
            end
            end
            
                spawn(function()
                   while wait(.3) do
                    pcall(function()
                        if _G.Bring_Fruits then
            for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                if v.ClassName == "Tool" then
                    v.Handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                end
            end
                        end
                    end)
                   end
                end)
            
                spawn(function()
                   while wait(.1) do
                    pcall(function()
                        if _G.Farm2 then
                            if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
            attack2()
            attack3()
            end
                        end
                    end)
                   end
                end)
                
                spawn(function()
                   while wait(.1) do
                    pcall(function()
                        if _G.Farm2 then
                            if game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
            attack4()
            attack()
                            end
                    end
                    end)
                   end
                end)
            
                    spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Modeeee then
                    if ModeFarm == "Under" then
            	        ModeFarm2 = CFrame.new(0,-Disc,0) * CFrame.Angles(math.rad(90),0,0)
            	    elseif ModeFarm == "Behind" then
            	        ModeFarm2 = CFrame.new(0,0,Disc)
            	    elseif ModeFarm == "Above" then
            	        ModeFarm2 = CFrame.new(0,Disc,0) * CFrame.Angles(math.rad(-90),0,0)
            	    else
            	        ModeFarm2 = CFrame.new(0,0,Disc)
            	    end
                        end
            end)
            end)
            end)
                
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.AUTOHYDRA then
                _G.Farm2 = true
                _G.NoClip = true
                if game:GetService("Workspace").Island["Sea King Water"]:FindFirstChild("SeaBeastChest")  or not game:GetService("Workspace").SeaMonster:FindFirstChild("HydraSeaKing") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Island["Sea King Water"].SeaBeastChest.RootPart.CFrame
                elseif game:GetService("Workspace").SeaMonster:FindFirstChild("HydraSeaKing")  and not game:GetService("Workspace").Island["Sea King Water"]:FindFirstChild("SeaBeastChest") then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame  = game:GetService("Workspace").SeaMonster.HydraSeaKing.HumanoidRootPart.CFrame * CFrame.new(0,50,-50)
            elseif _G.AUTOHYDRA == false then
                _G.Farm2 = false
                _G.NoClip = false
            end
                   end
                    end)
                   end)
                end)
                    vu = game:GetService("VirtualUser")
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Farm1 then
                            CheckLevel()
                if not string.find(game:GetService("Players").dadafsdgfsgtr.PlayerGui.Quest.QuestBoard.QuestCount.Text, NameMon) then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                    for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui:GetDescendants()) do
                                    if v.Name == "Dialogue" then
                        game:GetService'VirtualUser':CaptureController()
                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                wait(1)
                                       v.Accept.Size = UDim2.new(5000, 50, 50, 0)
                                       v.Accept.Position = UDim2.new(0, -900, 0, -900)
                                    end
                                   end
                                wait(.3)
                                vu:ClickButton1(Vector2.new(500,0))
            end
            end
            end)
                       end)
                    end)
            
                
                vu = game:GetService("VirtualUser")
                
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Farm1 then
                        CheckLevel()
                        if game:GetService("Players").LocalPlayer.PlayerGui.Quest.QuestBoard.Visible == true then
            if not game:GetService("Workspace").Monster.Mon:FindFirstChild(Ms) then
                                      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Monster.Boss[Ms].HumanoidRootPart.CFrame * ModeFarm2
            end
                                  end
                        end
                    end)
            end)
            end)
                
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Farm1 then
                        CheckLevel()
                _G.Farm2 = true
                _G.NoClip = true
                _G.Modeeee = true
                            if game:GetService("Players").LocalPlayer.PlayerGui.Quest.QuestBoard.Visible == false then
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                                                    for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui:GetDescendants()) do
                                    if v.Name == "Dialogue" then
                        game:GetService'VirtualUser':CaptureController()
                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                wait(1)
                                       v.Accept.Size = UDim2.new(5000, 50, 50, 0)
                                       v.Accept.Position = UDim2.new(0, -900, 0, -900)
                                    end
                                   end
                                wait(.3)
                                vu:ClickButton1(Vector2.new(500,0))
                            elseif game:GetService("Players").LocalPlayer.PlayerGui.Quest.QuestBoard.Visible == true then
                                for i,v in pairs(game:GetService("Workspace").Monster.Mon:GetChildren()) do 
                                  if v.Name == Ms and v.Humanoid.Health >= 1 then
                                      game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * ModeFarm2
                                      end
                                       if not game:GetService("Workspace").Monster.Boss:FindFirstChild(Ms) and not game:GetService("Workspace").Monster.Mon:FindFirstChild(Ms) then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
            end
            end
            elseif _G.Farm1 == false then
                _G.Farm2 = false
                _G.NoClip = false
                _G.Modeeee = false
               
                    end
                end
                end)
                end)
                end)
                
                    spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.GS then
                _G.Farm2 = true
                _G.NoClip = true
                for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                if string.find(v.Name, "Chest") and not game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Chest1.RootPart.CFrame
                    wait(.1)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Chest2.RootPart.CFrame
                    wait(.1)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Chest3.RootPart.CFrame
                    wait(.1)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Chest4.RootPart.CFrame
                elseif game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") and game:GetService("Workspace").GhostMonster["Ghost Ship"].Humanoid.Health >= 1 then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").GhostMonster["Ghost Ship"].HumanoidRootPart.CFrame * CFrame.new(0,50,0)
                elseif _G.GS == false then
                _G.Farm2 = false
                _G.NoClip = false
                end
                end
                    end
                    end)
                end) 
                end)
                
            spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.NoClip then 
                            if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                                local Noclip = Instance.new("BodyVelocity")
                                Noclip.Name = "BodyClip"
                                Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                                Noclip.MaxForce = Vector3.new(100000,100000,100000)
                                Noclip.Velocity = Vector3.new(0,0,0)
                            end
                        else
                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                        end
                    end)
                end
            end)
            
            spawn(function()
                pcall(function()
                    game:GetService("RunService").Stepped:Connect(function()
                        if _G.NoClip then
                            for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                                if v:IsA("BasePart") then
                                    v.CanCollide = false    
                                end
                            end
                        end
                    end)
                end)
            end)
                
                    spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.auto_buso then
                if game.Players.LocalPlayer.Character.Haki.Value == 0 then
                    game.Players.LocalPlayer.Character.Haki.Value = 1
                	game:GetService("Players").LocalPlayer.Character.Services.Client.Armament:FireServer()
                			 end
                        end
                			end)
                			end)
                    end)
            
               spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.AB or _G.Raid or _G.AutoKrisKringle or _G.Auto_Bounty then
                _G.Farm2 = true
                _G.NoClip = true
                _G.Modeeee = true
                else
                _G.Farm2 = false
                _G.NoClip = false
                _G.Modeeee = false
                        end
            end)
            end)
            end)
            
               spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.AutoKrisKringle then
                            if game:GetService("Workspace").Monster.Boss:FindFirstChild("Kris Kringle [Lv. 10000]") then
            				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Monster.Boss["Kris Kringle [Lv. 10000]"].HumanoidRootPart.CFrame * ModeFarm2
            				else
            				    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("ReplicatedStorage").MOB["Kris Kringle [Lv. 10000]"].HumanoidRootPart.CFrame * ModeFarm2
            				end
                   end
                        end)
            end)
            end)
            
               spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.AB then
            				for i,v in pairs(game:GetService("Workspace").SeaMonster:GetDescendants()) do
            						 if v.Humanoid.Health <= 0 or not game:GetService("Workspace").SeaMonster:FindFirstChild("SeaKing") then
            							if game:GetService("Workspace").Island:FindFirstChild("Legacy Island1") then
            							   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Island:FindFirstChild("Legacy Island1").ChestSpawner.CFrame
            							elseif game:GetService("Workspace").Island:FindFirstChild("Legacy Island2") then
            							   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Island:FindFirstChild("Legacy Island2").ChestSpawner.CFrame
            							elseif game:GetService("Workspace").Island:FindFirstChild("Legacy Island3") then
            							   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Island:FindFirstChild("Legacy Island3").ChestSpawner.CFrame
            							elseif game:GetService("Workspace").Island:FindFirstChild("Legacy Island4") then
            							   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Island:FindFirstChild("Legacy Island4").ChestSpawner.CFrame
            							elseif v.Name == "SeaKing" then
            						 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,18)
            
            	
                    end
                        end
                    end
                   end
                        end)
            end)
            end)
            
                    spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.GSHOP then
            if not game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") and not game:GetService("Workspace"):FindFirstChild("Chest1") then
                                        local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
                            end
                end
                   end)
                        end
            end)
            
                    spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.AUTOHYDRAHOP then
            if not game:GetService("Workspace").SeaMonster:FindFirstChild("HydraSeaKing") then
                                        local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
                            end
                end
                   end)
                        end
            end)
            
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Raid then
                            if First then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6731.81348, 103.697495, 955.572449, 0.0715826601, 1.15350801e-07, -0.997434676, 1.18002532e-13, 1, 1.15647488e-07, 0.997434676, -8.27847213e-09, 0.0715826601)
            end
                        end
                    end)
                   end)
                end)
            	
                spawn(function()
                   while wait() do
                    pcall(function()
                        if _G.Raid then
                            if Second then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4602.46826, 223.119171, -71.773056, 0.386346072, 7.43803383e-08, -0.922353923, 3.79542647e-10, 1, 8.08008451e-08, 0.922353923, -3.15671613e-08, 0.386346072)
            wait(0.1)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4585.50195, 223.119171, -65.6908112, -0.64535886, 3.89723676e-09, -0.763879538, 1.01225552e-08, 1, -3.45007778e-09, 0.763879538, -9.958951e-09, -0.64535886)
            end
                        end
                    end)
                   end
                end)
            
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Raid then
            if Raid then
            game:GetService("ReplicatedStorage").GoldenArenaEvents.StartEvent:FireServer()
            end
                    end
                    end)
                   end)
                end)
                
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Raid then
            if Raid then
            
            local args = {
                [1] = _G.Dungeon_Mode
            }
            
            game:GetService("ReplicatedStorage").ChooseMapRemote:FireServer(unpack(args))
            end
                    end
                    end)
                   end)
                end)
            
                spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.Raid then
                            if game.Players.LocalPlayer.Character.Humanoid.Health < 22000 then
            healingself()
            end
                    end
                    end)
                   end
                end)
            
            function healingself()
            local args = {
                [1] = "FS_Cyborg_E",
                [2] = {
                    ["Type"] = "Down",
                    ["MouseHit"] = CFrame.new(-4882.81201171875, 53.82545471191406, 1.7105255126953125) * CFrame.Angles(-0.15605567395687103, 0.07722476869821548, 0.012137485668063164)
                }
            }
            
            game:GetService("ReplicatedStorage").Remotes.Functions.SkillAction:InvokeServer(unpack(args))
                        end
            
                    spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Raid then
            for i,v in pairs(game:GetService("Workspace").MOB:GetChildren()) do
                for i,v2 in pairs(v:GetChildren()) do
                if v2.ClassName == "Tool" and v2.Name == "Flintlock" and game.Players.LocalPlayer.Character.Humanoid.Health > 22000 then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * ModeFarm2
            elseif game.Players.LocalPlayer.Character.Humanoid.Health > 22000 then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * ModeFarm2
            elseif game.Players.LocalPlayer.Character.Humanoid.Health < 22000 then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-37.8575897, 207.281296, -3.7075181, 0.038515456, 0.969142973, -0.243471608, -0.00132872199, 0.243701845, 0.969849288, 0.999257147, -0.037030682, 0.0106740091)
            end
            end
            end
                        end
                    end)
                   end)
                    end)
                
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Raid then
            for i,v in pairs(game:GetService("Workspace").MOB:GetChildren()) do
                if v.Humanoid.Health == 0 then
                    v:Destroy()
                end
            end
                       end
                    end)
                   end)
                end)
            
               spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.ABHOP then
                            if game:GetService("Workspace").SeaMonster:FindFirstChild("SeaKing").Humanoid.Health == 0 then
                            wait(10)
                                    local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
                            end
                            end
            end)
            end
            end)
            
                spawn(function()
                   game:GetService("RunService").RenderStepped:Connect(function()
                    pcall(function()
                        if _G.Auto_Bounty then
                            for i, v in pairs(game.Players:GetChildren()) do
                                if v.Name ~= game.Players.LocalPlayer.Name then
                    if game.Players.LocalPlayer.Character:FindFirstChild("LowerTorso") then
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4886.81299, 499.753448, -718.864319, 0.533848584, -2.07801225e-08, 0.845580101, -8.89226826e-08, 1, 8.0715445e-08, -0.845580101, -1.18281072e-07, 0.533848584)
                        wait(.5)
                        game.Players.LocalPlayer.Character:FindFirstChild("LowerTorso"):Remove();
                   elseif v.Character.Humanoid.Health >= 1 and not game.Players.LocalPlayer.Character:FindFirstChild("LowerTorso") then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Character.HumanoidRootPart.CFrame * ModeFarm2
                end
                                end
                            end
                        end
                    end)
            end)
            end)
            
            spawn(function()
                while wait(120) do
                    pcall(function()
                        if _G.Auto_Bounty_Hop then
                            _G.Auto_Bounty = false
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1485.09839, 407.165863, 4348.60986, 0.292715609, -5.85421596e-08, -0.956199527, 2.22957457e-08, 1, -5.43985266e-08, 0.956199527, -5.39588418e-09, 0.292715609)
            wait(30)
            local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
            end
            end)
            end
            end)
            
            spawn(function()
                while wait(30) do
                    pcall(function()
                        if _G.Auto_Bounty then 
            for i, v in pairs(game.Players:GetChildren()) do
                                if v.Name ~= game.Players.LocalPlayer.Name then
            if v.Character.Humanoid.Health == v.Character.Humanoid.MaxHealth then
                v.Character.Humanoid.Health = 0
            end
            end
            end
            end
            end)
            end
            end)
            
            
            
               spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.AutoKrisKringlehop then
            if not game:GetService("ReplicatedStorage").MOB:FindFirstChild("Kris Kringle [Lv. 10000]") and not game:GetService("Workspace").Monster.Boss:FindFirstChild("Kris Kringle [Lv. 10000]") then
                    local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
                end
                        end
            end)
            end
            end)
            
               spawn(function()
                   while wait(5) do
                    pcall(function()
                        if _G.ABHOP then
            if not game:GetService("Workspace").Island:FindFirstChild("Legacy Island1") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island2") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island3") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island4") then
                    local PlaceID = 6381829480
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            local File = pcall(function()
                AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
            end)
            if not File then
                table.insert(AllIDs, actualHour)
                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
            end
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            
            function Teleport()
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            
            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
            Teleport()
                end
                        end
            end)
            end
            end)
            elseif placeId == 9224601490 then -- Fruits Battleground
        local players = {}
        
        spawn(function()
            while wait(.1) do
                pcall(function()
                    table.clear(players)
        for i,v in pairs(game.Players:GetChildren()) do
            table.insert(players, v.Name)
        end
                            end)
                        end
        end)
        
        
        local TYU = loadstring(Game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()
         
        local PhantomForcesWindow = TYU:NewWindow("Winnable Hub / FB")
         
        local Main = PhantomForcesWindow:NewSection("Auto Farm")
        local Main2 = PhantomForcesWindow:NewSection("Combat")
         
        Main:CreateToggle("Auto Level Fruits", function(value)
        _G.auto_farm = value
        end)
        
        Main:CreateButton("Discord", function()
            local request = (syn and syn.request) or (http and http.request) or http_request
        if request then
            request(
                {
                    Url = "http://127.0.0.1:6463/rpc?v=1",
                    Method = "POST",
                    Headers = {
                        ["Content-Type"] = "application/json",
                        ["Origin"] = "https://discord.com"
                    },
                    Body = game:GetService("HttpService"):JSONEncode(
                        {
                            cmd = "INVITE_BROWSER",
                            args = {code = "Dfxktn5cMX"},
                            nonce = game:GetService("HttpService"):GenerateGUID(false)
                        }
                    )
                }
            )
        end
        end)
        
         Main2:CreateDropdown("Player(s) Select", players, 1, function(value)
        _G.SelectPlayers = value
        end)
        
        Main2:CreateToggle("Auto Farm Players", function(value)
        _G.Auto_Players = value
        end)   
        
        Main2:CreateToggle("ESP PLAYERS", function(value)
        _G.ESPPLAYERS = value
        end)    
        
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.Auto_Players then
                        for i,v in pairs(game.Players:GetChildren()) do
                            if v.Name == _G.SelectPlayers then
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,3)
        end
        end
        end
        end)
        end)
        end)
        
        spawn(function()
            while wait(.5) do
                pcall(function()
                    if _G.auto_farm then
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-570.393372, 936.071411, 1573.18884, 0.992543459, 1.21020927e-09, 0.121891484, -9.32624644e-09, 1, 6.60135981e-08, -0.121891484, -6.66581528e-08, 0.992543459)
        end
                            end)
                        end
        end)
        
        spawn(function()
            while wait(.2) do
                pcall(function()
                    if _G.Auto_Players then
        local args = {
            [1] = "Core",
            [2] = "M1",
            [3] = {}
        }
        
        game:GetService("ReplicatedStorage").Replicator:InvokeServer(unpack(args))
        end
                            end)
                        end
        end)
        
        spawn(function()
            while wait(2) do
                pcall(function()
                    if _G.auto_farm or _G.Auto_Players then
        for i,v in pairs(game:GetService("Players").LocalPlayer["MAIN_DATA"].Fruits:GetChildren()) do
        for i,v2 in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
        
        local args = {
            [1] = v.Name,
            [2] = v2.Name,
            [3] = {}
        }
        
        game:GetService("ReplicatedStorage").ReplicatorNoYield:FireServer(unpack(args))
        
        end
        end
        end
                            end)
                        end
        end)
                
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.ESPPLAYERS then
               for i,v in pairs(game.Players:GetChildren()) do
                   if v.Name ~= game.Players.LocalPlayer.Name then
                    if not v.Character.Torso:FindFirstChild("ESP") then
                        local BillboardGui = Instance.new("BillboardGui")
                        local TextLabel = Instance.new("TextLabel")
                        BillboardGui.Parent = v.Character.Torso
                        BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                        BillboardGui.Active = true
                        BillboardGui.Name = "ESP"
                        BillboardGui.AlwaysOnTop = true
                        BillboardGui.LightInfluence = 1.000
                        BillboardGui.Size = UDim2.new(0, 200, 0, 50)
                        BillboardGui.StudsOffset = Vector3.new(0, 2.5, 0)
                        TextLabel.Parent = BillboardGui
                        TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                        TextLabel.BackgroundTransparency = 1.000
                        TextLabel.Size = UDim2.new(0, 200, 0, 30)
                        TextLabel.Font = Enum.Font.SciFi
                        TextLabel.Text = v.Name.. " HP : ".. v.Character.Humanoid.Health
                        TextLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
                        TextLabel.TextScaled = true
                        TextLabel.TextSize = 1.000
                        TextLabel.TextStrokeTransparency = 0.000
                        TextLabel.TextWrapped = true
        end
        end
        end
                end
                end)
               end)
            end)
            
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Players then 
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                            local Noclip = Instance.new("BodyVelocity")
                            Noclip.Name = "BodyClip"
                            Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            Noclip.MaxForce = Vector3.new(100000,100000,100000)
                            Noclip.Velocity = Vector3.new(0,0,0)
                        end
                    else
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                    end
                end)
            end
        end)
        
        spawn(function()
            pcall(function()
                game:GetService("RunService").Stepped:Connect(function()
                    if _G.Auto_Players then
                        for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                            if v:IsA("BasePart") then
                                v.CanCollide = false    
                            end
                        end
                    end
                end)
            end)
        end)
            
            spawn(function()
               game:GetService("RunService").RenderStepped:Connect(function()
                pcall(function()
                    if _G.ESPPLAYERS then
               for i,v in pairs(game.Players:GetChildren()) do
                   if v.Name ~= game.Players.LocalPlayer.Name then
                   v.Character.Torso:FindFirstChild("ESP"):Destroy()
        end
        end
                end
                end)
               end)
            end)
            elseif placeId == 6918802270 then -- Project Neww World
                function checklevel()
            local lv = game:GetService("Players").LocalPlayer.PlayerData.Experience.Level.Value
            if lv == 1 or lv <= 9 then
                Mon = "Thief"
                Zone = "Starter Island"
                Quest1 = 1
                Quest2 = "1"
                Quest3 = "Level 1"
                CMON = CFrame.new(-2283.63794, 13.6224356, -3228.54248, 0.135328859, -9.09182205e-08, 0.990800738, 7.94203991e-09, 1, 9.06776023e-08, -0.990800738, -4.40231762e-09, 0.135328859)
            elseif lv == 10 or lv <= 24 then
                Mon = "Bandit"
                Zone = "Starter Island"
                Quest1 = 1
                Quest2 = "1"
                Quest3 = "Level 10"
                CMON = CFrame.new(-1906.97644, 13.8429213, -3118.32764, 0.0337360688, -1.27909402e-07, -0.999430776, -1.4949654e-08, 1, -1.28486889e-07, 0.999430776, 1.92757881e-08, 0.0337360688)
            elseif lv == 25 or lv <= 39 then
                Mon = "Bandit Boss"
                Zone = "Starter Island"
                Quest1 = 1
                Quest2 = "1"
                Quest3 = "Level 25"
                CMON = CFrame.new(-1838.29956, 41.9321671, -3294.60474, 0.999579072, 2.19569714e-08, 0.0290115289, -1.78533348e-08, 1, -1.41707503e-07, -0.0290115289, 1.41129902e-07, 0.999579072)
            elseif lv == 40 or lv <= 59 then
                Mon = "Pirate Clown"
                Zone = "Clown Island"
                Quest1 = 2
                Quest2 = 2
                Quest3 = "Level 40"
                CMON = CFrame.new(-2250.25537, 14.0049028, -355.49234, -0.709495246, 3.85175127e-08, 0.704710245, 1.62293445e-09, 1, -5.30232818e-08, -0.704710245, -3.64760666e-08, -0.709495246)
            elseif lv == 60 or lv <= 89 then
                Mon = "Clown Boss"
                Zone = "Clown Island"
                Quest1 = 2
                Quest2 = 2
                Quest3 = "Level 60"
                CMON = CFrame.new(-2210.07788, 33.7492981, -72.106987, -0.815615892, -4.26277644e-08, 0.578593731, 1.15915508e-08, 1, 9.00148294e-08, -0.578593731, 8.01243232e-08, -0.815615892)
            elseif lv == 90 or lv <= 119 then
                Mon = "Fishman"
                Zone = "Shark Park"
                Quest1 = 3
                Quest2 = 3
                Quest3 = "Level 90"
                CMON = CFrame.new(-4843.13281, 11.8115282, -3171.61865, 0.994148552, -1.05036371e-07, 0.108021446, 1.06401224e-07, 1, -6.87131196e-09, -0.108021446, 1.83247195e-08, 0.994148552)
            elseif lv == 160 or lv <= 199 then
                Mon = "Shark Boss"
                Zone = "Shark Park"
                Quest1 = 3
                Quest2 = 3
                Quest3 = "Level 120"
                CMON = CFrame.new(-4842.98535, 11.8115273, -3168.80737, -0.999592066, -1.08694573e-08, 0.028559655, -8.92448071e-09, 1, 6.8229717e-08, -0.028559655, 6.79470062e-08, -0.999592066)
            elseif lv == 200 or lv <= 249 then
                Mon = "Bomb Boss"
                Zone = "Desert Ruins"
                Quest1 = 4
                Quest2 = 4
                Quest3 = "Level 200"
                CMON = CFrame.new(-4976.94678, 31.9681492, 160.88327, 0.922331274, 1.14436638e-09, 0.386400104, 1.361607e-08, 1, -3.54629677e-08, -0.386400104, 3.79698548e-08, 0.922331274)
            elseif lv == 250 or lv <= 299 then
                Mon = "Krieg Pirate"
                Zone = "Sea Restaurant"
                Quest1 = 5
                Quest2 = 5
                Quest3 = "Level 250"
                CMON = CFrame.new(-5971.56396, 71.2033539, 2364.05762, 0.99996978, -2.93607538e-08, 0.00777152553, 2.97525666e-08, 1, -5.03008692e-08, -0.00777152553, 5.05305735e-08, 0.99996978)
            elseif lv == 300 or lv <= 349 then
                Mon = "Krieg Boss"
                Zone = "Sea Restaurant"
                Quest1 = 5
                Quest2 = 5
                Quest3 = "Level 300"
                CMON = CFrame.new(-6020.67334, 14.4119101, 2413.0603, -0.954065859, -4.25772519e-08, -0.299596965, -6.5195934e-08, 1, 6.55012045e-08, 0.299596965, 8.20249682e-08, -0.954065859)
            elseif lv == 350 or lv <= 399 then
                Mon = "Marine Recruit"
                Zone = "Logue Town"
                Quest1 = 6
                Quest2 = 6
                Quest3 = "Level 350"
                CMON = CFrame.new(-2886.83374, 76.1440353, 2098.49121, 0.999588728, 1.29314737e-08, -0.0286767259, -1.57039306e-08, 1, -9.64544995e-08, 0.0286767259, 9.68651648e-08, 0.999588728)
            elseif lv == 400 or lv <= 449 then
                Mon = "Tashii"
                Zone = "Logue Town"
                Quest1 = 6
                Quest2 = 6
                Quest3 = "Level 400"
                CMON = CFrame.new(-2886.83374, 76.1440353, 2098.49121, 0.999588728, 1.29314737e-08, -0.0286767259, -1.57039306e-08, 1, -9.64544995e-08, 0.0286767259, 9.68651648e-08, 0.999588728)
            elseif lv == 450 or lv <= 499 then
                Mon = "Monkey"
                Zone = "Tall Woods"
                Quest1 = 7
                Quest2 = 7
                Quest3 = "Level 450"
                CMON = CFrame.new(-299.608795, 50.5508308, 2287.24731, -0.989341915, 3.19376903e-09, 0.145610929, -7.21208293e-09, 1, -7.09355064e-08, -0.145610929, -7.12296284e-08, -0.989341915)
            elseif lv == 500 or lv <= 549 then
                Mon = "Gorilla"
                Zone = "Tall Woods"
                Quest1 = 7
                Quest2 = 7
                Quest3 = "Level 500"
                CMON = CFrame.new(623.50354, 57.5535965, 2144.8916, -0.549418092, 2.00656078e-08, 0.835547566, 4.14161008e-08, 1, 3.21842486e-09, -0.835547566, 3.63733825e-08, -0.549418092)
            elseif lv == 550 or lv <= 599 then
                Mon = "King Gorilla"
                Zone = "Tall Woods"
                Quest1 = 7
                Quest2 = 7
                Quest3 = "Level 550"
                CMON = CFrame.new(-187.307755, 79.9767227, 2937.63257, 0.353050202, -9.67595959e-09, -0.935604393, 2.03850163e-08, 1, -2.64965205e-09, 0.935604393, -1.81368502e-08, 0.353050202)
            elseif lv == 600 or lv <= 649 then
                Mon = "Marine Grunt"
                Zone = "Marine Base Town"
                Quest1 = 8
                Quest2 = 8
                Quest3 = "Level 600"
                CMON = CFrame.new(438.822479, 12.3911562, 5670.2915, -0.33976379, -1.22971811e-09, 0.940510809, -2.49369609e-08, 1, -7.70108954e-09, -0.940510809, -2.60700315e-08, -0.33976379)
            elseif lv == 650 or lv <= 699 then
                Mon = "Marine Captain"
                Zone = "Marine Base Town"
                Quest1 = 8
                Quest2 = 8
                Quest3 = "Level 650"
                CMON = CFrame.new(361.776489, 129.701019, 6320.88867, 0.831386328, 3.69294639e-09, 0.555694878, -1.05200204e-09, 1, -5.07171549e-09, -0.555694878, 3.63196273e-09, 0.831386328)
            elseif lv == 700 or lv <= 749 then
                Mon = "Satyr"
                Zone = "Three Islands"
                Quest1 = 9
                Quest2 = 9
                Quest3 = "Level 700"
                CMON = CFrame.new(-2516.38184, 855.226074, 5982.22656, 0.899187028, -1.52615094e-08, -0.437564522, -1.87108e-08, 1, -7.33286569e-08, 0.437564522, 7.41233563e-08, 0.899187028)
            elseif lv == 750 or lv <= 799 then
                Mon = "Minotaur"
                Zone = "Three Islands"
                Quest1 = 9
                Quest2 = 9
                Quest3 = "Level 750"
                CMON = CFrame.new(-2924.52783, 915.036804, 5620.08447, -0.766832173, -5.52716592e-08, -0.64184767, -7.42041593e-08, 1, 2.54028909e-09, 0.64184767, 4.95757426e-08, -0.766832173)
            elseif lv == 800 or lv <= 849 then
                Mon = "Elite Marine"
                Zone = "Marine HQ"
                Quest1 = 10
                Quest2 = 10
                Quest3 = "Level 800"
                CMON = CFrame.new(-6105.11279, 58.9645386, 6631.39404, -0.981685162, 9.44379011e-08, -0.190510526, 1.03800211e-07, 1, -3.91644015e-08, 0.190510526, -5.82221453e-08, -0.981685162)
            elseif lv == 850 or lv <= 899 then
                Mon = "Vice Admiral"
                Zone = "Marine HQ"
                Quest1 = 10
                Quest2 = 10
                Quest3 = "Level 850"
                CMON = CFrame.new(-5790.86377, 20.1127014, 7001.73145, 0.622295558, 3.15977182e-08, 0.782782376, 7.6266673e-08, 1, -1.0099631e-07, -0.782782376, 1.22549764e-07, 0.622295558)
            elseif lv >= 900 then
                Mon = "Ice Admiral"
                Zone = "Marine HQ"
                Quest1 = 10
                Quest2 = 10
                Quest3 = "Level 900"
                CMON = CFrame.new(-6682.59863, 206.256531, 6798.24121, -0.784886539, -3.88240231e-08, 0.619639516, 1.93059453e-08, 1, 8.71103225e-08, -0.619639516, 8.03344449e-08, -0.784886539)
        
            end
        end
        
        local TweenService = game:GetService('TweenService')
        local object = cre
        local tweenInfo = TweenInfo.new(2.5)
        
        while getfenv().RGB do
        local r, g, b = math.random(), math.random(), math.random()
        local goal = {Color = Color3.new(r, g, b)}
        
        local tween = TweenService:Create(object, tweenInfo, goal)
        tween:Play()
        tween.Completed:Wait()
        end
        
        if game.CoreGui:FindFirstChild("ToggleUI") then
        	game.CoreGui:FindFirstChild("ToggleUI"):Destroy()
        end
        local ToggleUI = Instance.new("ScreenGui")
        local ToggleButton = Instance.new("TextButton")
        local ToggleButtonHUI = Instance.new("UICorner")
        ToggleUI.Name = "ToggleUI"
        ToggleUI.Parent = game.CoreGui
        ToggleUI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        
        ToggleButton.Name = "ToggleButton"
        ToggleButton.Parent = ToggleUI
        ToggleButton.BackgroundColor3 = Color3.fromRGB(30,20,20)
        ToggleButton.BackgroundTransparency = 0.1
        ToggleButton.BorderSizePixel = 0
        ToggleButton.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
        ToggleButton.Size = UDim2.new(0, 50, 0, 50)
        ToggleButton.Font = Enum.Font.SourceSans
        ToggleButton.Text = ""
        ToggleButton.TextColor3 = Color3.fromRGB(0, 0, 0)
        ToggleButton.TextSize = 14.000
        ToggleButton.Draggable = true
        ToggleButton.MouseButton1Click:Connect(function()
        	game.CoreGui:FindFirstChild("Kenei").Enabled = not game.CoreGui:FindFirstChild("Kenei").Enabled
        end)
        
        coroutine.wrap(
        	function()
        	do
            local CoreGui = {}
            local CheckCoreGui = {}
            local CoreGui = game:GetService("CoreGui"):FindFirstChild("Kenei")
                if CoreGui then 
                 CoreGui:Destroy() 
                elseif CoreGui then 
                local CheckCoreGui = not game.CoreGui:FindFirstChild("Kenei").Enabled
                    if CheckCoreGui then
                    CoreGui:Destroy()
                    elseif not CoreGui and CheckCoreGuithen == nil then
                         local CoreGui = nil or {nil}
                         local CheckCoreGu = nil or {nil}
                    end
                end
            end
        end)();
        -- // variables
        local library = {}
        local pages = {}
        local sections = {}
        local multisections = {}
        local mssections = {}
        local toggles = {}
        local buttons = {}
        local sliders = {}
        local dropdowns = {}
        local multiboxs = {}
        local buttonboxs = {}
        local textboxs = {}
        local keybinds = {}
        local colorpickers = {}
        local configloaders = {}
        local watermarks = {}
        local loaders = {}
        --
        local utility = {}
        --
        local plrs = game:GetService("Players")
        local cre = game:GetService("CoreGui")
        local rs = game:GetService("RunService")
        local ts = game:GetService("TweenService") 
        local uis = game:GetService("UserInputService") 
        local hs = game:GetService("HttpService")
        local ws = game:GetService("Workspace")
        local plr = plrs.LocalPlayer
        local cam = ws.CurrentCamera
        -- // indexes
        library.__index = library
        pages.__index = pages
        sections.__index = sections
        multisections.__index = multisections
        mssections.__index = mssections
        toggles.__index = toggles
        buttons.__index = buttons
        sliders.__index = sliders
        dropdowns.__index = dropdowns
        multiboxs.__index = multiboxs
        buttonboxs.__index = buttonboxs
        textboxs.__index = textboxs
        keybinds.__index = keybinds
        colorpickers.__index = colorpickers
        configloaders.__index = configloaders
        watermarks.__index = watermarks
        loaders.__index = loaders
        -- // functions
        utility.new = function(instance,properties) 
        	-- // instance
        	local ins = Instance.new(instance)
        	-- // properties setting
        	for property,value in pairs(properties) do
        		ins[property] = value
        	end
        	-- // return
        	return ins
        end
        --
        utility.dragify = function(ins,touse)
        	local dragging
        	local dragInput
        	local dragStart
        	local startPos
        	--
        	local function update(input)
        		local delta = input.Position - dragStart
        		touse:TweenPosition(UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.1,true)
        	end
        	--
        	ins.InputBegan:Connect(function(input)
        		if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
        			dragging = true
        			dragStart = input.Position
        			startPos = touse.Position
        
        			input.Changed:Connect(function()
        				if input.UserInputState == Enum.UserInputState.End then
        					dragging = false
        				end
        			end)
        		end
        	end)
        	--
        	ins.InputChanged:Connect(function(input)
        		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
        			dragInput = input
        		end
        	end)
        	--
        	uis.InputChanged:Connect(function(input)
        		if input == dragInput and dragging then
        			update(input)
        		end
        	end)
        end
        --
        utility.round = function(n,d)
        	return tonumber(string.format("%."..(d or 0).."f",n))
        end
        --
        utility.zigzag = function(X)
        	return math.acos(math.cos(X*math.pi))/math.pi
        end
        --
        utility.capatalize = function(s)
        	local l = ""
        	for v in s:gmatch('%u') do
        		l = l..v
        	end
        	return l
        end
        --
        utility.splitenum = function(enum)
        	local s = tostring(enum):split(".")
        	return s[#s]
        end
        --
        utility.from_hex = function(h)
        	local r,g,b = string.match(h,"^#?(%w%w)(%w%w)(%w%w)$")
        	return Color3.fromRGB(tonumber(r,16), tonumber(g,16), tonumber(b,16))
        end
        --
        utility.to_hex = function(c)
        	return string.format("#%02X%02X%02X",c.R *255,c.G *255,c.B *255)
        end
        --
        utility.removespaces = function(s)
           return s:gsub(" ","")
        end
        -- // main
        function library:new(props)
        	-- // properties
        	local textsize = props.textsize or props.TextSize or props.textSize or props.Textsize or 12
        	local font = props.font or props.Font or "RobotoMono"
        	local name = props.name or props.Name or props.UiName or props.Uiname or props.uiName or props.username or props.Username or props.UserName or props.userName or "new ui"
        	local color = props.color or props.Color or props.mainColor or props.maincolor or props.MainColor or props.Maincolor or props.Accent or props.accent or Color3.fromRGB(225, 58, 81)
        	-- // variables
        	local window = {}
        	-- // main
        	local screen = utility.new(
        		"ScreenGui",
        		{
        			Name = "Kenei",
        			DisplayOrder = 9999,
        			ResetOnSpawn = false,
        			ZIndexBehavior = "Global",
        			Parent = cre
        		}
        	)
        	-- 1
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = color,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,541,0,341),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = screen
        		}
        	)
        	-- 2
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = outline
        		}
        	)
        	-- 3
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = outline2
        		}
        	)
        	-- 4
        	local main = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-10,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline2
        		}
        	)
        	-- 5
        	local outline3 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	--
        	local titletext = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextXAlignment = "Left",
        			TextSize = textsize,
        			TextStrokeTransparency = 0,
        			Parent = title
        		}
        	)
        	-- 6
        	local holder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-6,1,-6),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	-- 7
        	local holder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-6,1,-6),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Parent = main
        		}
        	)
        	-- 8
        	local tabs = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,-20),
        			Position = UDim2.new(0.5,0,1,0),
        			Parent = holder
        		}
        	)
        	--
        	local tabsbuttons = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,21),
        			Position = UDim2.new(0.5,0,0,0),
        			ZIndex = 2,
        			Parent = holder
        		}
        	)
        	-- 9
        	local outline4 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabs
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Horizontal",
        			Padding = UDim.new(0,2),
        			Parent = tabsbuttons
        		}
        	)
        	--
        	utility.dragify(title,outline)
        	-- // window tbl
        	window = {
        		["screen"] = screen,
        		["holder"] = holder,
        		["labels"] = {},
        		["tabs"] = outline4,
        		["tabsbuttons"] = tabsbuttons,
        		["outline"] = outline,
        		["pages"] = {},
        		["pointers"] = {},
        		["dropdowns"] = {},
        		["multiboxes"] = {},
        		["buttonboxs"] = {},
        		["colorpickers"] = {},
        		["x"] = true,
        		["y"] = true,
        		["key"] = Enum.KeyCode.RightShift,
        		["textsize"] = textsize,
        		["font"] = font,
        		["theme"] = {
        			["accent"] = color
        		},
        		["themeitems"] = {
        			["accent"] = {
        				["BackgroundColor3"] = {},
        				["BorderColor3"] = {},
        				["TextColor3"] = {}
        			}
        		}
        	}
        	--
        	table.insert(window.themeitems["accent"]["BackgroundColor3"],outline)
        	--
        	local toggled = true
        	local cooldown = false
        	local saved = UDim2.new(0,0,0,0)
        	--
        	uis.InputBegan:Connect(function(Input)
        		if Input.UserInputType == Enum.UserInputType.Keyboard then
        			if Input.KeyCode == window.key then
        				if cooldown == false then
        					if toggled then
        						cooldown = true
        						toggled = not toggled
        						saved = outline.Position
        						local xx,yy = 0,0
        						local xxx,yyy = 0,0
        						--
        						if (outline.AbsolutePosition.X+(outline.AbsoluteSize.X/2)) < (cam.ViewportSize.X/2) then
        							xx = -3
        						else
        							xx = 3
        						end
        						--
        						if window.y then
        							if (outline.AbsolutePosition.Y+(outline.AbsoluteSize.Y/2)) < (cam.ViewportSize.Y/2) then
        								yy = -3
        							else
        								yy = 3
        							end
        						else
        							yy = saved.Y.Scale
        							yyy = saved.Y.Offset
        						end
        						--
        						if window.x == false and window.y == false then
        							screen.Enabled = false
        						else
        							ts:Create(outline, TweenInfo.new(0.5,Enum.EasingStyle.Quad,Enum.EasingDirection.In), {Position = UDim2.new(xx,xxx,yy,yyy)}):Play()
        						end
        						wait(0.5)
        						cooldown = false
        					else
        						cooldown = true
        						toggled = not toggled
        						if window.x == false and window.y == false then
        							screen.Enabled = true
        						else
        							ts:Create(outline, TweenInfo.new(0.5,Enum.EasingStyle.Quad,Enum.EasingDirection.Out), {Position = saved}):Play()
        						end
        						wait(0.5)
        						cooldown = false
        					end
        				end
        			end
        		end
        	end)
        	--
        	window.labels[#window.labels+1] = titletext
        	-- // metatable indexing + return
        	setmetatable(window, library)
        	return window
        end
        --
        function library:watermark()
        	local watermark = {}
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = self.theme.accent,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,300,0,26),
        			Position = UDim2.new(1,-10,0,10),
        			ZIndex = 9900,
        			Visible = false,
        			Parent = self.screen
        		}
        	)
        	--
        	table.insert(self.themeitems["accent"]["BackgroundColor3"],outline)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9901,
        			Parent = outline
        		}
        	)
        	--
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9902,
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.font,
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextXAlignment = "Left",
        			TextSize = self.textsize,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local con
        	con = title:GetPropertyChangedSignal("TextBounds"):Connect(function()
        		outline.Size = UDim2.new(0,title.TextBounds.X+20,0,26)
        	end)
        	--
        	watermark = {
        		["outline"] = outline,
        		["outline2"] = outline2,
        		["indent"] = indent,
        		["title"] = title,
        		["connection"] = con
        	}
        	--
        	self.labels[#self.labels+1] = title
        	--
        	setmetatable(watermark,watermarks)
        	return watermark
        end
        --
        function watermarks:update(content)
        	local content = content or {}
        	local watermark = self
        	--
        	local text = ""
        	--
        	for i,v in pairs(content) do
        		text = text..i..": "..v.."  "
        	end
        	--
        	text = text:sub(0, -3)
        	--
        	watermark.title.Text = text
        end
        --
        function watermarks:updateside(side)
        	side = utility.removespaces(tostring(side):lower())
        	--
        	local sides = {
        		topright = {
        			AnchorPoint = Vector2.new(1,0),
        			Position = UDim2.new(1,-10,0,10)
        		},
        		topleft = {
        			AnchorPoint = Vector2.new(0,0),
        			Position = UDim2.new(0,10,0,10)
        		},
        		bottomright = {
        			AnchorPoint = Vector2.new(1,1),
        			Position = UDim2.new(1,-10,1,-10)
        		},
        		bottomleft = {
        			AnchorPoint = Vector2.new(0,1),
        			Position = UDim2.new(0,10,1,-10)
        		}
        	}
        	--
        	if sides[side] then
        		self.outline.AnchorPoint = sides[side].AnchorPoint
        		self.outline.Position = sides[side].Position
        	end
        end
        --
        function library:loader(props)
        	local name = props.name or props.Name or props.LoaderName or props.Loadername or props.loaderName or props.loadername or "Loader"
        	local scriptname = props.scriptname or props.Scriptname or props.ScriptName or props.scriptName or "Universal"
        	local closed = props.close or props.Close or props.closecallback or props.Closecallback or props.CloseCallback or props.closeCallback or function()end
        	local logedin = props.login or props.Login or props.logincallback or props.Logincallback or props.LoginCallback or props.loginCallback or function()end
        	local loader = {}
        	--
        	local screen = utility.new(
        		"ScreenGui",
        		{
        			Name = tostring(math.random(0,999999))..tostring(math.random(0,999999)),
        			DisplayOrder = 9999,
        			ResetOnSpawn = false,
        			ZIndexBehavior = "Global",
        			Parent = cre
        		}
        	)
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(168, 52, 235),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,300,0,90),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9900,
        			Visible = false,
        			Parent = screen
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(0, 0, 0),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-4,1,-4),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9901,
        			Parent = outline
        		}
        	)
        	--
        	local indent = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0.5,0,0.5,0),
        			ZIndex = 9902,
        			Parent = outline2
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = "RobotoMono",
        			Text = name,
        			TextColor3 = Color3.fromRGB(168, 52, 235),
        			TextXAlignment = "Center",
        			TextSize = 12,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local scripttitle = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,20),
        			Font = "RobotoMono",
        			Text = "Script: "..scriptname,
        			TextColor3 = Color3.fromRGB(255, 255, 255),
        			TextXAlignment = "Center",
        			TextSize = 12,
        			TextStrokeTransparency = 0,
        			ZIndex = 9903,
        			Parent = indent
        		}
        	)
        	--
        	local makebutton = function(name,parent)
        		local button_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 9904,
        				Parent = parent
        			}
        		)
        		--
        		local button_outline = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 9905,
        				Parent = button_holder
        			}
        		)
        		--
        		local button_outline2 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 9906,
        				Parent = button_outline
        			}
        		)
        		--
        		local button_color = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 9907,
        				Parent = button_outline2
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = button_color
        			}
        		)
        		--
        		local button_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = 12,
        				TextStrokeTransparency = 0,
        				Font = "RobotoMono",
        				ZIndex = 9908,
        				Parent = button_holder
        			}
        		)
        		--
        		return {button_holder,button_outline,button_button}
        	end
        	--
        	local close = makebutton("close",indent)
        	local login = makebutton("login",indent)
        	--
        	close[1].AnchorPoint = Vector2.new(0.5,0)
        	close[1].Size = UDim2.new(0.5,0,0,20)
        	close[1].Position = UDim2.new(0.5,0,0,40)
        	--
        	login[1].AnchorPoint = Vector2.new(0.5,0)
        	login[1].Size = UDim2.new(0.5,0,0,20)
        	login[1].Position = UDim2.new(0.5,0,0,62)
        	--
        	close[3].MouseButton1Down:Connect(function()
        		close[2].BorderColor3 = Color3.fromRGB(168, 52, 235)
        		outline:TweenPosition(UDim2.new(-1.5,0,0.5,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.75,true)
        		closed()
        		wait(0.05)
        		close[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait(0.7)
        		screen:Remove()
        	end)
        	--
        	login[3].MouseButton1Down:Connect(function()
        		login[2].BorderColor3 = Color3.fromRGB(168, 52, 235)
        		outline:TweenPosition(UDim2.new(1.5,0,0.5,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.75,true)
        		logedin()
        		wait(0.05)
        		login[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait(0.7)
        		screen:Remove()
        	end)
        	--
        	loader = {
        		["outline"] = outline,
        		["outline2"] = outline2,
        		["indent"] = indent,
        		["title"] = title
        	}
        	--
        	setmetatable(loader,loaders)
        	return loader
        end
        --
        function loaders:toggle()
        	self.outline.Visible = true
        end
        --
        function watermarks:toggle(bool)
        	local watermark = self
        	--
        	watermark.outline.Visible = bool
        end
        --
        function library:saveconfig()
        	local cfg = {}
        	--
        	for i,v in pairs(self.pointers) do
        		cfg[i] = {}
        		for c,d in pairs(v) do
        			cfg[i][c] = {}
        			for x,z in pairs(d) do
        				if typeof(z.current) == "Color3" then
        					cfg[i][c][x] = {z.current.R,z.current.G,z.current.B}
        				else
        					cfg[i][c][x] = z.current
        				end
        			end
        		end
        	end
        	--
        	return hs:JSONEncode(cfg)
        end
        --
        function library:loadconfig(cfg)
        	local cfg = hs:JSONDecode(readfile(cfg))
        	for i,v in pairs(cfg) do
        		for c,d in pairs(v) do
        			for x,z in pairs(d) do
        				if z ~= nil then
        					if self.pointers[i] ~= nil and self.pointers[i][c] ~= nil and self.pointers[i][c][x] ~= nil then
        						self.pointers[i][c][x]:set(z)
        					end
        				end
        			end
        		end
        	end
        end
        --
        function library:settheme(theme,color)
        	local window = self
        	--
        	if window.theme[theme] then
        		window.theme[theme] = color
        	end
        	--
        	if window.themeitems[theme] then
        		for i,v in pairs(window.themeitems[theme]) do
        			for z,x in pairs(v) do
        				x[i] = color
        			end
        		end
        	end
        end
        --
        function library:setkey(key)
        	if typeof(key) == "EnumItem" then
        		local window = self
        		window.key = key
        	end
        end
        --
        function library:settoggle(side,bool)
        	if side == "x" then
        		self.x = bool
        	else
        		self.y = bool
        	end
        end
        --
        function library:setfont(font)
        	if font ~= nil then
        		local window = self
        		for i,v in pairs(window.labels) do
        			if v ~= nil then
        				v.Font = font
        			end
        		end
        	end
        end
        --
        function library:settextsize(size)
        	if size ~= nil then
        		local window = self
        		for i,v in pairs(window.labels) do
        			if v ~= nil then
        				v.TextSize = size
        			end
        		end
        	end
        end
        --
        function library:page(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	-- // variables
        	local page = {}
        	-- // main
        	local tabbutton = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,75,1,0),
        			Parent = self.tabsbuttons
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabbutton
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = tabbutton
        		}
        	)
        	--
        	local r_line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(1,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local l_line = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(0,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local label = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.textsize,
        			TextStrokeTransparency = 0,
        			Parent = outline
        		}
        	)
        	--
        	local pageholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,-20),
        			Position = UDim2.new(0.5,0,0.5,0),
        			Visible = false,
        			Parent = self.tabs
        		}
        	)
        	--
        	local left = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(0,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = true,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,10),
        			Parent = left
        		}
        	)
        	--
        	local right = utility.new(
        		"ScrollingFrame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(1,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = true,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,10),
        			Parent = right
        		}
        	)
        	-- // page tbl
        	page = {
        		["library"] = self,
        		["outline"] = outline,
        		["r_line"] = r_line,
        		["l_line"] = l_line,
        		["line"] = line,
        		["page"] = pageholder,
        		["left"] = left,
        		["right"] = right,
        		["open"] = false,
        		["pointers"] = {}
        	}
        	--
        	table.insert(self.pages,page)
        	--
        	button.MouseButton1Down:Connect(function()
        		if page.open == false then
        			for i,v in pairs(self.pages) do
        				if v ~= page then
        					if v.open then
        						v.page.Visible = false
        						v.open = false
        						v.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        						v.line.Size = UDim2.new(1,0,0,2)
        						v.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        					end
        				end
        			end
        			--
        			self:closewindows()
        			--
        			page.page.Visible = true
        			page.open = true
        			page.outline.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			page.line.Size = UDim2.new(1,0,0,3)
        			page.line.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		self.pointers[tostring(pointer)] = page.pointers
        	end
        	--
        	self.labels[#self.labels+1] = label
        	-- // metatable indexing + return
        	setmetatable(page, pages)
        	return page
        end
        --
        function pages:openpage()
        	local page = self
        	--
        	if page.open == false then
        		for i,v in pairs(page.library.pages) do
        			if v ~= page then
        				if v.open then
        					v.page.Visible = false
        					v.open = false
        					v.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        					v.line.Size = UDim2.new(1,0,0,2)
        					v.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        				end
        			end
        		end
        		--
        		page.page.Visible = true
        		page.open = true
        		page.outline.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        		page.line.Size = UDim2.new(1,0,0,3)
        		page.line.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        	end
        end
        --
        function pages:section(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local side = props.side or props.Side or props.sectionside or props.Sectionside or props.SectionSide or props.sectionSide or "left"
        	local size = props.size or props.Size or props.yaxis or props.yAxis or props.YAxis or props.Yaxis or 200
        	side = side:lower()
        	-- // variables
        	local section = {}
        	-- // main
        	local sectionholder = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,size),
        			Parent = self[side]
        		}
        	)
        
        	--[[BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0.5,-5,1,0),
        			Position = UDim2.new(0,0,0,0),
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 1,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 0,
        			ClipsDescendants = false,
        			VerticalScrollBarInset = "None",
        			VerticalScrollBarPosition = "Right",
        			Parent = pageholder
        		}]]
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = sectionholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	--[[local content = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-12,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			Parent = outline
        		}
        	)]]
        
        	local content = utility.new(
        		'Frame',
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-12,1,-25),
        			Position = UDim2.new(0.5,0,1,-5),
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-5,0,20),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,5),
        			Parent = content
        		}
        	)
        	-- // section tbl
        	section = {
        		["library"] = self.library,
        		["sectionholder"] = sectionholder,
        		["color"] = color,
        		["content"] = content,
        		["pointers"] = {}
        	}
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = section.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(section, sections)
        	return section
        end
        --
        function pages:multisection(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local side = props.side or props.Side or props.sectionside or props.Sectionside or props.SectionSide or props.sectionSide or "left"
        	local size = props.size or props.Size or props.yaxis or props.yAxis or props.YAxis or props.Yaxis or 200
        	side = side:lower()
        	-- // variables
        	local multisection = {}
        	-- // main
        	local sectionholder = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,size),
        			Parent = self[side]
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = sectionholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local tabsholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,-15),
        			Position = UDim2.new(0,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-5,0,20),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = outline
        		}
        	)
        	--
        	local buttons = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-6,0,20),
        			Position = UDim2.new(0.5,0,0,5),
        			Parent = tabsholder
        		}
        	)
        	--
        	local tabs = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-6,1,-27),
        			Position = UDim2.new(0.5,0,1,-3),
        			Parent = tabsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Horizontal",
        			Padding = UDim.new(0,2),
        			Parent = buttons
        		}
        	)
        	--
        	local tabs_outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabs
        		}
        	)
        	-- // section tbl
        	multisection = {
        		["library"] = self.library,
        		["sectionholder"] = sectionholder,
        		["color"] = color,
        		["tabsholder"] = tabsholder,
        		["mssections"] = {},
        		["buttons"] = buttons,
        		["tabs"] = tabs,
        		["tabs_outline"] = tabs_outline,
        		["pointers"] = {}
        	}
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = multisection.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(multisection,multisections)
        	return multisection
        end
        --
        function multisections:section(props)
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	-- // variables
        	local mssection = {}
        	-- // main
        	local tabbutton = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,60,0,20),
        			Parent = self.buttons
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = tabbutton
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = tabbutton
        		}
        	)
        	--
        	local r_line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(1,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local l_line = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,1,0,1),
        			Position = UDim2.new(0,0,1,1),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local line = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(20, 20, 20),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	--
        	local label = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Parent = outline
        		}
        	)
        	--
        	local content = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,1),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-6,1,-27),
        			Position = UDim2.new(0.5,0,1,-3),
        			Parent = self.tabs_outline
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,5),
        			Parent = content
        		}
        	)
        	-- // mssection tbl
        	mssection = {
        		["library"] = self.library,
        		["outline"] = outline,
        		["r_line"] = r_line,
        		["l_line"] = l_line,
        		["line"] = line,
        		["content"] = content,
        		["open"] = false,
        		["pointers"] = {}
        	}
        	--
        	table.insert(self.mssections,mssection)
        	--
        	button.MouseButton1Down:Connect(function()
        		if mssection.open == false then
        			for i,v in pairs(self.mssections) do
        				if v ~= mssection then
        					if v.open then
        						v.page.Visible = false
        						v.open = false
        						v.outline.BackgroundColor3 = Color3.fromRGB(31, 31 ,31)
        						v.line.Size = UDim2.new(1,0,0,2)
        						v.line.BackgroundColor3 = Color3.fromRGB(31, 31 ,31)
        					end
        				end
        			end
        			--
        			mssection.library:closewindows()
        			--
        			mssection.content.Visible = true
        			mssection.open = true
        			mssection.outline.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        			mssection.line.Size = UDim2.new(1,0,0,3)
        			mssection.line.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = mssection.pointers
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = label
        	-- // metatable indexing + return
        	setmetatable(mssection,mssections)
        	return mssection
        end
        --
        function sections:toggle(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or props.toggle or props.Toggle or props.toggled or props.Toggled or false
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local toggle = {}
        	-- // main
        	local toggleholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,15,0,15),
        			Parent = toggleholder
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = toggleholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,20,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = toggleholder
        		}
        	)
        	--
        	local col = Color3.fromRGB(20, 20, 20)
        	if def then
        		col = self.library.theme.accent
        	end
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = col,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	if def then
        		table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	end
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	-- // toggle tbl
        	toggle = {
        		["library"] = self.library,
        		["toggleholder"] = toggleholder,
        		["title"] = title,
        		["color"] = color,
        		["callback"] = callback,
        		["current"] = def
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		if toggle.current then
        			toggle.callback(false)
        			toggle.color.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			local find = table.find(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BackgroundColor3"],find)
        			end
        			toggle.current = false
        		else
        			toggle.callback(true)
        			toggle.color.BackgroundColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			toggle.current = true
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = toggle
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(toggle, toggles)
        	return toggle
        end
        --
        function toggles:set(bool)
        	if bool ~= nil then
        		local toggle = self
        		toggle.callback(bool)
        		toggle.current = bool
        		if bool then
        			toggle.color.BackgroundColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        		else
        			toggle.color.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        			local find = table.find(self.library.themeitems["accent"]["BackgroundColor3"],toggle.color)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BackgroundColor3"],find)
        			end
        		end
        	end
        end
        --
        function sections:button(props)
        	-- // properties
        	local name = props.name or props.Name or "new button"
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local button = {}
        	-- // main
        	local buttonholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,20),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = buttonholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	local gradient = utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local buttonpress = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = buttonholder
        		}
        	)
        	--
        	buttonpress.MouseButton1Down:Connect(function()
        		callback()
        		outline.BorderColor3 = self.library.theme.accent
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        		wait(0.05)
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end)
        	-- // button tbl
        	button = {
        		["library"] = self.library
        	}
        	--
        	self.library.labels[#self.library.labels+1] = buttonpress
        	-- // metatable indexing + return
        	setmetatable(button, buttons)
        	return button
        end
        --
        function sections:slider(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or 0
        	local max = props.max or props.Max or props.maximum or props.Maximum or 100
        	local min = props.min or props.Min or props.minimum or props.Minimum or 0
        	local rounding = props.rounding or props.Rounding or props.round or props.Round or props.decimals or props.Decimals or false
        	local ticking = props.tick or props.Tick or props.ticking or props.Ticking or false
        	local measurement = props.measurement or props.Measurement or props.digit or props.Digit or props.calc or props.Calc or ""
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	def = math.clamp(def,min,max)
        	-- // variables
        	local slider = {}
        	-- // main
        	local sliderholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,25),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,12),
        			Position = UDim2.new(0,0,0,15),
        			Parent = sliderholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)	
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,2),
        			Position = UDim2.new(0,0,0.5,0),
        			Font = self.library.font,
        			Text = def..measurement.."/"..max..measurement,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			ZIndex = 3,
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local slide = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new((1 / color.AbsoluteSize.X) * (color.AbsoluteSize.X / (max - min) * (def - min)),0,1,0),
        			ZIndex = 2,
        			Parent = outline
        		}
        	)
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],slide)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = slide
        		}
        	)
        	--
        	local sliderbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = sliderholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = sliderholder
        		}
        	)
        	-- // slider tbl
        	slider = {
        		["library"] = self.library,
        		["outline"] = outline,
        		["sliderbutton"] = sliderbutton,
        		["title"] = title,
        		["value"] = value,
        		["slide"] = slide,
        		["color"] = color,
        		["max"] = max,
        		["min"] = min,
        		["current"] = def,
        		["measurement"] = measurement,
        		["tick"] = ticking,
        		["rounding"] = rounding,
        		["callback"] = callback
        	}
        	--
        	local function slide()
        		local size = math.clamp(plr:GetMouse().X - slider.color.AbsolutePosition.X ,0 ,slider.color.AbsoluteSize.X)
        		local result = (slider.max - slider.min) / slider.color.AbsoluteSize.X * size + slider.min
        		if slider.rounding then
        			local newres = math.floor(result)
        			value.Text = newres..slider.measurement.."/"..slider.max..slider.measurement
        			slider.current = newres
        			slider.callback(newres)
        			if slider.tick then
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * (slider.color.AbsoluteSize.X / (slider.max - slider.min) * (newres - slider.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			else
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			end
        		else
        			local newres = utility.round(result ,2)
        			value.Text = newres..slider.measurement.."/"..slider.max..slider.measurement
        			slider.current = newres
        			slider.callback(newres)
        			if slider.tick then
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * (slider.color.AbsoluteSize.X / (slider.max - slider.min) * (newres - slider.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			else
        				slider.slide:TweenSize(UDim2.new((1 / slider.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        			end
        		end
        	end
        	--
        	sliderbutton.MouseButton1Down:Connect(function()
        		slider.holding = true
        		slide()
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        		outline.BorderColor3 = self.library.theme.accent
        	end)
        	--
        	uis.InputChanged:Connect(function()
        		if slider.holding then
        			slide()
        		end
        	end)
        	--
        	uis.InputEnded:Connect(function(Input)
        		if Input.UserInputType.Name == 'MouseButton1' and slider.holding then
        			slider.holding = false
        			outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        			local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        			if find then
        				table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        			end
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = slider
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(slider, sliders)
        	return slider
        end
        --
        function sliders:set(value)
        	local size = math.clamp((self.color.AbsoluteSize.X / (self.max - self.min) * (value - self.min)) ,0 ,self.color.AbsoluteSize.X)
        	local result = value
        	if self.rounding then
        		local newres = math.floor(result)
        		self.value.Text = newres..self.measurement.."/"..self.max..self.measurement
        		self.current = newres
        		self.callback(newres)
        		if self.tick then
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * (self.color.AbsoluteSize.X / (self.max - self.min) * (newres - self.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		else
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		end
        	else
        		local newres = utility.round(result ,2)
        		self.value.Text = newres..self.measurement.."/"..self.max..self.measurement
        		self.current = newres
        		self.callback(newres)
        		if self.tick then
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * (self.color.AbsoluteSize.X / (self.max - self.min) * (newres - self.min)) ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		else
        			self.slide:TweenSize(UDim2.new((1 / self.color.AbsoluteSize.X) * size ,0 ,1 ,0) ,Enum.EasingDirection.Out ,Enum.EasingStyle.Quad ,0.15 ,true)
        		end
        	end
        end
        --
        function library:closewindows(ignore)
        	local window = self
        	--
        	for i,v in pairs(window.dropdowns) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.multiboxes) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.buttonboxs) do
        		if v ~= ignore then
        			if v.open then
        				v.optionsholder.Visible = false
        				v.indicator.Text = "-"
        				v.open = false
        			end
        		end
        	end
        	--
        	for i,v in pairs(window.colorpickers) do
        		if v ~= ignore then
        			if v.open then
        				v.cpholder.Visible = false
        				v.open = false
        			end
        		end
        	end
        end
        --
        function sections:dropdown(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local dropdown = {}
        	-- // main
        	local dropdownholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = dropdownholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = def,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = dropdownholder
        		}
        	)
        	--
        	local dropdownbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = dropdownholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = dropdownholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // dropdown tbl
        	dropdown = {
        		["library"] = self.library,
        		["optionsholder"] = optionsholder,
        		["indicator"] = indicator,
        		["options"] = options,
        		["title"] = title,
        		["value"] = value,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(dropdown.library.dropdowns,dropdown)
        	--
        	for i,v in pairs(options) do
        		local ddoptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local ddoptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = ddoptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = ddoptiontitle
        		--
        		table.insert(dropdown.titles,ddoptiontitle)
        		--
        		if v == dropdown.current then ddoptiontitle.TextColor3 = self.library.theme.accent end
        		--
        		ddoptionbutton.MouseButton1Down:Connect(function()
        			optionsholder.Visible = false
        			dropdown.open = false
        			indicator.Text = "+"
        			for z,x in pairs(dropdown.titles) do
        				if x.TextColor3 == self.library.theme.accent then
        					x.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        			end
        			dropdown.current = v
        			dropdown.value.Text = v
        			ddoptiontitle.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],ddoptiontitle)
        			dropdown.callback(v)
        		end)
        	end
        	--
        	dropdownbutton.MouseButton1Down:Connect(function()
        		dropdown.library:closewindows(dropdown)
        		for i,v in pairs(dropdown.titles) do
        			if v.Text == dropdown.current then
        				v.TextColor3 = dropdown.library.theme.accent
        			else
        				v.TextColor3 = Color3.fromRGB(255,255,255)
        			end
        		end
        		optionsholder.Visible = not dropdown.open
        		dropdown.open = not dropdown.open
        		if dropdown.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = dropdown
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(dropdown, dropdowns)
        	return dropdown
        end
        --
        function sections:buttonbox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local buttonbox = {}
        	-- // main
        	local buttonboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local buttonboxbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = buttonboxholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // buttonbox tbl
        	buttonbox = {
        		["library"] = self.library,
        		["optionsholder"] = optionsholder,
        		["indicator"] = indicator,
        		["options"] = options,
        		["title"] = title,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(buttonbox.library.buttonboxs,buttonbox)
        	--
        	for i,v in pairs(options) do
        		local bboptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local bboptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = bboptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = bboptiontitle
        		--
        		table.insert(buttonbox.titles,bboptiontitle)
        		--
        		bboptionbutton.MouseButton1Down:Connect(function()
        			optionsholder.Visible = false
        			buttonbox.open = false
        			indicator.Text = "+"
        			buttonbox.current = v
        			buttonbox.callback(v)
        		end)
        	end
        	--
        	buttonboxbutton.MouseButton1Down:Connect(function()
        		buttonbox.library:closewindows(buttonbox)
        		optionsholder.Visible = not buttonbox.open
        		buttonbox.open = not buttonbox.open
        		if buttonbox.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = buttonbox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(buttonbox, buttonboxs)
        	return buttonbox
        end
        --
        function dropdowns:set(value)
        	if value ~= nil then
        		local dropdown = self
        		if table.find(dropdown.options,value) then
        			self.current = tostring(value)
        			self.value.Text = tostring(value)
        			self.callback(tostring(value))
        			for z,x in pairs(dropdown.titles) do
        				if x.Text == value then
        					x.TextColor3 = dropdown.library.theme.accent
        				else
        					x.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        			end
        		end
        	end
        end
        --
        function sections:multibox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or {}
        	local max = props.max or props.Max or props.maximum or props.Maximum or 4
        	local options = props.options or props.Options or props.Settings or props.settings or {}
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	local defstr = ""
        	if #def > 1 then
        		for i,v in pairs(def) do
        			if i == #def then
        				defstr = defstr..v
        			else
        				defstr = defstr..v..", "
        			end
        		end
        	else
        		for i,v in pairs(def) do
        			defstr = defstr..v
        		end
        	end
        	-- // variables
        	local multibox = {}
        	-- // main
        	local multiboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = multiboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-20,1,0),
        			Position = UDim2.new(0,5,0,0),
        			Font = self.library.font,
        			Text = defstr,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local indicator = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,1,0),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = "+",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Right",
        			ClipsDescendants = true,
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = multiboxholder
        		}
        	)
        	--
        	local dropdownbutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			Parent = multiboxholder
        		}
        	)
        	--
        	local optionsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,34),
        			Visible = false,
        			Parent = multiboxholder
        		}
        	)
        	--
        	local size = #options
        	--
        	size = math.clamp(size,1,max)
        	--
        	local optionsoutline = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,size,2),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			CanvasSize = UDim2.new(0,0,0,18*#options),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			ZIndex = 5,
        			Parent = optionsholder
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Parent = optionsoutline
        		}
        	)
        	-- // dropdown tbl
        	multibox = {
        		["library"] = self.library,
        		["indicator"] = indicator,
        		["optionsholder"] = optionsholder,
        		["options"] = options,
        		["value"] = value,
        		["open"] = false,
        		["titles"] = {},
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	table.insert(multibox.library.multiboxes,multibox)
        	--
        	for i,v in pairs(options) do
        		local ddoptionbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Text = "",
        				ZIndex = 6,
        				Parent = optionsoutline
        			}
        		)
        		--
        		local ddoptiontitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,
        				Text = v,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				ClipsDescendants = true,
        				ZIndex = 6,
        				Parent = ddoptionbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = ddoptiontitle
        		--
        		table.insert(multibox.titles,ddoptiontitle)
        		--
        		for c,b in pairs(def) do if v == b then ddoptiontitle.TextColor3 = self.library.theme.accent end end
        		--
        		ddoptionbutton.MouseButton1Down:Connect(function()
        			local find = table.find(multibox.current,v)
        			if find == nil then
        				table.insert(multibox.current,v)
        				local str = ""
        				if #multibox.current > 1 then
        					for i,v in pairs(multibox.current) do
        						if i == #multibox.current then
        							str = str..v
        						else
        							str = str..v..", "
        						end
        					end
        				else
        					for i,v in pairs(multibox.current) do
        						str = str..v
        					end
        				end
        				value.Text = str
        				ddoptiontitle.TextColor3 = self.library.theme.accent
        				table.insert(self.library.themeitems["accent"]["TextColor3"],ddoptiontitle)
        				multibox.callback(multibox.current)
        			else
        				table.remove(multibox.current,find)
        				local str = ""
        				if #multibox.current > 1 then
        					for i,v in pairs(multibox.current) do
        						if i == #multibox.current then
        							str = str..v
        						else
        							str = str..v..", "
        						end
        					end
        				else
        					for i,v in pairs(multibox.current) do
        						str = str..v
        					end
        				end
        				value.Text = str
        				ddoptiontitle.TextColor3 = Color3.fromRGB(255,255,255)
        				multibox.callback(multibox.current)
        			end
        		end)
        	end
        	--
        	dropdownbutton.MouseButton1Down:Connect(function()
        		multibox.library:closewindows(multibox)
        		for i,v in pairs(multibox.titles) do
        			if v.TextColor3 ~= Color3.fromRGB(255,255,255) then
        				v.TextColor3 = self.library.theme.accent
        			end
        		end
        		optionsholder.Visible = not multibox.open
        		multibox.open = not multibox.open
        		if multibox.open then
        			indicator.Text = "-"
        		else
        			indicator.Text = "+"
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = multibox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = value
        	self.library.labels[#self.library.labels+1] = title
        	-- // metatable indexing + return
        	setmetatable(multibox, multiboxs)
        	return multibox
        end
        --
        function buttonboxs:set(value)
        	if value ~= nil then
        		local dropdown = self
        		if table.find(dropdown.options,value) then
        			self.current = tostring(value)
        			self.callback(tostring(value))
        		end
        	end
        end
        --
        function multiboxs:set(tbl)
        	if tbl then
        		local multibox = self
        		if typeof(tbl) == "table" then
        			multibox.current = {}
        			for i,v in pairs(tbl) do
        				if table.find(multibox.options,v) then
        					table.insert(multibox.current,v)
        				end
        			end
        			--
        			for i,v in pairs(multibox.titles) do
        				if v.TextColor3 == multibox.library.theme.accent then
        					v.TextColor3 = Color3.fromRGB(255,255,255)
        				end
        				if table.find(tbl,v.Text) then
        					v.TextColor3 = multibox.library.theme.accent
        				end
        			end
        			--
        			local str = ""
        			if #multibox.current > 1 then
        				for i,v in pairs(multibox.current) do
        					if i == #multibox.current then
        						str = str..v
        					else
        						str = str..v..", "
        					end
        				end
        			else
        				for i,v in pairs(multibox.current) do
        					str = str..v
        				end
        			end
        			--
        			multibox.value.Text = str
        		end
        	end
        end
        --
        function sections:textbox(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or ""
        	local placeholder = props.placeholder or props.Placeholder or props.placeHolder or props.PlaceHolder or props.placeholdertext or props.PlaceHolderText or props.PlaceHoldertext or props.placeHolderText or props.placeHoldertext or props.Placeholdertext or props.PlaceholderText or props.placeholderText or ""
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	-- // variables
        	local textbox = {}
        	-- // main
        	local textboxholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,35),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,20),
        			Position = UDim2.new(0,0,0,15),
        			Parent = textboxholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	local gradient = utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = textboxholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = textboxholder
        		}
        	)
        	--
        	local tbox = utility.new(
        		"TextBox",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,15),
        			PlaceholderText = placeholder,
        			Text = def,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextTruncate = "AtEnd",
        			Font = self.library.font,
        			Parent = textboxholder
        		}
        	)
        	-- // textbox tbl
        	textbox = {
        		["library"] = self.library,
        		["tbox"] = tbox,
        		["current"] = def,
        		["callback"] = callback
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		tbox:CaptureFocus()
        	end)
        	--
        	tbox.Focused:Connect(function()
        		outline.BorderColor3 = self.library.theme.accent
        		table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        	end)
        	--
        	tbox.FocusLost:Connect(function(enterPressed)
        		textbox.current = tbox.Text
        		callback(tbox.Text)
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = textbox
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = tbox
        	-- // metatable indexing + return
        	setmetatable(textbox, textboxs)
        	return textbox
        end
        --
        function textboxs:set(value)
        	self.tbox.Text = value
        	self.current = value
        	self.callback(value)
        end
        --
        function sections:keybind(props)
        	-- // properties
        	local name = props.name or props.Name or props.page or props.Page or props.pagename or props.Pagename or props.PageName or props.pageName or "new ui"
        	local def = props.def or props.Def or props.default or props.Default or nil
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	local allowed = props.allowed or props.Allowed or 1
        	--
        	local default = ".."
        	local typeis = nil
        	--
        	if typeof(def) == "EnumItem" then
        		if def == Enum.UserInputType.MouseButton1 then
        			if allowed == 1 then
        				default = "MB1"
        				typeis = "UserInputType"
        			end
        		elseif def == Enum.UserInputType.MouseButton2 then
        			if allowed == 1 then
        				default = "MB2"
        				typeis = "UserInputType"
        			end
        		elseif def == Enum.UserInputType.MouseButton3 then
        			if allowed == 1 then
        				default = "MB3"
        				typeis = "UserInputType"
        			end
        		else
        			local capd = utility.capatalize(def.Name)
        			if #capd > 1 then
        				default = capd
        			else
        				default = def.Name
        			end
        			typeis = "KeyCode"
        		end
        	end
        	-- // variables
        	local keybind = {}
        	-- // main
        	local keybindholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,17),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,40,1,0),
        			Position = UDim2.new(1,0,0,0),
        			Parent = keybindholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline
        		}
        	)
        	--
        	local value = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = default,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = color
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = keybindholder
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = keybindholder
        		}
        	)
        	-- // keybind tbl
        	keybind = {
        		["library"] = self.library,
        		["down"] = false,
        		["outline"] = outline,
        		["value"] = value,
        		["allowed"] = allowed,
        		["current"] = {typeis,utility.splitenum(def)},
        		["pressed"] = false,
        		["callback"] = callback
        	}
        	--
        	button.MouseButton1Down:Connect(function()
        		if keybind.down == false then
        			outline.BorderColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["BorderColor3"],outline)
        			wait()
        			keybind.down = true
        		end
        	end)
        	--
        	button.MouseButton2Down:Connect(function()
        		keybind.down = false
        		keybind.current = {nil,nil}
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        		value.Text = ".."
        		outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        	end)
        	--
        	local function turn(typeis,current)
        		outline.Size = UDim2.new(0,value.TextBounds.X+20,1,0)
        		keybind.down = false
        		keybind.current = {typeis,utility.splitenum(current)}
        		outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        		local find = table.find(self.library.themeitems["accent"]["BorderColor3"],outline)
        		if find then
        			table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        		end
        	end
        	--
        	uis.InputBegan:Connect(function(Input)
        		if keybind.down then
        			if Input.UserInputType == Enum.UserInputType.Keyboard then
        				local capd = utility.capatalize(Input.KeyCode.Name)
        				if #capd > 1 then
        					value.Text = capd
        				else
        					value.Text = Input.KeyCode.Name
        				end
        				turn("KeyCode",Input.KeyCode)
        				callback(Input.KeyCode)
        			end
        			if allowed == 1 then
        				if Input.UserInputType == Enum.UserInputType.MouseButton1 then
        					value.Text = "MB1"
        					turn("UserInputType",Input)
        					callback(Input)
        				elseif Input.UserInputType == Enum.UserInputType.MouseButton2 then
        					value.Text = "MB2"
        					turn("UserInputType",Input)
        					callback(Input)
        				elseif Input.UserInputType == Enum.UserInputType.MouseButton3 then
        					value.Text = "MB3"
        					turn("UserInputType",Input)
        					callback(Input)
        				end
        			end
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = keybind
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = value
        	-- // metatable indexing + return
        	setmetatable(keybind, keybinds)
        	return keybind
        end
        --
        function keybinds:set(key)
        	if key then
        		if typeof(key) == "EnumItem" or typeof(key) == "table" then
        			if typeof(key) == "table" then
        				if key[1] and key[2] then
        					key = Enum[key[1]][key[2]]
        				else
        					return
        				end
        			end
        			local keybind = self
        			local typeis = ""
        			--
        			local default = ".."
        			--
        			if key == Enum.UserInputType.MouseButton1 then
        				if keybind.allowed == 1 then
        					default = "MB1"
        					typeis = "UserInputType"
        				end
        			elseif key == Enum.UserInputType.MouseButton2 then
        				if keybind.allowed == 1 then
        					default = "MB2"
        					typeis = "UserInputType"
        				end
        			elseif key == Enum.UserInputType.MouseButton3 then
        				if keybind.allowed == 1 then
        					default = "MB3"
        					typeis = "UserInputType"
        				end
        			else
        				local capd = utility.capatalize(key.Name)
        				if #capd > 1 then
        					default = capd
        				else
        					default = key.Name
        				end
        				typeis = "KeyCode"
        			end
        			--
        			keybind.value.Text = default
        			keybind.current = {typeis,utility.splitenum(key)}
        			keybind.callback(keybind.current)
        			keybind.outline.Size = UDim2.new(0,keybind.value.TextBounds.X+20,1,0)
        			--
        			if keybind.down then
        				keybind.down = false
        				keybind.outline.BorderColor3 = Color3.fromRGB(12, 12, 12)
        				local find = table.find(self.library.themeitems["accent"]["BorderColor3"],keybind.outline)
        				if find then
        					table.remove(self.library.themeitems["accent"]["BorderColor3"],find)
        				end
        			end
        		end
        	end
        end
        --
        function sections:colorpicker(props)
        	-- // properties
        	local name = props.name or props.Name or "new colorpicker"
        	local cpname = props.cpname or props.Cpname or props.CPname or props.CPName or props.cPname or props.cpName or props.colorpickername or nil
        	local def = props.def or props.Def or props.default or props.Default or Color3.fromRGB(255,255,255)
        	local callback = props.callback or props.callBack or props.CallBack or props.Callback or function()end
        	--
        	local h,s,v = def:ToHSV()
        	-- // variables
        	local colorpicker = {}
        	-- // main
        	local colorpickerholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			ZIndex = 2,
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,30,1,0),
        			Position = UDim2.new(1,0,0,0),
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local cpcolor = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = def,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline2
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        			Rotation = 90,
        			Parent = cpcolor
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Font = self.library.font,
        			Text = name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local button = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local cpholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,0,230),
        			Position = UDim2.new(0,0,1,5),
        			Visible = false,
        			ZIndex = 5,
        			Parent = colorpickerholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = cpholder
        		}
        	)
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,-2,0,1),
        			Position = UDim2.new(0.5,0,0,0),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local cptitle = utility.new(
        		"TextLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,-10,0,20),
        			Position = UDim2.new(0.5,0,0,0),
        			Font = self.library.font,
        			Text = cpname or name,
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Left",
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local cpholder2 = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0.875,0,0,150),
        			Position = UDim2.new(0,5,0,20),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local outline3 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromHSV(h,1,1),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = cpholder2
        		}
        	)
        	--
        	local cpimage = utility.new(
        		"ImageButton",
        		{
        			AutoButtonColor = false,
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Image = "rbxassetid://7074305282",
        			Parent = outline3
        		}
        	)
        	--
        	local cpcursor = utility.new(
        		"ImageLabel",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(0,6,0,6),
        			Position = UDim2.new(s,0,1-v,0),
        			ZIndex = 5,
        			Image = "rbxassetid://7074391319",
        			Parent = cpimage
        		}
        	)
        	--
        	local huepicker = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(1,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0.05,0,0,150),
        			Position = UDim2.new(1,-5,0,20),
        			ZIndex = 5,
        			Parent = outline2
        		}
        	)
        	--
        	local outline4 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(255, 255, 255),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			ZIndex = 5,
        			Parent = huepicker
        		}
        	)
        	--
        	local huebutton = utility.new(
        		"TextButton",
        		{
        			AnchorPoint = Vector2.new(0,0),
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Text = "",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			Font = self.library.font,
        			ZIndex = 5,
        			Parent = huepicker
        		}
        	)
        	--
        	utility.new(
        		"UIGradient",
        		{
        			Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(0.10, Color3.fromRGB(255, 153, 0)), ColorSequenceKeypoint.new(0.20, Color3.fromRGB(209, 255, 0)), ColorSequenceKeypoint.new(0.30, Color3.fromRGB(55, 255, 0)), ColorSequenceKeypoint.new(0.40, Color3.fromRGB(0, 255, 102)), ColorSequenceKeypoint.new(0.50, Color3.fromRGB(0, 255, 255)), ColorSequenceKeypoint.new(0.60, Color3.fromRGB(0, 102, 255)), ColorSequenceKeypoint.new(0.70, Color3.fromRGB(51, 0, 255)), ColorSequenceKeypoint.new(0.80, Color3.fromRGB(204, 0, 255)), ColorSequenceKeypoint.new(0.90, Color3.fromRGB(255, 0, 153)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 4))},
        			Rotation = 90,
        			Parent = outline4
        		}
        	)
        	--
        	local huecursor = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0.5),
        			BackgroundColor3 = Color3.fromRGB(255, 255, 255),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(0,12,0,6),
        			Position = UDim2.new(0.5,0,h,0),
        			ZIndex = 5,
        			Parent = outline4
        		}
        	)
        	--
        	local huecursor_inline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromHSV(h,1,1),
        			BorderColor3 = Color3.fromRGB(255, 255, 255),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			ZIndex = 5,
        			Parent = huecursor
        		}
        	)
        	--
        	local function textbox(parent,size,position)
        		local textbox_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				Position = position,
        				Size = size,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local outline5 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local outline6 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = outline5
        			}
        		)
        		--
        		local color2 = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = outline6
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = color2
        			}
        		)
        		--
        		local tbox = utility.new(
        			"TextBox",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				PlaceholderColor3 = Color3.fromRGB(255,255,255),
        				PlaceholderText = "",
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local tbox_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		tbox_button.MouseButton1Down:Connect(function()
        			tbox:CaptureFocus()
        		end)
        		--
        		return {textbox_holder,tbox,outline5}
        	end
        	--
        	local red = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	local green = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	green[1].AnchorPoint = Vector2.new(0.5,0)
        	green[1].Position = UDim2.new(0.5,0,0,175)
        	local blue = textbox(outline2,UDim2.new(0,62,0,20),UDim2.new(0,5,0,175))
        	blue[1].AnchorPoint = Vector2.new(1,0)
        	blue[1].Position = UDim2.new(1,-5,0,175)
        	local hex = textbox(outline2,UDim2.new(1,-10,0,20),UDim2.new(0,5,0,200))
        	hex[2].Size = UDim2.new(1,-12,1,0)
        	hex[2].TextXAlignment = "Left"
        	-- // colorpicker tbl
        	colorpicker = {
        		["library"] = self.library,
        		["cpholder"] = cpholder,
        		["cpcolor"] = cpcolor,
        		["huecursor"] = huecursor,
        		["outline3"] = outline3,
        		["huecursor_inline"] = huecursor_inline,
        		["cpcursor"] = cpcursor,
        		["current"] = def,
        		["open"] = false,
        		["cp"] = false,
        		["hue"] = false,
        		["hsv"] = {h,s,v},
        		["red"] = red[2],
        		["green"] = green[2],
        		["blue"] = blue[2],
        		["hex"] = hex[2],
        		["callback"] = callback
        	}
        	--
        	table.insert(self.library.colorpickers,colorpicker)
        	--
        	local function updateboxes()
        		colorpicker.red.PlaceholderText = "R: "..tostring(math.floor(colorpicker.current.R*255))
        		colorpicker.green.PlaceholderText = "G: "..tostring(math.floor(colorpicker.current.G*255))
        		colorpicker.blue.PlaceholderText = "B: "..tostring(math.floor(colorpicker.current.B*255))
        		colorpicker.hex.PlaceholderText = "Hex: "..utility.to_hex(colorpicker.current)
        	end
        	--
        	updateboxes()
        	--
        	local function movehue()
        		local posy = math.clamp(plr:GetMouse().Y-outline3.AbsolutePosition.Y,0,outline3.AbsoluteSize.Y)
        		local resy = (1/outline3.AbsoluteSize.Y)*posy
        		outline3.BackgroundColor3 = Color3.fromHSV(resy,1,1)
        		huecursor_inline.BackgroundColor3 = Color3.fromHSV(resy,1,1)
        		colorpicker.hsv[1] = resy
        		colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        		cpcolor.BackgroundColor3 = colorpicker.current
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        		huecursor:TweenPosition(UDim2.new(0.5,0,resy,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        	end
        	--
        	local function movecp()
        		local posx,posy = math.clamp(plr:GetMouse().X-outline3.AbsolutePosition.X,0,outline3.AbsoluteSize.X),math.clamp(plr:GetMouse().Y-outline3.AbsolutePosition.Y,0,outline3.AbsoluteSize.Y)
        		local resx,resy = (1/outline3.AbsoluteSize.X)*posx,(1/outline3.AbsoluteSize.Y)*posy
        		colorpicker.hsv[2] = resx
        		colorpicker.hsv[3] = 1-resy
        		colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        		cpcolor.BackgroundColor3 = colorpicker.current
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        		cpcursor:TweenPosition(UDim2.new(resx,0,resy,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        	end
        	--
        	button.MouseButton1Down:Connect(function()
        		self.library:closewindows(colorpicker)
        		cpholder.Visible = not colorpicker.open
        		colorpicker.open = not colorpicker.open
        	end)
        	--
        	huebutton.MouseButton1Down:Connect(function()
        		colorpicker.hue = true
        		movehue()
        	end)
        	--
        	cpimage.MouseButton1Down:Connect(function()
        		colorpicker.cp = true
        		movecp()
        	end)
        	--
        	uis.InputChanged:Connect(function()
        		if colorpicker.cp then
        			movecp()
        		end
        		if colorpicker.hue then
        			movehue()
        		end
        	end)
        	--
        	uis.InputEnded:Connect(function(Input)
        		if Input.UserInputType.Name == 'MouseButton1'  then
        			if colorpicker.cp then
        				colorpicker.cp = false
        			end
        			if colorpicker.hue then
        				colorpicker.hue = false
        			end
        		end
        	end)
        	--
        	red[2].Focused:Connect(function()
        		red[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	red[2].FocusLost:Connect(function()
        		local saved = red[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			red[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					red[2].PlaceholderText = "R: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(tonumber(saved),colorpicker.current.G*255,colorpicker.current.B*255))
        				red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			red[2].Text = ""
        			red[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	green[2].Focused:Connect(function()
        		green[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	green[2].FocusLost:Connect(function()
        		local saved = green[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			green[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					green[2].PlaceholderText = "G: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(colorpicker.current.R*255,tonumber(saved),colorpicker.current.B*255))
        				green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			green[2].Text = ""
        			green[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	blue[2].Focused:Connect(function()
        		blue[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	blue[2].FocusLost:Connect(function()
        		local saved = blue[2].Text
        		local num = tonumber(saved)
        		if num then
        			saved = tostring(math.clamp(tonumber(saved),0,255))
        			blue[2].Text = ""
        			if saved then
        				if #saved >= 1 and #saved <= 3 then
        					blue[2].PlaceholderText = "B: "..tostring(saved)
        				end
        				colorpicker:set(Color3.fromRGB(colorpicker.current.R*255,colorpicker.current.G*255,tonumber(saved)))
        				blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			else
        				blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			blue[2].Text = ""
        			blue[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	hex[2].Focused:Connect(function()
        		hex[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	hex[2].FocusLost:Connect(function()
        		local saved = hex[2].Text
        		if #saved >= 6 and #saved <= 7 then
        			local e,s = pcall(function()
        				utility.from_hex(saved)
        			end)
        			if e == true then
        				local hexcolor = utility.from_hex(saved)
        				if hexcolor then
        					colorpicker:set(hexcolor)
        					hex[2].Text = ""
        					hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        				else
        					hex[2].Text = ""
        					hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        				end
        			else
        				hex[2].Text = ""
        				hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        			end
        		else
        			hex[2].Text = ""
        			hex[3].BorderColor3 = Color3.fromRGB(12,12,12)
        		end
        	end)
        	--
        	local pointer = props.pointer or props.Pointer or props.pointername or props.Pointername or props.PointerName or props.pointerName or nil
        	--
        	if pointer then
        		if self.pointers then
        			self.pointers[tostring(pointer)] = colorpicker
        		end
        	end
        	--
        	self.library.labels[#self.library.labels+1] = title
        	self.library.labels[#self.library.labels+1] = hex[2]
        	self.library.labels[#self.library.labels+1] = red[2]
        	self.library.labels[#self.library.labels+1] = green[2]
        	self.library.labels[#self.library.labels+1] = blue[2]
        	self.library.labels[#self.library.labels+1] = cptitle
        	-- // metatable indexing + return
        	setmetatable(colorpicker, colorpickers)
        	return colorpicker
        end
        --
        function colorpickers:set(color)
        	if color then
        		if typeof(color) == "table" then
        			color = Color3.fromRGB(color[1]*255,color[2]*255,color[3]*255)
        		end
        		local colorpicker = self
        		local h,s,v = color:ToHSV()
        		--
        		local function updateboxes()
        			colorpicker.red.PlaceholderText = "R: "..tostring(math.floor(colorpicker.current.R*255))
        			colorpicker.green.PlaceholderText = "G: "..tostring(math.floor(colorpicker.current.G*255))
        			colorpicker.blue.PlaceholderText = "B: "..tostring(math.floor(colorpicker.current.B*255))
        			colorpicker.hex.PlaceholderText = "Hex: "..utility.to_hex(colorpicker.current)
        		end
        		--
        		local function movehue()
        			colorpicker.outline3.BackgroundColor3 = Color3.fromHSV(h,1,1)
        			colorpicker.huecursor_inline.BackgroundColor3 = Color3.fromHSV(h,1,1)
        			colorpicker.hsv[1] = h
        			colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        			colorpicker.cpcolor.BackgroundColor3 = colorpicker.current
        			colorpicker.huecursor:TweenPosition(UDim2.new(0.5,0,h,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        		end
        		--
        		local function movecp()
        			colorpicker.hsv[2] = s
        			colorpicker.hsv[3] = v
        			colorpicker.current = Color3.fromHSV(colorpicker.hsv[1],colorpicker.hsv[2],colorpicker.hsv[3])
        			colorpicker.cpcolor.BackgroundColor3 = colorpicker.current
        			colorpicker.cpcursor:TweenPosition(UDim2.new(s,0,1-v,0),Enum.EasingDirection.Out,Enum.EasingStyle.Quad,0.15,true)
        		end
        		--
        		movehue()
        		movecp()
        		updateboxes()
        		colorpicker.callback(colorpicker.current)
        	end
        end
        --
        function sections:configloader(props)
        	-- // properties
        	local folder = props.folder or props.Folder
        	-- // variables
        	local configloader = {}
        	-- // main
        	local clholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,222),
        			Parent = self.content
        		}
        	)
        	--
        	local outline = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = clholder
        		}
        	)
        	--
        	local outline2 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Parent = outline
        		}
        	)
        	--
        	local title = utility.new(
        		"TextLabel",
        		{
        			BackgroundTransparency = 1,
        			Size = UDim2.new(1,0,0,15),
        			Position = UDim2.new(0,0,0,3),
        			Font = self.library.font,
        			Text = "configs",
        			TextColor3 = Color3.fromRGB(255,255,255),
        			TextSize = self.library.textsize,
        			TextStrokeTransparency = 0,
        			TextXAlignment = "Center",
        			Parent = outline
        		}
        	)
        	--
        	self.library.labels[#self.library.labels+1] = title
        	--
        	local color = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = self.library.theme.accent,
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-6,0,1),
        			Position = UDim2.new(0.5,0,0,19),
        			Parent = outline
        		}
        	)
        	--
        	table.insert(self.library.themeitems["accent"]["BackgroundColor3"],color)
        	--
        	local buttonsholder = utility.new(
        		"Frame",
        		{
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,0,64),
        			Position = UDim2.new(0,0,0,150),
        			Parent = outline
        		}
        	)
        	--
        	local configsholder = utility.new(
        		"Frame",
        		{
        			AnchorPoint = Vector2.new(0.5,0),
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(12, 12, 12),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,-10,0,120),
        			Position = UDim2.new(0.5,0,0,25),
        			Parent = outline
        		}
        	)
        	--
        	local outline3 = utility.new(
        		"Frame",
        		{
        			BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        			BorderColor3 = Color3.fromRGB(56, 56, 56),
        			BorderMode = "Inset",
        			BorderSizePixel = 1,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			Parent = configsholder
        		}
        	)
        	--
        	local outline4 = utility.new(
        		"ScrollingFrame",
        		{
        			BackgroundColor3 = Color3.fromRGB(56, 56, 56),
        			BackgroundTransparency = 1,
        			BorderSizePixel = 0,
        			Size = UDim2.new(1,0,1,0),
        			Position = UDim2.new(0,0,0,0),
        			ClipsDescendants = true,
        			AutomaticCanvasSize = "Y",
        			CanvasSize = UDim2.new(0,0,0,0),
        			ScrollBarImageTransparency = 0.25,
        			ScrollBarImageColor3 = Color3.fromRGB(0,0,0),
        			ScrollBarThickness = 5,
        			VerticalScrollBarInset = "ScrollBar",
        			VerticalScrollBarPosition = "Right",
        			Parent = outline3
        		}
        	)
        	--
        	utility.new(
        		"UIListLayout",
        		{
        			FillDirection = "Vertical",
        			Padding = UDim.new(0,0),
        			Parent = outline4
        		}
        	)
        	--
        	local createdbuttons = {}
        	local selected
        	--
        	local makebutton = function(name,toggled)
        		local createdbutton = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,0,18),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				Parent = outline4
        			}
        		)
        		--
        		local grey = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundColor3 = Color3.fromRGB(125, 125, 125),
        				BackgroundTransparency = 0.9,
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,-4,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Visible = false,
        				Parent = createdbutton
        			}
        		)
        		--
        		local createdtitle = utility.new(
        			"TextLabel",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,-10,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				Font = self.library.font,	
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				TextXAlignment = "Left",
        				Parent = createdbutton
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = createdtitle
        		--
        		local createdb = {
        			["button"] = createdbutton,
        			["grey"] = grey,
        			["title"] = createdtitle,
        			["name"] = name
        		}
        		--
        		table.insert(createdbuttons,createdb)
        		--
        		if toggled then
        			createdb.grey.Visible = true
        			createdb.title.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],createdb.title)
        			selected = createdb
        		end
        		--
        		createdbutton.MouseButton1Down:Connect(function()
        			for i,v in pairs(createdbuttons) do
        				if v ~= createdb then
        					v.grey.Visible = false
        					v.title.TextColor3 = Color3.fromRGB(255,255,255)
        					local find = table.find(self.library.themeitems["accent"]["TextColor3"],v.title)
        					if find then
        						table.remove(self.library.themeitems["accent"]["TextColor3"],find)
        					end
        				end
        			end
        			--
        			createdb.grey.Visible = true
        			createdb.title.TextColor3 = self.library.theme.accent
        			table.insert(self.library.themeitems["accent"]["TextColor3"],createdb.title)
        			selected = createdb
        		end)
        	end
        	--
        	local newbutton = function(parent,name)
        		local button_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local button_outline = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = button_holder
        			}
        		)
        		--
        		local button_outline2 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = button_outline
        			}
        		)
        		--
        		local button_color = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = button_outline2
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = button_color
        			}
        		)
        		--
        		local button_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = name,
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = button_holder
        			}
        		)
        		--
        		self.library.labels[#self.library.labels+1] = button_button
        		--
        		return {button_holder,button_outline,button_button}
        	end
        	--
        	local function textbox(parent)
        		local textbox_holder = utility.new(
        			"Frame",
        			{
        				BackgroundTransparency = 1,
        				BorderSizePixel = 0,
        				ZIndex = 5,
        				Parent = parent
        			}
        		)
        		--
        		local outline5 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(12, 12, 12),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local outline6 = utility.new(
        			"Frame",
        			{
        				BackgroundColor3 = Color3.fromRGB(24, 24, 24),
        				BorderColor3 = Color3.fromRGB(56, 56, 56),
        				BorderMode = "Inset",
        				BorderSizePixel = 1,
        				Position = UDim2.new(0,0,0,0),
        				Size = UDim2.new(1,0,1,0),
        				ZIndex = 5,
        				Parent = outline5
        			}
        		)
        		--
        		local color2 = utility.new(
        			"Frame",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundColor3 = Color3.fromRGB(30, 30, 30),
        				BorderSizePixel = 0,
        				Size = UDim2.new(1,0,0,0),
        				Position = UDim2.new(0,0,0,0),
        				ZIndex = 5,
        				Parent = outline6
        			}
        		)
        		--
        		utility.new(
        			"UIGradient",
        			{
        				Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(199, 191, 204)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))},
        				Rotation = 90,
        				Parent = color2
        			}
        		)
        		--
        		local tbox = utility.new(
        			"TextBox",
        			{
        				AnchorPoint = Vector2.new(0.5,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0.5,0,0,0),
        				PlaceholderColor3 = Color3.fromRGB(178, 178, 178),
        				PlaceholderText = "",
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		local tbox_button = utility.new(
        			"TextButton",
        			{
        				AnchorPoint = Vector2.new(0,0),
        				BackgroundTransparency = 1,
        				Size = UDim2.new(1,0,1,0),
        				Position = UDim2.new(0,0,0,0),
        				Text = "",
        				TextColor3 = Color3.fromRGB(255,255,255),
        				TextSize = self.library.textsize,
        				TextStrokeTransparency = 0,
        				Font = self.library.font,
        				ZIndex = 5,
        				Parent = textbox_holder
        			}
        		)
        		--
        		tbox_button.MouseButton1Down:Connect(function()
        			tbox:CaptureFocus()
        		end)
        		--
        		return {textbox_holder,tbox,outline5}
        	end
        	--
        	local refresh = function()
        		for i,v in pairs(createdbuttons) do
        			v.button:Remove()
        			v.grey:Remove()
        			v.title:Remove()
        		end
        		createdbuttons = {}
        		for i,v in pairs(listfiles(folder)) do
        			if v:sub(-4) == ".cfg" then
        				if i == 1 then 
        					makebutton(v:sub(#tostring(folder)+2, -5),true)
        				else
        					makebutton(v:sub(#tostring(folder)+2, -5),false)
        				end
        			end
        		end
        	end
        	--
        	refresh()
        	--
        	local name = textbox(buttonsholder)
        	local load = newbutton(buttonsholder,"Load")
        	local delete = newbutton(buttonsholder,"Delete")
        	local save = newbutton(buttonsholder,"Save")
        	local create = newbutton(buttonsholder,"Create")
        	--
        	name[1].Size = UDim2.new(1,-10,0,20)
        	load[1].Size = UDim2.new(0.5,-6,0,20)
        	delete[1].Size = UDim2.new(0.5,-6,0,20)
        	save[1].Size = UDim2.new(0.5,-6,0,20)
        	create[1].Size = UDim2.new(0.5,-6,0,20)
        	--
        	name[1].Position = UDim2.new(0.5,0,0,0)
        	name[1].AnchorPoint = Vector2.new(0.5,0)
        	--
        	load[1].Position = UDim2.new(0,5,0,22)
        	load[1].AnchorPoint = Vector2.new(0,0)
        	--
        	delete[1].Position = UDim2.new(1,-5,0,22)
        	delete[1].AnchorPoint = Vector2.new(1,0)
        	--
        	save[1].Position = UDim2.new(0,5,0,44)
        	save[1].AnchorPoint = Vector2.new(0,0)
        	--
        	create[1].Position = UDim2.new(1,-5,0,44)
        	create[1].AnchorPoint = Vector2.new(1,0)
        	--
        	name[2].PlaceholderText = "Name"
        	--
        	local currentname = nil
        	--
        	name[2].Focused:Connect(function()
        		name[3].BorderColor3 = self.library.theme.accent
        	end)
        	--
        	name[2].FocusLost:Connect(function()
        		local saved = name[2].Text
        		if #saved >= 3 and #saved <= 15 then
        			currentname = saved
        		else
        			name[2].Text = ""
        			currentname = nil
        		end
        		name[3].BorderColor3 = Color3.fromRGB(12,12,12)
        	end)
        	--
        	load[3].MouseButton1Down:Connect(function()
        		self.library:loadconfig(folder..selected.name..".cfg")
        		load[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		load[2].BorderColor3 = Color3.fromRGB(12,12,12)
        	end)
        	--
        	delete[3].MouseButton1Down:Connect(function()
        		delfile(folder..selected.name..".cfg")
        		delete[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		delete[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	--
        	save[3].MouseButton1Down:Connect(function()
        		writefile(folder..selected.name..".cfg", self.library:saveconfig())
        		save[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		save[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	--
        	create[3].MouseButton1Down:Connect(function()
        		writefile(folder..currentname..".cfg", self.library:saveconfig())
        		create[2].BorderColor3 = self.library.theme.accent
        		wait(0.05)
        		create[2].BorderColor3 = Color3.fromRGB(12,12,12)
        		wait()
        		refresh()
        	end)
        	-- // button tbl
        	configloader = {
        		["library"] = self.library
        	}
        	-- // metatable indexing + return
        	setmetatable(configloader, configloaders)
        	return configloader 
        end
        
        
        local window = library:new({textsize = 13.5,font = Enum.Font.RobotoMono,name = "Winnable Hub / Project New World",color = Color3.fromRGB(255,135,0)})
        
        local Main_1_Page = window:page({name = "Main"})
        
        local farm = Main_1_Page:section({name = "Auto Farm",side = "left",size = 250})
        
        local stat = Main_1_Page:section({name = "Stats",side = "right",size = 250})
        
        farm:toggle({name = "Auto Farm Level",def = false,callback = function(vu)
            _G.Auto_Farm = vu
            tween_cancel()
        end})
        
        farm:toggle({name = "Auto Chest",def = false,callback = function(vu)
            _G.Auto_Chest = vu
            tween_cancel()
        end})
        
        Weapon = {
            "Melee",
            "Sword",
            "Devil Fruit"
        }
        
        farm:dropdown({name = "Please Select Your Weapon",def = "-->",max = 10,options = Weapon,callback = function(vu)
           _G.typeofweapon = vu
        end})
        
        stat:toggle({name = "Auto Melee",def = false,callback = function(vu)
            _G.Auto_Melee = vu
        end})
        
        stat:toggle({name = "Auto Defense",def = false,callback = function(vu)
            _G.Auto_Defense = vu
        end})
        
        stat:toggle({name = "Auto Sword",def = false,callback = function(vu)
            _G.Auto_Sword = vu
        end})
        
        stat:toggle({name = "Auto Fruit",def = false,callback = function(vu)
            _G.Auto_Fruit = vu
        end})
        
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Melee then
        local args = {
            [1] = "Combat",
            [2] = 1
        }
        
        game:GetService("ReplicatedStorage").Replication.ClientEvents.Stats_Event:FireServer(unpack(args))
        
                end
        end)
        end
        end)
        
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Defense then
        local args = {
            [1] = "Defense",
            [2] = 1
        }
        
        game:GetService("ReplicatedStorage").Replication.ClientEvents.Stats_Event:FireServer(unpack(args))
        
                end
        end)
        end
        end)
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Fruit then
        local args = {
            [1] = "Fruit",
            [2] = 1
        }
        
        game:GetService("ReplicatedStorage").Replication.ClientEvents.Stats_Event:FireServer(unpack(args))
        
        
                end
        end)
        end
        end)
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Sword then
        local args = {
            [1] = "Sword",
            [2] = 1
        }
        
        game:GetService("ReplicatedStorage").Replication.ClientEvents.Stats_Event:FireServer(unpack(args))
        
        
                end
        end)
        end
        end)
        
        
                function tween_cancel()
            local Distance2 = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                        local tween_s = game:service"TweenService"
                        local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
                        local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame})
                        tween:Play()
        end
        
        spawn(function()
            while task.wait(1) do
                pcall(function()
                    if _G.Auto_Farm then
                    for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        for i,v2 in pairs(v:GetChildren()) do
        if _G.typeofweapon == "Melee" then
            if v2.Name == "CoolDown" then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name))
            end
        end
        if _G.typeofweapon == "Sword" then
            if v2.Name == "SlashCD" then
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name))
            end
        end
        end
        end
        end
        end)
        end
        end)
        
        
        spawn(function()
            while task.wait(3) do
                pcall(function()
                    if _G.Auto_Farm then
                        checklevel()
        local args = {
            [1] = Zone
        }
        
        game:GetService("ReplicatedStorage").Replication.ClientEvents.SetSpawnPoint:FireServer(unpack(args))
        
                    end
                end)
            end
        end)
        
        spawn(function()
            while task.wait(.6) do
                pcall(function()
                    if _G.Auto_Farm then
                    game:GetService'VirtualUser':CaptureController()
                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672)) 
        end
        end)
        end
        end)
        
        spawn(function()
            game:GetService("RunService").Stepped:Connect(function()
                pcall(function()
                    if _G.Auto_Farm then
                        checklevel()
                        if game.Players.LocalPlayer.PlayerGui.QuestGui.Enabled == false and game.Players.LocalPlayer.Character.Humanoid.Health >= 1 then
            local Distance2 = (game:GetService("Workspace").LOL.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/600, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game:GetService("Workspace").LOL.CFrame * CFrame.new(0,0,0)})
            tween:Play()
        wait(.3)
        
        local args = {
            [1] = workspace.Npc_Workspace.QuestGivers:FindFirstChild(Quest1):FindFirstChild(Quest2),
            [2] = Quest3
        }
        
        game:GetService("Players").LocalPlayer.PlayerGui.QuestGui.QuestFunction:InvokeServer(unpack(args))
        
        
        elseif game.Players.LocalPlayer.PlayerGui.QuestGui.Enabled == true and game.Players.LocalPlayer.Character.Humanoid.Health >= 1 then
        for i,v in pairs(game:GetService("Workspace")["NPC Zones"][Zone].NPCS:GetChildren()) do
            if string.find(v.Name, Mon) then
            local Distance2 = (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/600, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,5.5,0) * CFrame.Angles(math.rad(-90),0,0)})
            tween:Play()
        end
        end
                        end
                end
                end)
            end)
        end)
        
        
        spawn(function()
            game:GetService("RunService").Stepped:Connect(function()
                pcall(function()
                    if _G.Auto_Farm then
                        checklevel()
        if not game:GetService("Workspace")["NPC Zones"]:FindFirstChild(Zone) then
            local Distance2 = (game:GetService("Workspace").LOL.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/600, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = game:GetService("Workspace").LOL.CFrame * CFrame.new(0,0,0)})
            tween:Play()
        end
                end
                end)
            end)
        end)
        
                    spawn(function()
                        game:GetService("RunService").Heartbeat:Connect(function()
                            if _G.Auto_Farm then
                                checklevel()
                                if not game:GetService("Workspace"):FindFirstChild("LOL") then
                                    local LOL = Instance.new("Part")
                                    LOL.Name = "LOL"
                                    LOL.Parent = game.Workspace
                                    LOL.Anchored = true
                                    LOL.Transparency = 1
                                    LOL.Size = Vector3.new(7,-0.2,7)
                                    LOL.Material = "Neon"
                                elseif game:GetService("Workspace"):FindFirstChild("LOL") then
                                    game.Workspace["LOL"].CFrame = CMON
                                end
                        end
                        end)
                    end)
                    
        spawn(function()
            game:GetService("RunService").Stepped:Connect(function()
                pcall(function()
                    if _G.Auto_Chest then 
                        for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
            if v.Name == "Chest" then
            local Distance2 = (v.Hitbox.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
            local tween_s = game:service"TweenService"
            local info = TweenInfo.new(Distance2/850, Enum.EasingStyle.Linear)
            local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = v.Hitbox.CFrame * CFrame.new(0,0,0)})
            tween:Play()
            end
        end
                    end
                end)
            end)
        end)
        
        spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Auto_Chest or _G.Auto_Farm then 
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                            local Noclip = Instance.new("BodyVelocity")
                            Noclip.Name = "BodyClip"
                            Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            Noclip.MaxForce = Vector3.new(100000,100000,100000)
                            Noclip.Velocity = Vector3.new(0,0,0)
                        end
                    else
                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                    end
                end)
            end
        end)
        
        spawn(function()
            pcall(function()
                game:GetService("RunService").Stepped:Connect(function()
                    if _G.Auto_Chest or _G.Auto_Farm then
                        for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                            if v:IsA("BasePart") then
                                v.CanCollide = false    
                            end
                        end
                    end
                end)
            end)
        end)
            elseif placeId == 11427352058 then
        local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Winnable Hub / Psycho Mystery", "Synapse")
    local Tab = Window:NewTab("Main")
    local Section = Tab:NewSection("Main")
    local Tab2 = Window:NewTab("Players")
    local Section2 = Tab2:NewSection("Check People Name")
    
    Section:NewDropdown("Select Item To Pick Up", "", {"Detective's Tool", "Pistol", "Bug Repellant", "Medkit"}, function(value)
    _G.Select_Item_To_Pick_Up = value
    end)
    
    
    Section:NewButton("Auto Pick Up", "", function()
    for i,v in pairs(game:GetService("Workspace").WorldItems:GetChildren()) do
        if v.Name == _G.Select_Item_To_Pick_Up then   
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Root.CFrame
            wait(.1)
            fireproximityprompt(v.Root.ProximityPrompt,1)
        end
    end
    end)
    
    PlayersList = {}    
    
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        table.insert(PlayersList,v.Name)
    end
    
    local adropdown = Section2:NewDropdown("Please People To Check Name", "", PlayersList, function(value)
        _G.Select_Check_People = value
    end)
    
    Section2:NewButton("Refresh People", "", function()
      adropdown:Refresh(PlayersList)
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        table.insert(PlayersList,v.Name)
    end
    end)
    
    local username = Section2:NewLabel("username = ")
    
    Section2:NewButton("Check People Name", "", function()
        for i,v in pairs(game.Players:GetChildren()) do
            if v.Name == _G.Select_Check_People then
                    username:UpdateLabel(v.Name.. " = " ..game:GetService("Workspace")[v.Name].HumanoidRootPart.CharacterBill.NameLabel.Text)
            end
        end
    end)
    elseif placeId == 12017032683 then
        Lighting = game:GetService("Lighting")
    
    Food = {
        "Burger",
        "Soda",
        "Hotdog",
        "Water",
        "Donut",
        "Pizza"
    }
    
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Winnable Hub / SCP - 096", "Midnight")
    local Tab = Window:NewTab("LocalPlayer")
    local Section = Tab:NewSection("LocalPlayer")
    local Tab2 = Window:NewTab("Item")
    local Section2 = Tab2:NewSection("Food")
    local Tab3 = Window:NewTab("Player")
    local Section3 = Tab3:NewSection("Player")
    local Tab4 = Window:NewTab("Game")
    local Section4 = Tab4:NewSection("Game")
    
    Section:NewSlider("Speed", "", 500, 16, function(value)
        _G.Speedz = value
    end)
    
    Section:NewButton("Set Speed", "ButtonInfo", function()
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = _G.Speedz
    end)
    
    Section:NewSlider("Jump Power", "", 500, 50, function(value)
        _G.Jump = value
    end)
    
    Section:NewButton("Set Jump Power", "ButtonInfo", function()
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = _G.Jump
    end)
    
    Section:NewSlider("Set Fly Speed", "", 100, 1, function(value)
        _G.Speed = value
    end)
    
    Section:NewToggle("Fly", "", function(state)
    Fly = state
    activatefly()
    end)
    
    
    
    Section2:NewDropdown("Select Food To Pick Up", "", Food, function(value)
        _G.Item_Pick_Selected = value
    end)
    
    Section2:NewToggle("Pick Up", "", function(state)
    _G.Auto_Pickup = state
    end)
    
    PlayersList = {}    
    
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        table.insert(PlayersList,v.Name)
    end
    
    local adropdown = Section3:NewDropdown("Player Select", "", PlayersList, function(value)
        _G.Selected_Player = value
    end)
    
    Section3:NewButton("Refresh Player", "", function()
      adropdown:Refresh(PlayersList)
    for i,v in pairs(game:GetService("Players"):GetChildren()) do
        table.insert(PlayersList,v.Name)
    end
    end)
    
    Section3:NewButton("Teleport To Player", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[_G.Selected_Player].Character.HumanoidRootPart.CFrame
    end)
    
    Section3:NewToggle("Spectate Player", "", function(state)
     Sp = state
                                        local plr1 = game.Players.LocalPlayer.Character.Humanoid
                                        local plr2 = game.Players:FindFirstChild(_G.Selected_Player)
                                        repeat wait(.1)
                                            game.Workspace.Camera.CameraSubject = plr2.Character.Humanoid
                                        until Sp == false 
                                        game.Workspace.Camera.CameraSubject = game.Players.LocalPlayer.Character.Humanoid
    end)
    
    Section3:NewToggle("ESP Players", "", function(state)
    _G.ESP_PLAYERS = state
    end)
    
    Section4:NewToggle("ESP SCP-096", "", function(state)
    _G.ESP_SCP = state
    end)
    
    Section4:NewButton("Nofog", "ButtonInfo", function()
        	Lighting.FogEnd = 100000
    	for i,v in pairs(Lighting:GetDescendants()) do
    		if v:IsA("Atmosphere") then
    			v:Destroy()
    		end
    	end
    end)
    
    Section4:NewButton("Full Bright", "", function()
    Lighting.Brightness = 2
    	Lighting.ClockTime = 14
    	Lighting.FogEnd = 100000
    	Lighting.GlobalShadows = false
    	Lighting.OutdoorAmbient = Color3.fromRGB(128, 128, 128)
    end)
    
    spawn(function()
    while wait() do
         pcall(function()
             if _G.ESP_PLAYERS == false then
           for i,v in pairs(game.Players:GetChildren()) do
                v.Character.Head.ESP:Destroy()
            end
            end
        end) 
    end
    end)
    
    spawn(function()
    while wait() do
         pcall(function()
             if _G.ESP_PLAYERS then
           for i,v in pairs(game.Players:GetChildren()) do
                if not v.Character.Head:FindFirstChild("ESP") then
                    local BillboardGui = Instance.new("BillboardGui")
                    local TextLabel = Instance.new("TextLabel")
                    BillboardGui.Parent = v.Character.Head
                    BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                    BillboardGui.Active = true
                    BillboardGui.Name = "ESP"
                    BillboardGui.AlwaysOnTop = true
                    BillboardGui.LightInfluence = 1.000
                    BillboardGui.Size = UDim2.new(0, 200, 0, 50)
                    BillboardGui.StudsOffset = Vector3.new(0, 2.5, 0)
                    TextLabel.Parent = BillboardGui
                    TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TextLabel.BackgroundTransparency = 1.000
                    TextLabel.Size = UDim2.new(0, 200, 0, 50)
                    TextLabel.Font = Enum.Font.GothamBold
                    TextLabel.Text = v.Name
                    TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
                    TextLabel.TextScaled = true
                    TextLabel.TextSize = 14.000
                    TextLabel.TextStrokeTransparency = 0.000
                    TextLabel.TextWrapped = true
                    end
            end
            end
        end) 
    end
    end)
    
    spawn(function()
        while wait(.1) do
            pcall(function()
                if _G.Auto_Pickup then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Interact[_G.Item_Pick_Selected].Hitbox.CFrame
            
    local args = {
        [1] = workspace.Interact[_G.Item_Pick_Selected]
    }
    
    game:GetService("ReplicatedStorage").Remotes.ObjectInteract:FireServer(unpack(args))
    end
    end)
    end
    end)
    
    spawn(function()
    while wait(.1) do
         pcall(function()
             if _G.ESP_SCP == false then
    game:GetService("Workspace")["SCP-096"].Head.ESP:Destroy()
            end
        end) 
    end
    end)
    
    spawn(function()
    while wait() do
         pcall(function()
             if _G.ESP_SCP then
           for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
               if v.Name == "SCP-096" then
                if not v.Head:FindFirstChild("ESP") then
                    local BillboardGui = Instance.new("BillboardGui")
                    local TextLabel = Instance.new("TextLabel")
                    BillboardGui.Parent = v.Head
                    BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
                    BillboardGui.Active = true
                    BillboardGui.Name = "ESP"
                    BillboardGui.AlwaysOnTop = true
                    BillboardGui.LightInfluence = 1.000
                    BillboardGui.Size = UDim2.new(0, 200, 0, 50)
                    BillboardGui.StudsOffset = Vector3.new(0, 2.5, 0)
                    TextLabel.Parent = BillboardGui
                    TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TextLabel.BackgroundTransparency = 1.000
                    TextLabel.Size = UDim2.new(0, 200, 0, 50)
                    TextLabel.Font = Enum.Font.GothamBold
                    TextLabel.Text = v.Name
                    TextLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
                    TextLabel.TextScaled = true
                    TextLabel.TextSize = 14.000
                    TextLabel.TextStrokeTransparency = 0.000
                    TextLabel.TextWrapped = true
                end
               end
    end
            end
        end) 
    end
    end)
    
    Fly = false
    function activatefly()
        local mouse=game.Players.LocalPlayer:GetMouse''
        localplayer=game.Players.LocalPlayer
        game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart")
        local torso = game.Players.LocalPlayer.Character.HumanoidRootPart
        local speedSET = _G.Speed
        local keys={a=false,d=false,w=false,s=false}
        local e1
        local e2
        local function start()
            local pos = Instance.new("BodyPosition",torso)
            local gyro = Instance.new("BodyGyro",torso)
            pos.Name="EPIXPOS"
            pos.maxForce = Vector3.new(math.huge, math.huge, math.huge)
            pos.position = torso.Position
            gyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
            gyro.cframe = torso.CFrame
            repeat
                wait()
                localplayer.Character.Humanoid.PlatformStand=true
                local new=gyro.cframe - gyro.cframe.p + pos.position
                if not keys.w and not keys.s and not keys.a and not keys.d then
                    speed=1
                end
                if keys.w then
                    new = new + workspace.CurrentCamera.CoordinateFrame.lookVector * speed
                    speed=speed+speedSET
                end
                if keys.s then
                    new = new - workspace.CurrentCamera.CoordinateFrame.lookVector * speed
                    speed=speed+speedSET
                end
                if keys.d then
                    new = new * CFrame.new(speed,0,0)
                    speed=speed+speedSET
                end
                if keys.a then
                    new = new * CFrame.new(-speed,0,0)
                    speed=speed+speedSET
                end
                if speed>speedSET then
                    speed=speedSET
                end
                pos.position=new.p
                if keys.w then
                    gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(-math.rad(speed*15),0,0)
                elseif keys.s then
                    gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(math.rad(speed*15),0,0)
                else
                    gyro.cframe = workspace.CurrentCamera.CoordinateFrame
                end
            until not Fly
            if gyro then 
                gyro:Destroy() 
            end
            if pos then 
                pos:Destroy() 
            end
            flying=false
            localplayer.Character.Humanoid.PlatformStand=false
            speed=0
        end
        e1=mouse.KeyDown:connect(function(key)
            if not torso or not torso.Parent then 
                flying=false e1:disconnect() e2:disconnect() return 
            end
            if key=="w" then
                keys.w=true
            elseif key=="s" then
                keys.s=true
            elseif key=="a" then
                keys.a=true
            elseif key=="d" then
                keys.d=true
            end
        end)
        e2=mouse.KeyUp:connect(function(key)
            if key=="w" then
                keys.w=false
            elseif key=="s" then
                keys.s=false
            elseif key=="a" then
                keys.a=false
            elseif key=="d" then
                keys.d=false
            end
        end)
        start()
    end
    
    _G.Speed = 25
    
    elseif placeId == 2788229376 then
    
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Winnable Hub / DHC", "DarkTheme")
    local Tab = Window:NewTab("Funtion")
    local Section = Tab:NewSection("Function")
    Section:NewLabel("type :drop to start")
    Section:NewLabel("type _G.Name On The Script To Use")
    
    for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame["Frame_MessageLogDisplay"].Scroller:GetChildren()) do
    if v.Name == "Frame" then
        v:Destroy()
    end
    end
    
    function showimange()
        local ScreenGui = Instance.new("ScreenGui")
    local Frame = Instance.new("ImageLabel")
    local TextLabel = Instance.new("TextLabel")
    ScreenGui.Parent = game:GetService("CoreGui")
    
    TextLabel.Parent = ScreenGui
    TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 78)
    TextLabel.BackgroundTransparency = 1
    TextLabel.Position = UDim2.new(0.5, 0, 0.9, 0)
    TextLabel.Size = UDim2.new(0, 20, 0, 20)
    TextLabel.Font = Enum.Font.Gotham
    TextLabel.Text = "Script By Winnable Hub"
    TextLabel.TextColor3 = Color3.fromRGB(255, 175, 0)
    TextLabel.TextSize = 70.000
    TextLabel.TextStrokeTransparency = 0.000
    end
    
    function removeimange()
            local ScreenGui = Instance.new("ScreenGui")
    local Frame = Instance.new("ImageLabel")
    local TextLabel = Instance.new("TextLabel")
    ScreenGui.Parent = game:GetService("CoreGui")
        game.CoreGui:FindFirstChild("ScreenGui"):Destroy()
    end
    
    function startdrop()
    local a = math.random(1,12)
    if a == 1 then
        cf = CFrame.new(-869.177429, -38.3992157, -621.157837, 0.0531697273, 1.31608049e-08, -0.998585463, 6.40279696e-09, 1, 1.35203644e-08, 0.998585463, -7.1126145e-09, 0.0531697273)
    elseif a == 2 then
        cf = CFrame.new(-879.385376, -38.3992119, -625.729858, 0.255153686, 1.63641669e-08, 0.966900527, -9.17912004e-08, 1, 7.29826555e-09, -0.966900527, -9.06151385e-08, 0.255153686)
    elseif a == 3 then
        cf = CFrame.new(-894.101929, -39.3992119, -628.210205, -0.159800887, 1.64522862e-09, 0.987149239, 4.7147859e-09, 1, -9.03411124e-10, -0.987149239, 4.50983118e-09, -0.159800887)
    elseif a == 4 then
        cf = CFrame.new(-878.388733, -38.3992119, -593.938904, -0.719561934, 2.57587129e-09, -0.694428265, 3.84629795e-09, 1, -2.76167311e-10, 0.694428265, -2.86969759e-09, -0.719561934)
    elseif a == 5 then
        cf = CFrame.new(-868.955261, -38.3992081, -597.47467, 0.0115734003, -1.02213349e-08, -0.999933004, 7.32954106e-08, 1, -9.37368583e-09, 0.999933004, -7.31820151e-08, 0.0115734003)
    elseif a == 6 then
        cf = CFrame.new(-859.185669, -38.3992081, -597.144531, -0.122026466, -3.87366539e-09, -0.992526829, -9.50852197e-09, 1, -2.73380429e-09, 0.992526829, 9.10386699e-09, -0.122026466)
    elseif a == 7 then
        cf = CFrame.new(-855.461182, -38.8992119, -586.707214, -0.99999392, 7.75952191e-09, -0.00349254557, 7.75498865e-09, 1, 1.31152778e-09, 0.00349254557, 1.28443511e-09, -0.99999392)
    elseif a == 8 then
        cf = CFrame.new(-860.985779, -38.3992119, -577.634949, -0.993863165, -7.44609991e-08, 0.110616662, -7.43778088e-08, 1, 4.87844165e-09, -0.110616662, -3.37892181e-09, -0.993863165)
    elseif a == 9 then
        cf = CFrame.new(-869.362427, -38.3992119, -575.571838, -0.0106501309, 3.92342159e-09, 0.999943256, 6.53102674e-08, 1, -3.22804161e-09, -0.999943256, 6.52721894e-08, -0.0106501309)
    elseif a == 10 then
        cf = CFrame.new(-879.671204, -38.3992119, -573.767212, -0.0917523578, 4.10615497e-09, 0.995781839, 8.42019787e-08, 1, 3.63490815e-09, -0.995781839, 8.41803143e-08, -0.0917523578)
    elseif a == 11 then
        cf = CFrame.new(-892.383972, -38.8992157, -588.085083, 0.971367955, 6.40305728e-08, -0.237580135, -6.11616855e-08, 1, 1.9446377e-08, 0.237580135, -4.35878666e-09, 0.971367955)
    elseif a == 12 then
        cf = CFrame.new(-892.462769, -38.8992119, -578.909546, 0.441420555, -4.11911678e-08, 0.897300363, 1.08370358e-07, 1, -7.40636574e-09, -0.897300363, 1.00510086e-07, 0.441420555)    
    end
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = cf
    wait(2)
    _G.Drop = true
    game.RunService:Set3dRenderingEnabled(false)
    wait(.1)
    showimange()
    end
    
    spawn(function()
        while wait(1) do
            pcall(function()
                if _G.Drop then
    local args = {
        [1] = "DropMoney",
        [2] = "10000"
    }
    
    game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))
                end
    end)
    end
    end)
    
    spawn(function()
        while wait(1) do
            pcall(function()
    for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame["Frame_MessageLogDisplay"].Scroller:GetChildren()) do
    if v.Name == "Frame" then
        for i,v2 in pairs(v.TextLabel:GetChildren()) do
                   if string.find(v2.Text, _G.Name) and string.find(v2.Parent.Text, ":stop") then
                   v2.Parent:Destroy()
                   wait(1)
                   startdrop()
                   end
    end
    end
    end
    end)
    end
    end)
    spawn(function()
        while wait(1) do
            pcall(function()
    for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame["Frame_MessageLogDisplay"].Scroller:GetChildren()) do
    if v.Name == "Frame" then
        for i,v2 in pairs(v.TextLabel:GetChildren()) do
                   if string.find(v2.Text, _G.Name) and string.find(v2.Parent.Text, ":drop") then
                   v2.Parent:Destroy()
                   wait(1)
                   startdrop()
                   end
    end
    end
    end
    end)
    end
    end)
    elseif placeId == 12192552089 then
            loadstring(game:HttpGet("https://raw.githubusercontent.com/xlostpexz/fruitwarriors/Fps/Loading.lua"))()
    elseif placeId == 9380307595 then
    loadstring(game:HttpGet("https://raw.githubusercontent.com/xlostpexz/PixelPiece/Fps/Loading.lua"))()
    elseif placeId == 11943871352 then
        loadstring(game:HttpGet("https://raw.githubusercontent.com/xlostpexz/HPS/Fps/Loading.lua"))()
            else
            game.StarterGui:SetCore("SendNotification", {
                  Icon = "rbxassetid://11634040122";
                  Title = "Winnable Hub", 
                  Text = "Game Not Support"
              })
            end
            end
            
            executenow()
