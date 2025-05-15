<pre style="caret-color: rgb(0, 0, 0); color: rgb(0, 0, 0); font-style: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: auto; word-spacing: 0px; -webkit-tap-highlight-color: rgba(26, 26, 26, 0.3); -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; text-decoration: none; overflow-wrap: break-word; white-space: pre-wrap;">--those script are broken dont read (no its not)

local ws = cloneref(game:GetService("Workspace"))

if ws:FindFirstChild("Gayze") then
cloneref(game:GetService("StarterGui")):SetCore("SendNotification", {
    Title = "Notification";
    Text = "Script alr executed";
    Duration = 5;
})
return end

local part = Instance.new("Part")
part.Parent = ws
part.Name = "Gayze"
part.Size = Vector3.new(5, 5, 5)
part.Position = Vector3.new(0, 5, 0)
part.Transparency = 1
part.CanCollide = false
part.Anchored = true

_G.CannonFound = false


function Load(url)
    coroutine.wrap(function()
        local success, scriptFunction = pcall(function()
            return loadstring(game:HttpGet(url, true))
        end)

        if success and scriptFunction then
            coroutine.wrap(scriptFunction)() 
        else
            warn("Failed to load script:", scriptFunction)
        end
    end)()
end




Load("https://raw.githubusercontent.com/Gazer-Ha/Gaze-stuff/refs/heads/main/Get%20cannon")
while not _G.CannonFound do
    task.wait()
end
Load("https://raw.githubusercontent.com/jolgue02928/Bounds-2/refs/heads/main/README.md")</pre>
