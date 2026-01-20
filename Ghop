-- Freeze All con la tecla F (excepto tú)

local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")

local localPlayer = Players.LocalPlayer
local frozen = false

local function freezeAll()
	for _, player in pairs(Players:GetPlayers()) do
		if player ~= localPlayer then
			local character = player.Character
			if character and character:FindFirstChild("HumanoidRootPart") then
				character.HumanoidRootPart.Anchored = true
			end
		end
	end
end

local function unfreezeAll()
	for _, player in pairs(Players:GetPlayers()) do
		if player ~= localPlayer then
			local character = player.Character
			if character and character:FindFirstChild("HumanoidRootPart") then
				character.HumanoidRootPart.Anchored = false
			end
		end
	end
end

UserInputService.InputBegan:Connect(function(input, gameProcessed)
	if gameProcessed then return end

	if input.KeyCode == Enum.KeyCode.F then
		frozen = not frozen

		if frozen then
			freezeAll()
		else
			unfreezeAll()
		end
	end
end)
