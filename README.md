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

Images:

 - ![image](https://user-images.githubusercontent.com/82664951/115093275-2aa92580-9ef0-11eb-93fa-b2d7d50fc0eb.png) -- Script.
- ![image](https://user-images.githubusercontent.com/82664951/115093289-3268ca00-9ef0-11eb-8493-00ce41ecc678.png) -- Script localization.



