# AI Trading Desk — perfis da equipa

Exportação dos perfis atualmente configurados no OpenBot, preparada para consulta e reutilização noutro computador.

## Conteúdo

- `agents/`: instruções por agente, em Markdown.
- `PROJECT.md`: âmbito, sequência de trabalho, controlos e limitações conhecidas.

## Importante

Este repositório contém prompts/instruções, não uma aplicação pronta para negociar. Não inclui código de estratégia, instalação/configuração Freqtrade, ligação à Bybit, credenciais, dados de conta nem automatização dos controlos descritos. Os perfis não criam por si só bloqueios técnicos de ordens. Para usar noutro OpenBot, cria os agentes e cola o conteúdo dos respetivos ficheiros no campo de instruções; permissões, integrações, rotinas e aprovações devem ser configuradas separadamente.

Mantém este repositório privado. Nunca guardes chaves API, segredos, ficheiros de configuração privados ou dados pessoais nele.

## Agentes

1. Alpha Estr — pesquisa de estratégias
2. Quant Bteste — backtests e validação
3. Tuner — otimização
4. Pair Hunter — universo de contratos
5. Incubator — paper trading
6. Risk Officer — revisão de risco e veto
7. Live Trader — execução, apenas com autorização e integração verificável
8. Desk Chief — coordenação
9. VPS Watcher — tráfego da VPS, separado do trading
