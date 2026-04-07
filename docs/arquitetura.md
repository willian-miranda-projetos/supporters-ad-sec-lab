
# 🏗️ Arquitetura do Ambiente - Supporters

## 📌 Visão Geral

Este ambiente simula a infraestrutura de uma empresa fictícia chamada **Supporters**, com foco em Active Directory, segurança e hardening.

---

## 🖥️ Componentes

### 🔹 Domain Controller

* Sistema: Windows Server 2022
* Funções:

  * Active Directory Domain Services (AD DS)
  * DNS Server
  * DHCP Server (rede isolada)

---

### 🔹 Clientes

* Sistema: Windows 10/11
* Ingressados no domínio `sup.local`
* Recebem políticas via GPO

---

## 🌐 Rede

* Segmento interno: `10.10.10.0/24`
* Domain Controller: `10.10.10.10`
* DHCP controlado pelo servidor
* DNS apontando para o DC

---

## 🗂️ Estrutura de OUs

```
SUPPORTERS
(SUP.LOCAL)
├── ADMIN
│   ├── Admins de Dominio
│   └── Admins de Servidores
├── COMPUTADORES
│   ├── Financeiro
│   ├── RH
│   └── TI
├── CONTAS DE SERVIÇO
│   ├── Distribuição
│   └── Segurança
├── SERVIDORES
│   ├── Application Servers
│   ├── Domain Controllers
│   └── File Servers
├── SUPPORTERS
│   ├── Financeiro
│   ├── RH
│   └── TI

```

---

## 🔐 Segurança Aplicada

### 🔹 Controle de Usuário

* Restrição de painel de controle
* Bloqueio de CMD e Regedit

### 🔹 Hardening

* SMB Signing habilitado
* Credenciais em cache reduzidas

### 🔹 Auditoria

* Eventos 4624, 4625, 4648, 4688
* Command line habilitado

### 🔹 LAPS

* Rotação de senha automática
* Armazenamento no AD

### 🔹 NTLM

* Auditoria habilitada
* Bloqueio aplicado (Deny for domain accounts)

---

## 🧠 Modelo de Autenticação

* Kerberos como protocolo principal
* NTLM desabilitado no domínio
* Ambiente preparado para SIEM

---

## 🎯 Objetivo da Arquitetura

Criar um ambiente:

* Seguro
* Monitorável
* Próximo da realidade corporativa
* Preparado para integração com Wazuh
