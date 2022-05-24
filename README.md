local plr = game.Players.LocalPlayer
local Character = plr.Character

while true do 
    wait(0.43)
    for i , v in pairs( game:GetService("Workspace").Trinkets:GetDescendants())do
    if v.ClassName == "ClickDetector"then
        local magnitude = (v.Parent.Position - Character.HumanoidRootPart.Position).magnitude
            local range = 20
            if magnitude < range then
                fireclickdetector(v)
            end
    end
end    
end

local the = game.Players
local one = the.LocalPlayer
local Lbozo = one.Character
local Nofal = Lbozo.CharacterHandler
if Nofal.Remotes:FindFirstChild("ApplyFallDamage") then
   Nofal.Remotes.ApplyFallDamage:Destroy()
end
