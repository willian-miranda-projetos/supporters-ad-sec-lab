# 🏢 Supporters - Active Directory Security Lab

## 📌 Sobre o Projeto

Este projeto simula a implementação de um ambiente corporativo completo baseado em Active Directory, com foco em **segurança, hardening e preparação para SIEM (Wazuh)**.

A estrutura foi construída como se fosse uma empresa real chamada **Supporters**, com separação de departamentos, políticas de segurança e controle de acesso.

---

## 🎯 Objetivos

* Implementar um domínio Active Directory funcional
* Aplicar boas práticas de segurança (hardening)
* Configurar auditoria avançada para integração com SIEM
* Mitigar riscos de lateral movement
* Implementar controle de credenciais com LAPS

---

## 🏗️ Arquitetura

* 1x Domain Controller (Windows Server 2022)
* Clientes Windows 10/11 ingressados no domínio
* Estrutura de OUs por departamento:

  * Financeiro
  * RH
  * TI
* Grupos de segurança organizados

---

## 🔐 Segurança Implementada

### 👤 Controle de Usuário

* Restrição de Painel de Controle
* Bloqueio de CMD e Regedit
* Controle de acesso a ferramentas administrativas

### 🖥️ Hardening de Endpoint

* SMB Signing habilitado
* Redução de credenciais em cache
* Configurações de segurança aplicadas via GPO

### 🔍 Auditoria (SIEM Ready)

* Logon Success/Failure (4624 / 4625)
* Process Creation (4688 com command line)
* Credential Usage (4648)
* Policy Change e Privilege Use

### 🔑 LAPS (Local Administrator Password Solution)

* Rotação automática de senha
* Armazenamento no Active Directory
* Conta de administrador local habilitada via GPO

### 🚫 Proteção contra Lateral Movement

* Auditoria de NTLM habilitada
* Ambiente operando com Kerberos
* Bloqueio de NTLM:

  * Deny for domain accounts

---

## 📊 Resultados Obtidos

* Ambiente operando com autenticação Kerberos
* NTLM praticamente inexistente
* Logs ricos para análise em SIEM
* Base pronta para integração com Wazuh

---

## 📁 Documentação

* GPOs detalhadas: `/docs/GPO_Configuracoes_SUP.txt`
* Estrutura do ambiente: `/docs/arquitetura.md`
* Checklist de implantação: `/docs/checklist_implantacao.md`

---

## 🚀 Próximos Passos

* Integração com Wazuh (SIEM)
* Criação de regras de detecção
* Simulação de ataques (Red Team)
* Monitoramento e resposta a incidentes

---

## 🧠 Autor

Projeto desenvolvido com foco em evolução profissional em infraestrutura e segurança da informação.

---

## 🏁 Conclusão

Este laboratório representa um ambiente corporativo funcional, seguro e preparado para monitoramento e detecção de ameaças, aplicando boas práticas de mercado em Active Directory e segurança ofensiva/defensiva.
