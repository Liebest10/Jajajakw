local scriptCode = [[
-- Configuração de sorte
local baseChance = 10 -- Chance base de 10%
local luckBonus = 20  -- Bônus de sorte (20% extra)

-- Função para calcular se o jogador tem sorte
function isLucky()
    local finalChance = baseChance + luckBonus
    local randomNumber = math.random(1, 100) -- Gera um número entre 1 e 100
    return randomNumber <= finalChance
end

-- Testando o sistema de sorte
if isLucky() then
    print("Você teve sorte! Recebeu um item raro!")
else
    print("Não foi dessa vez. Tente novamente!")
end
]]

-- Executando o script com loadstring
local func = loadstring(scriptCode)
if func then
    func()
else
    print("Erro ao carregar o script.")
end
