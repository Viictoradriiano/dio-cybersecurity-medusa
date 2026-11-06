# 🛡️ Desafio DIO: Simulando um Ataque de Brute Force com Medusa e Kali Linux

Repositório criado para documentar o desafio prático de auditoria de segurança e simulação de ataques de força bruta utilizando o **Kali Linux** e a ferramenta **Medusa**, em um ambiente controlado com o **Metasploitable 2**.

---

## 📋 Sumário
- [Descrição do Desafio](#-descrição-do-desafio)
- [Ambiente Utilizado](#-ambiente-utilizado)
- [Passo a Passo da Execução](#-passo-a-passo-da-execução)
  - [1. Criação das Wordlists](#1-criação-das-wordlists)
  - [2. Execução do Ataque com Medusa](#2-execução-do-ataque-com-medusa)
  - [3. Validação do Acesso (FTP)](#3-validação-do-acesso-ftp)
- [Resultados e Evidências](#-resultados-e-evidências)
- [Medidas de Mitigação e Defesa](#-medidas-de-mitigação-e-defesa)

---

## 🎯 Descrição do Desafio
O objetivo deste laboratório prático é compreender os riscos associados a senhas fracas e serviços expostos, simulando um ataque de força bruta (*Brute Force*) contra o serviço FTP em uma máquina vulnerável dentro de um ambiente isolado.

---

## 💻 Ambiente Utilizado
* **Máquina Atacante:** Kali Linux (VirtualBox)
* **Máquina Alvo:** Metasploitable 2 (VirtualBox)
* **Rede:** Adaptador Somente Hospedado (Host-Only) para isolamento seguro do laboratório.
* **Ferramentas:** 
  * `Medusa v2.3` (Testes automatizados de força bruta)
  * `Cliente FTP` (Validação de credenciais)

---

## 🚀 Passo a Passo da Execução

### 1. Criação das Wordlists
Foram criados arquivos de texto contendo listas de usuários potenciais e senhas comuns para testar contra o endereço IP do alvo (`192.168.56.101`).

* **Criação da wordlist de senhas (`passwords.txt`):**
```bash
echo -e "password\n123456\nWelcome123\nmsfadmin" > passwords.txt
