script_key = "CVtVbafUZJYwgaiaiTJWKtLuEArcRpqS" 
getgenv().Team = "Pirates"
getgenv().WebhookSetting = {
    Enable = true,
    Url = "",
    Embed = true,
    StoredFruit = true,
    ImageEmbed = true,
    CustomImage = true,
    CustomImageUrl = "https://cdn.discordapp.com/attachments/1240444143717716052/1240444901699878983/Du_an_moi_03B4A16.gif?ex=6647e756&is=664695d6&hm=44adffc984c81b15e5f907b415ea8740fbdd738a8d1a7b6de6c04795a5f86f77&", --Your Url
    OnServerHop = true,
    BountyChanged = true,
}
getgenv().PlayerSetting = {
    SafeMode = true,
    SafeModeHealth = {4000,70},--Number And %, Start Safe Mode And Stop Safe Mode
    UseRaceV3 = true,
    SmartUseRaceV3= true,
    DashIfV4 = true,
    Dash=true,
    IgnoreInCombat = true, --Turn This Off When Reseting Or Hop You Lost Bounty (Rare, Happens On Some Accounts)
    ChatKillEnable = false,
    Chat = {"config by phfeelsig","w-azure"},
    IgnoreFriends = true, --Serverhop if you friend in your server
}
getgenv().AttackSetting = {
    ForceMelee = true,
    ForceMeleeTime = 3.5,
    StopAttack =true, --When Meet Below Condition
    StopAttackAtHealth = 70,--%
    FastAttack=true, -- Toggle Fast Attack
}
getgenv().UseSkillSetting = {
    -- Three Methods: "Normal", "Fast", "Spam", "SpamAll"
    MethodIfTargetOnV4 = "Fast",
    MethodIfPlayerOnV4 = "Normal",
    MethodIfTargetUseFruit = {Fruits={},Method="Fast"},
    NormalMethod = "Normal",
    LowHealthPlayerCondition = { --Player Can Attack Us, No Need For Slow Attack
        Enable = true,
        Health = 60,--%Health That Are Low
        Method = "Fast",
    },
    LowHealthTargetCondition = {
        Enable = true,
        Health = 30,--%Health That Are Low
        DelayFirstTime = {true,2}, --1 Is Enable, 2 Is Second To Delay Before Attack Again
        Method = "Normal",
        WaitTime = 1,-- If Normal Method, Wait Every Skill If It Hits Target
    }
}
getgenv().WeaponsSetting = {
    ["Melee"] = {
        ["Enable"] = true,
        ["Delay"] = 2.5, 
        ["SwitchNextWeaponIfCooldown"] = true,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["NoPredict"] = false, -- For Dragon Tailon, Disable it 
                ["HoldTime"] = 0.3,
                ["TimeToNextSkill"] = 0,
            },
        [ "X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.2,
                ["TimeToNextSkill"] = 0,
            },

            ["C"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.5,
                ["TimeToNextSkill"] = 0,
            },
        },
    },
    ["Blox Fruit"] = {
        ["Enable"] = false,
        ["Delay"] = 4,
        ["SwitchNextWeaponIfCooldown"] = true,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 2,
                ["TimeToNextSkill"] = 0,
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0,
                ["TimeToNextSkill"] = 0,
            },

            ["C"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0,
                ["TimeToNextSkill"] = 0,
            },
            ["V"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0,
                ["TimeToNextSkill"] = 0,
            },
            ["F"] = {
                ["Enable"] = false,
                ["HoldTime"] = 0,
                ["TimeToNextSkill"] = 0,
            },
        },
    },
    ["Sword"] = {
        ["Enable"] = true,
        ["Delay"] = 1.5,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 1,
                ["TimeToNextSkill"] = 0.2,
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.3,
                ["TimeToNextSkill"] = 2,
            },
        },
    },
    ["Gun"] = {
        ["Enable"] = false,
        ["Delay"] = 0.5,
        ["Skills"] = {
            ["Z"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0,
            },
            ["X"] = {
                ["Enable"] = true,
                ["HoldTime"] = 0.1,
                ["TimeToNextSkill"] = 0,
            },
        },
    },
}
getgenv().Theme = { -- getgenv().Theme = false if you want to disable
    OldTheme = false,
    Name="xFade", -- config by xfein
    Custom={
            ["Enable"] = true,
            ['char_size'] = UDim2.new(0.668, 0, 1.158, 0),
            ['char_pos'] = UDim2.new(0.463, 0, -0.105, 0),
            ['title_color'] = Color3.fromRGB(230, 230, 250),
            ['titleback_color'] = Color3.fromRGB(123, 104, 238),
            ['list_color'] = Color3.fromRGB(230, 230, 250),
            ['liststroke_color'] = Color3.fromRGB(123, 104, 238),
            ['button_color'] = Color3.fromRGB(230, 230, 250)
       }
}
loadstring(game:HttpGet("https://api.luarmor.net/files/v3/loaders/248f97d7a28a4d09c641d8279a935333.lua"))()
