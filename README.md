# Autofarm-RC

```
warn("Anti afk running")
game:GetService("Players").LocalPlayer.Idled:connect(function()
warn("Anti afk ran")
game:GetService("VirtualUser"):CaptureController()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Marco8642/science/main/ui%20libs2"))()
local example = library:CreateWindow({
  text = "Nigga Autofarm"
})
example:AddToggle("Auto farm", function(state)
getfenv().test = (state and true or false)
local plr = game.Players.LocalPlayer
local chr = plr.Character
local car = chr.Humanoid.SeatPart.Parent
car.PrimaryPart = car.Body["#Weight"]
local location = car.PrimaryPart.CFrame
while getfenv().test do
  task.wait()
  local plr = game.Players.LocalPlayer
  local chr = plr.Character
  local car = chr.Humanoid.SeatPart.Parent
  if not workspace:FindFirstChild("justanormalpart") then
local Block = Instance.new("Part",workspace)
Block.Name = "justanormalpart"
Block.Anchored = true
Block.Size = Vector3.new(10000,10,10000)
Block.Position = chr.HumanoidRootPart.Position+Vector3.new(0,5000,0)
  end
  car.PrimaryPart.Velocity = car.PrimaryPart.CFrame.LookVector*300
  task.wait(1.7)
  car:PivotTo(workspace:FindFirstChild("justanormalpart").CFrame+Vector3.new(0,7,0))
end
end)
