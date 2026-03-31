
# 📊 Resumo de GPOs - Supporters

## 👤 Usuários

### GPO_USERS_BASICA

* Controle do Painel de Controle
* Permissão de recursos essenciais

### GPO_USERS_RESTRICOES_INTELIGENTES

* Bloqueio de CMD
* Bloqueio de Regedit

---

## 🖥️ Computadores

### GPO_COMPUTADORES_HARDENING_LEVE

* SMB Signing
* CachedLogonsCount = 1

---

## 🔍 Auditoria

### GPO_AUDITORIA_SEGURANCA

* Logon (4624 / 4625)
* Process Creation (4688)
* Credential usage (4648)

### GPO_AUDITORIA_BASICA

* Force Advanced Audit

---

## 🔑 Credenciais

### GPO_LAPS_ADMIN_LOCAL

* Rotação de senha local
* Backup no AD

### GPO_ADMIN_LOCAL_ATIVACAO

* Ativação do usuário Administrator

---

## 🔐 Segurança Avançada

### GPO_NTLM_AUDIT

* Monitoramento de NTLM

### GPO_NTLM_BLOCK

* Bloqueio de NTLM (Deny for domain accounts)

---

## 🧠 Resultado Final

* Ambiente baseado em Kerberos
* NTLM desabilitado
* Hardening aplicado
* SIEM-ready
