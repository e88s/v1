local http = (syn and syn.request) or (http_request) or (request)

local webhookUrl = "https://discord.com/api/webhooks/1401551309043400734/uB4VFn7iHjMkFyuPDE_QuDXkjQHkc5v0thRb-9NyuN158JceEAg4piVfiBBdv_XVic1v"


local data = {
    ["username"] = "Roblox Executor Bot",
    ["content"] = "Webhook sent from executor!",
}

local headers = {
    ["Content-Type"] = "application/json"
}

local payload = game:GetService("HttpService"):JSONEncode(data)

http({
    Url = webhookUrl,
    Method = "POST",
    Headers = headers,
    Body = payload
})
