# 🛡️ Cibersegurança & Infraestrutura | Portfólio Prático

**Samuel Araújo Cocchi Amaral** | *Graduando em Cibersegurança | Analista em Formação | Blue & Red Team* 📍 São Paulo, SP, Brasil | 🔗 [LinkedIn](https://www.linkedin.com/in/samuel-araujo-608532271/) | ✉️ mr.oreo0207@gmail.com | 📞 11 93465-5319

---

## 👨‍💻 Sobre Mim
Profissional de TI com sólida base em redes corporativas e infraestrutura, atualmente focado em Cibersegurança Tática. Trago a experiência prática do ambiente corporativo como estagiário na IDT Corporation (Net2Phone) e uma base técnica robusta forjada em Informática (Senac) e Eletrônica (ETEC). 

Minha abordagem de segurança é orientada ao ciclo completo (*Kill Chain*): não apenas explorar vulnerabilidades em laboratórios (*Red Team*), mas principalmente projetar e aplicar mitigações de rede, *hardening* de servidores e auditorias de conformidade (*Blue Team*).

🎓 **Educação:** Cibersegurança - Faculdade Impacta (Previsão: Jun/2027)  
🏆 **Certificações Ativas:** Cisco CCNA (Introduction to Networks | SRWE) | Cisco IT Essentials | Network Security | NDG Linux Unhatched | Python Essentials 1

---

## 🛠️ Stack Tecnológico & Habilidades

* **Sistemas & Infraestrutura:** Administração em Windows Server, Linux Ubuntu e Cisco IOS. Arquitetura de Redes L2/L3 e Topologias Seguras.
* **Defensive Security (Blue Team):** Hardening de Servidores (IIS, Apache, WordPress), Mitigação em Nível de Kernel (Netfilter/iptables), Port Security, Gestão de Identidade e Acesso (SSH Keys, RBAC), Patching corporativo.
* **Offensive Security (Red Team):** Enumeração de Serviços (Nmap, Netdiscover), Análise de Vulnerabilidades (OpenVAS/Greenbone), Exploração (Metasploit Framework, Exploit-DB, Hydra), Esgotamento de Recursos (MAC Flooding), Injeções de SQL (SQLmap).

---

## 🔬 Projetos em Destaque: Laboratório de Auditoria e Mitigação

Este repositório documenta auditorias ponta a ponta realizadas em um ambiente de laboratório isolado, englobando ecossistemas Windows, Linux e Infraestrutura de Redes[cite: 74].

### 1. 🛡️ Segurança de Infraestrutura L2: Switch Cisco
* **Red Team:** Saturação de memória CAM (*MAC Flooding*) induzindo o equipamento ao estado de *Fail-Open* para interceptação de tráfego *unicast*.
* **Blue Team:** Hardening arquitetural da interface de acesso aplicando os princípios de *Zero Trust* L2 via *Port Security* (`maximum 1` e `violation shutdown`), contendo a ameaça na borda.
* 📄 **[Ver Playbook Tático e Prova de Conceito](./Auditorias_e_Pentests/MAC-Flooding-L2-Security/Playbook-MAC-Flooding.md)**

### 2. 🌐 Auditoria Web e Banco de Dados: Máquina N7 (Linux Ubuntu)
* **Red Team:** Exploração crítica de *Time-Based Blind SQLi* contornando autenticação e automatizando a exfiltração total de banco de dados e credenciais em *plaintext* utilizando SQLmap.
* **Blue Team:** Refatoração da arquitetura de código aplicando *Prepared Statements* (PDO), implantação de WAF (ModSecurity com OWASP CRS) e aplicação do Princípio do Menor Privilégio no motor MySQL.
* 📄 **[Ver Playbook Tático e Exfiltração](./Auditorias_e_Pentests/Web_N7/01_Playbook_N7_Blind_SQLi.md)**

### 3. 🐧 Auditoria e Hardening: Metasploitable (Linux)
* **Red Team:** Exploração de *backdoor* crítico em serviço legado (vsftpd 2.3.4), Execução Remota de Comandos (RCE) via Samba (CVE-2007-2447), e *deploy* malicioso em Apache Tomcat[cite: 75]. Escalonamento de privilégios via força bruta com *downgrade* criptográfico no OpenSSH 4.7p1[cite: 76].
* **Blue Team:** Contenção de perímetro via *firewall* (iptables `DROP`), mitigação de configurações padrão, auditoria de senhas fracas e reestruturação de acesso SSH[cite: 77].
* 📄 **[Ver Playbooks e Relatórios Táticos](./Auditorias_e_Pentests/Metasploitable/)**

### 4. 🪟 Auditoria e Contenção: Máquina Shadow (Windows Server)
* **Red Team:** Exploração da vulnerabilidade crítica SMBv1 (EternalBlue)[cite: 78].
* **Blue Team:** Mitigação tática via PowerShell e aplicação de políticas de *Patching* corporativo[cite: 79].
* 📄 **[Ver Playbook de Defesa](./Auditorias_e_Pentests/Windows_Shadow/01_Playbook_Shadow_EternalBlue_MS17-010.md)** 

### 5. 🌐 Auditoria Web: Máquina Storm (Windows 10)
* **Red Team:** Exploração de serviços de áudio e sequestro de token no Microsoft IIS[cite: 80].
* **Blue Team:** Estratégias de mitigação e controle de acesso a serviços web[cite: 81].
* 📄 **[Ver Documentação](./Auditorias_e_Pentests/Windows_Storm/01_Playbook_Storm_Icecast_TokenMagic.md)** 

### 6. 🔒 Hardening de CMS: Máquina CSEC (Linux Ubuntu)
* **Red Team:** Comprometimento via exploração de *backdoor* no ProFTPD 1.3.3c[cite: 82].
* **Blue Team:** Implementação de *Hardening* em ecossistema Apache/WordPress, bloqueando ataques de amplificação e desativando XML-RPC via `.htaccess`[cite: 83].
* 📄 **[Ver Relatórios Ofensivos e Mitigação](./Auditorias_e_Pentests/Linux_CSEC/01_Playbook_CSEC_ProFTPD_WordPress.md)** 

---

## 🤝 Extensão e Consultoria

### Projeto de Consultoria em Segurança Escolar
Participação em projeto prático de consultoria e conscientização em cibersegurança desenvolvido para a **Escola Estadual Prof. Nelson Pizzotti Mendes**, traduzindo conceitos técnicos complexos de proteção de dados e segurança digital para o ambiente acadêmico e educacional.

---
*Nota: Todos os testes documentados neste repositório foram executados em ambientes de laboratório locais, estritamente controlados e com autorização prévia, para fins puramente acadêmicos e de pesquisa em Segurança da Informação.*