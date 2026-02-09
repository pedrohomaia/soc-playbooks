# Playbook — Login suspeito / Acesso anômalo

## Gatilho (alerta)
- Impossible travel
- Novo dispositivo/localização
- Burst de falhas seguido de sucesso
- Login fora do horário padrão

## Triagem (10–15 min)
- Confirmar conta e contexto (VIP? acesso admin?)
- Verificar localização, dispositivo, user-agent, ASN (se disponível)
- Conferir se o usuário reconhece a atividade

## Investigação
- Analisar sequência: falhas → sucesso → ações sensíveis
- Verificar alterações de segurança (senha/MFA/email)
- Checar logs correlatos (VPN, EDR, proxy, DNS)

## Contenção
- Revogar sessões ativas
- Reset de senha e exigir MFA
- Bloquear origem se houver confirmação de abuso

## Erradicação e Recuperação
- Revisar acessos e permissões
- Verificar persistência (tokens/chaves adicionadas)
- Restaurar integridade da conta

## Pós-incidente
- Ajustar thresholds e reduzir falsos positivos
- Recomendar hardening de autenticação (MFA forte, device trust)
