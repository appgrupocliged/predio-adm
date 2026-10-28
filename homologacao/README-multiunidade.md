# Homologação multiunidade — CLIGED QR

## Objetivo
Preparar Prédio Administrativo Macaé (19 locais) e Clínica CLIGED Macaé (8 locais levantados) para compartilharem o mesmo sistema de QR Codes, TomTicket (cliente atual, departamento Infraestrutura e atendente Gleice) e Google Chat.

## Regras inegociáveis
- Não alterar a branch main nem fazer deploy sem testes e aprovação.
- Links impressos do Prédio ADM (`?local=B.14`) devem continuar funcionando e indicar ADM-MCE.
- Links futuros devem identificar unidade e local (`?unidade=CLI-MCE&local=B.01`).
- Identificações B.01 a B.08 da clínica são provisórias até validação física.
- Cliente, departamento, operador e integração Google Chat são centralizados.
- O catálogo técnico no repositório da API **não está ativado no Worker** e não gera QR Codes.
- O arquivo `worker.js` de produção permanece a referência para o fluxo atual.

## Pendências de implementação antes de habilitar a clínica
1. Endpoint de catálogo e roteamento por unidade no Worker.
2. Conclusão autenticada e validação entre chamado, unidade e local.
3. Idempotência da abertura para evitar chamados duplicados.
4. Resposta mínima da rota de status.
5. Atualização dos HTMLs para catálogo e navegação segura.
6. Homologação separada no Cloudflare e no GitHub Pages.
7. Testes simulados e depois testes integrados com credenciais e espaços de TESTE.

## Situação
Apenas branch e documentação/catálogo de homologação. Nenhuma mudança no serviço ativo.
