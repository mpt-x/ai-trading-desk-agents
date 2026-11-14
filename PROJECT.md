# AI Trading Desk — resumo do projeto

## Âmbito

Futuros Perpétuos lineares da Bybit liquidados em USDT. O projeto considera posições Long e Short, taxas, funding, alavancagem, margem e liquidação. A regra operacional pretendida é uma posição global de cada vez.

## Pipeline

Alpha Estr → Quant Bteste → Tuner → Pair Hunter → Incubator → Risk Officer → Live Trader. Desk Chief coordena e apresenta evidências. VPS Watcher é independente e trata apenas do tráfego Kamatera.

## Controlo de uma posição

Para operação Freqtrade, os perfis exigem subconta dedicada, uma instância, `max_open_trades=1`, ausência de atividade manual/externa, leitura de posições e ordens pendentes e registo de sinais concorrentes suprimidos. Se houver várias instâncias, seria necessário um árbitro serializado comum e comprovado. Prompts e configurações isoladas não demonstram que este controlo esteja implementado; estado incerto bloqueia entradas.

## Limitações do Freqtrade/Bybit registadas nos perfis

As notas oficiais consultadas para Freqtrade 2026.8 indicam suporte Bybit Futures apenas em margem isolada, modo one-way definido no arranque, conta dedicada por bot e ausência de funding histórico Bybit no Freqtrade; a taxa calculada em dry-run também é usada em live. Confirma a versão instalada e a documentação correspondente antes de testes ou live. Cross deve ser identificado como simulação e funding histórico exige uma fonte externa verificada.

## Passagens de trabalho

Cada passagem deve manter versão/hash, configuração, fontes e períodos dos dados, universo, custos/funding, critérios prévios, métricas Long/Short, limitações e evidências. Gráficos devem indicar fonte, período e o que é observado ou simulado. Critérios de aceitação não mudam depois de vistos os resultados.

## Estado conhecido na exportação

Os perfis instruem salvaguardas; não foi encontrada uma implementação local Freqtrade neste workspace nem uma integração Bybit API ativa nesta configuração. Portanto, esta exportação não está pronta para enviar ordens. Live exige revisão aprovada do Risk Officer, limites numéricos definidos pelo utilizador, autorização explícita, conta limpa e SL/TP aprovados e ativos.

## Segurança

Não incluir credenciais no GitHub, nos prompts ou no chat. Guardar segredos apenas no gestor de segredos local/Vault ou em ficheiro privado fora do Git. O repositório deve permanecer privado.
