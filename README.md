--- Roblox Square body script ---

(Usage notes at the end)

game.Players.PlayerAdded:Connect(function(player)
	while true do
		wait()
		local char = player.Character or player.CharacterAdded:Wait()

		if char then
			for c, charmesh in pairs(char:GetChildren()) do
				if charmesh:IsA("CharacterMesh") then
					charmesh:Destroy() 
				end
			end
		end
	end
end)

Usage notes:

- Make sure the game is on R6 (Game Setings> Avatar)
- The script must be placed in "ServerScriptService"
- It is a Script and not LocalScript.


