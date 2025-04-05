-- Fronthook GUI with Rayfield

-- Rayfield Loader
loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

-- Notification
Rayfield:Notify({
    Title = "Fronthook",
    Content = "GUI inicializado com sucesso!",
    Duration = 6.5,
    Image = 4483362458,
    Actions = {
        Ignore = {
            Name = "Fechar",
            Callback = function() end
        }
    }
})

-- Janela principal
local Window = Rayfield:CreateWindow({
    Name = "Fronthook - Hub",
    LoadingTitle = "Fronthook está carregando...",
    LoadingSubtitle = "by @guxtaDelas",
    ConfigurationSaving = {
        Enabled = true,
        FolderName = "Fronthook",
        FileName = "HubConfig"
    },
    Discord = {
        Enabled = true,
        Invite = "fronthook",
        RememberJoins = true
    },
    KeySystem = false
})

-- Aba: Combat
local CombatTab = Window:CreateTab("⚔️ Combat", 4483362458)
CombatTab:CreateParagraph({Title = "Seção de Combate", Content = "Ferramentas úteis para PvP"})

CombatTab:CreateButton({
    Name = "Aimbot (em breve)",
    Callback = function()
        Rayfield:Notify({
            Title = "Aimbot",
            Content = "Essa função ainda está em desenvolvimento.",
            Duration = 4
        })
    end,
})

-- Aba: Player
local PlayerTab = Window:CreateTab("🏃 Player", 4483362458)
PlayerTab:CreateParagraph({Title = "Player Tools", Content = "Ferramentas para movimentação e interação"})

PlayerTab:CreateButton({
    Name = "Fly (em breve)",
    Callback = function()
        Rayfield:Notify({
            Title = "Fly",
            Content = "Essa função será adicionada futuramente.",
            Duration = 4
        })
    end,
})

-- Aba: Visual
local VisualTab = Window:CreateTab("🧿 Visual", 4483362458)
VisualTab:CreateParagraph({Title = "ESP / Visual", Content = "Melhore sua visão do jogo"})

VisualTab:CreateButton({
    Name = "ESP (em breve)",
    Callback = function()
        Rayfield:Notify({
            Title = "ESP",
            Content = "Função de ESP ainda não disponível.",
            Duration = 4
        })
    end,
})

-- Aba: Miscelânea
local MiscTab = Window:CreateTab("🧩 Misc", 4483362458)
MiscTab:CreateParagraph({Title = "Outros Scripts", Content = "Ferramentas adicionais"})

MiscTab:CreateButton({
    Name = "TP Kill (em breve)",
    Callback = function()
        Rayfield:Notify({
            Title = "TP Kill",
            Content = "TP Kill será adicionado futuramente.",
            Duration = 4
        })
    end,
})

MiscTab:CreateButton({
    Name = "Rejoin",
    Callback = function()
        game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
    end,
})

-- Aba: Créditos
local CreditsTab = Window:CreateTab("💬 Créditos", 4483362458)
CreditsTab:CreateParagraph({
    Title = "Desenvolvido por",
    Content = "Fronthook GUI por @guxtaDelas\nBaseado na Rayfield UI Library"
})
