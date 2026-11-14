# AI Trading Desk — perfis da equipa

Exportação da equipa AI Trading Desk atualmente configurada no OpenBot, preparada para consulta e recriação noutro computador.

## Conteúdo

- `agents/`: instruções por agente, em Markdown.
- `PROJECT.md`: âmbito, sequência de trabalho, controlos e limitações conhecidas.
- `openbot-manifest.json`: nomes, modelos, nível de raciocínio, permissões, ferramentas e agrupamento atuais.
- `RECREATE.md`: instruções de configuração manual.

## Importante

O OpenBot não fornece importação de agentes a partir deste manifesto. O repositório é um pacote de recriação manual, não uma cópia instantânea do ambiente. Não contém histórico/conversas, IDs locais dos agentes, código de estratégia, instalação/configuração Freqtrade, ligação à Bybit, credenciais nem dados de conta. Também não automatiza os controlos descritos. Segue `RECREATE.md` para configurar os agentes.

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
