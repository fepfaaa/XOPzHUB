_G.Key = 'I-SUS-KEN'

VPSIP = "127.0.0.1"

function script()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/fepfaaa/XOPSCRIPTz/main/SCRIPTXOP.lua"))();
end





local server = syn.request({
    Url = "http://127.0.0.1/server.php?key=".._G.Key,
    Method = "GET"
})

local decode = syn_crypt_b64_decode(server.Body)

if decode == "" then
    print("Invaild Key")
elseif decode == "Invalid Key" then
      print("Invaild Key") 
elseif decode == "Update Hwid" then
    print("Update Hwid")
elseif decode == "Invalid HWID" then
    print("Invalid HWID")
elseif decode == "You Are Got Blacklist" then
   print("You Are Got Blacklist")
elseif decode == "Whitelist" then
    script()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/fepfaaa/XOPSCRIPTz/main/SCRIPTXOP.lua"))();
end
