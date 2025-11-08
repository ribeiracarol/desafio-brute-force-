# Desafio DIO - Bootcamp Santander Cibersegurança 2025

# 🛡️ Simulando um Ataque de Brute Force de Senhas com Medusa e Kali Linux

## 📜 Visão Geral do Projeto

Este projeto é um **laboratório prático de cibersegurança** focado em ataques de **Força Bruta (Brute-Force)**. Utilizando a distribuição **Kali Linux** e a ferramenta **Medusa**, simulamos cenários de invasão em ambientes controlados e vulneráveis, como o **Metasploitable 2** e o **DVWA (Damn Vulnerable Web Application)**.

O principal objetivo é **compreender, executar e documentar** o processo de um ataque de força bruta em diferentes serviços, e, mais importante, **exercitar e propor medidas de prevenção e mitigação** para essas vulnerabilidades.

-----

## 🎯 Objetivos de Aprendizagem

Ao longo deste desafio, os seguintes objetivos foram alcançados:

  * **Compreensão de Ataques:** Entender como os ataques de força bruta se manifestam em diferentes protocolos (FTP, Web, SMB).
  * **Utilização de Ferramentas:** Adquirir proficiência no uso do **Kali Linux** e da ferramenta **Medusa** para auditoria de segurança.
  * **Documentação Técnica:** Desenvolver a habilidade de documentar processos técnicos, comandos e evidências de forma clara e estruturada.
  * **Mitigação:** Reconhecer vulnerabilidades e propor soluções e medidas de defesa eficazes.
  * **Portfólio:** Utilizar o **GitHub** como portfólio técnico para compartilhar conhecimento e evidências de aprendizado.

-----

## 🎯 Ferramentas

medusa – ataques de força-bruta (FTP, HTTP, SMB)

nmap – descoberta de hosts e serviços

enum4linux – enumeração SMB

smbclient – acesso e validação de compartilhamentos SMB

-----

## ⚙️ Configuração do Ambiente

O ambiente de laboratório foi montado utilizando máquinas virtuais (VMs) no **VirtualBox** para garantir que todos os testes fossem realizados em um espaço isolado e seguro.

  * **Sistema Atacante:** **Kali Linux** (VM 1)
      * **Ferramenta Principal:** **Medusa**
  * **Sistemas Alvo/Vulneráveis:**
      * **Metasploitable 2** (VM 2)
      * **DVWA** (Hospedado no Metasploitable 2 ou em outra VM, conforme a configuração)
  * **Configuração de Rede:**
      * As VMs foram configuradas com uma rede **Host-Only (Rede Interna)** para isolar o tráfego de ataque da rede local.

-----

## 🔬 Cenários de Ataque Simulado

Os testes foram divididos em cenários específicos para demonstrar a versatilidade dos ataques de força bruta.

### 1\. Força Bruta em Serviço FTP

### 2\. Automação de Tentativas em Formulário Web (DVWA)

### 3\. Password Spraying em Serviço SMB


-----

## 📝 Documentação e Mitigação

Esta seção detalha os artefatos gerados e as principais recomendações de segurança.

### Wordlists e Scripts

  * As **wordlists** utilizadas foram simples e criadas para fins educacionais, focadas em credenciais fracas. (Disponíveis na pasta `/wordlists`).
  * **Comandos:** Uma lista completa dos comandos Medusa e demais ferramentas. (Disponíveis em `commands.txt`).

### Medidas de Mitigação Recomendadas 🔑

| Vulnerabilidade | Medida de Prevenção | Detalhes |
| :--- | :--- | :--- |
| Senhas Fracas | Forçar o uso de **senhas complexas** e longas. | Implementar políticas de complexidade mínima (maiúsculas, minúsculas, números, símbolos). |
| Força Bruta | Implementar **mecanismos de *lockout*** (bloqueio de conta). | Bloquear o acesso por um período (ex: 30 minutos) após 3 a 5 tentativas falhas. |
| Serviços Expostos | **Restrição de Rede** e **Rate Limiting**. | Limitar o número de requisições por IP em um intervalo de tempo, especialmente para formulários de login. |
| Autenticação | Adotar **Autenticação de Múltiplos Fatores (MFA)**. | Adicionar uma camada de segurança que impede a invasão apenas com a senha comprometida. |

-----

## 🔗 Repositório

* /images
* /wordlists
* commands.txt
