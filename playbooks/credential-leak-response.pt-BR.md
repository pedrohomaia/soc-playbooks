# Playbook — Suspeita de credenciais vazadas

## Gatilho (alerta)
- Alerta de exposição (fontes públicas/monitoramento), report interno, credenciais reutilizadas
- Tentativas de login incomuns no IdP/SSO

## Triagem (10–15 min)
- Identificar contas potencialmente afetadas
- Verificar sinais de acesso (logins recentes, falhas, novas sessões, MFA prompts)
- Checar se a credencial era usada em sistemas críticos

## Investigação
- Confirmar origem do alerta (confiabilidade / contexto)
- Correlacionar com: logins de locais/horários incomuns, resets de senha, criação de tokens
- Verificar atividades sensíveis: alterações de email/senha, permissões, criação de chaves

## Contenção
- Reset imediato de senha + revogar sessões/tokens
- Forçar MFA (se não existir), rotação de chaves de API
- Bloquear logins suspeitos (IP/ASN) se aplicável

## Erradicação e Recuperação
- Revisar permissões e logs de auditoria
- Orientar usuário (higiene de senhas, gerenciador, não reutilizar)
- Ajustar políticas (MFA, passwordless, detecção de anomalia)

## Pós-incidente
- Melhorar detecções (impossible travel, múltiplas falhas)
- Revisar processo de onboarding/offboarding
