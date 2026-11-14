# Recriar a equipa noutro OpenBot

Este pacote ajuda a reproduzir a configuração atual, mas o OpenBot não importa o manifesto automaticamente.

## Passos

1. Cria a secção `Equipa de Agentes`.
2. Para cada entrada em `openbot-manifest.json`, cria um agente com o mesmo nome e título e cola o ficheiro indicado em `profileFile` como instruções.
3. Seleciona o provider/modelo e `reasoningEffort` indicados no manifesto.
4. Define `access` para `workspace`; replica `computerUse`, `notifications` e `autoApprove`.
5. Instala/ativa as integrações MCP indicadas. MCP é uma ligação do servidor OpenBot e pode precisar de autenticação própria; não está embutida neste repositório.
6. Atribui todos os nove agentes à secção e usa `pipelineOrder` para a sequência de trabalho.

## Limites da reprodução

- Os IDs dos agentes e da secção são locais e não são reutilizáveis; o OpenBot atribui IDs novos.
- Conversas, anexos de conversas, estado de tarefas, ligações/autenticações de serviços, configuração da conta e dados locais não são exportados.
- O `initialMessage` não foi preservado. As rotinas e skills listadas estavam vazias na leitura atual.
- A preferência `autoApprove` só pode ser alterada pelo utilizador nas definições do agente; nesta equipa está desligada.
- A configuração de um agente não prova que controlos de negociação estejam implementados. O pacote não instala Freqtrade nem configura ordens ou API Bybit.

## Dados do snapshot

O manifesto regista o que foi lido do OpenBot em 14-11-2026. Provedores, modelos e integrações podem não estar disponíveis no outro servidor ou conta. Confirma cada valor ao recriar.
