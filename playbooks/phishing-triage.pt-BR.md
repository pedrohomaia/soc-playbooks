# Playbook — Phishing Triage

## Gatilho (alerta)
- Report de usuário / alerta de email gateway / IOC conhecido

## Triagem (10–15 min)
- Identificar remetente/domínio (sem clicar em links)
- Verificar assunto, urgência, anexos e URLs
- Buscar mensagens semelhantes em outros destinatários

## Investigação
- Validar reputação do domínio e se há lookalike
- Verificar se houve clique/execução (telemetria EDR/Proxy)
- Checar possíveis credenciais expostas (tentativas de login)

## Contenção
- Bloquear domínio/URL/anexo no gateway
- Isolar máquinas com sinais de execução maliciosa
- Reset de senha e MFA se houver risco de credencial

## Erradicação e Recuperação
- Remover artefatos, revisar regras, reforçar filtro
- Comunicar usuários afetados

## Pós-incidente
- Ajustar detecções, treinar usuários e registrar lições
