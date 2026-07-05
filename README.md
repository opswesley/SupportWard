# 🛠️ Ward Toolkit - Ferramenta de Suporte Técnico

![Version](https://img.shields.io/badge/Versão-0.02a%20(ALPHA)-orange)
![OS](https://img.shields.io/badge/Sistema-Windows%2010%20%7C%2011-blue)
![Format](https://img.shields.io/badge/Formato-Executável%20(.exe)-green)
![License](https://img.shields.io/badge/Licença-Freeware%20(Todos%20os%20Direitos%20Reservados)-lightgrey)

> ⚠️ **AVISO IMPORTANTE: FASE ALPHA (v0.02a)**
> Esta ferramenta está em fase **ALPHA**. Embora tenha sido testada em ambientes controlados (VMs, Desktops e Notebooks), ela está sujeita a comportamentos inesperados. 
> 🚨 **É ALTAMENTE RECOMENDÁVEL criar um Ponto de Restauração do Sistema** antes de utilizar qualquer função relacionada a otimizações, debloat ou remoção de ferramentas nativas. **Use por sua conta e risco!**

---

## 📖 Sobre o Projeto

O **Ward Toolkit** (nossa suíte avançada de Suporte Técnico) é uma ferramenta extremamente leve e robusta desenvolvida para automatizar, centralizar e acelerar rotinas de suporte técnico, análise de sistemas, troubleshooting e otimização no Windows 10 e 11. 

Criada inicialmente para uso corporativo com o objetivo de economizar horas de digitação de comandos manuais e navegação por painéis de controle, decidi disponibilizá-la gratuitamente para agregar valor à comunidade técnica. A ferramenta atua como um "canivete suíço", integrando desde a leitura profunda de SMART de discos e decodificação de fabricantes de RAM, até a aplicação de perfis de otimização de registro com **snapshot de rollback automático**.

---

## 🚀 Funcionalidades Principais

### 🩺 Diagnóstico e Análise Avançada
* **Dashboard em Tempo Real:** Visão geral de CPU, RAM, GPU, Disco, Bateria e Rede.
* **Análise Completa e Rápida:** Varredura inteligente que gera um **Plano de Ação** com recomendações práticas baseadas nos problemas encontrados.
* **SMART Detalhado:** Leitura de temperatura, horas ligadas, erros de leitura/escrita e desgaste (SSD) via `Get-StorageReliabilityCounter`.
* **Histórico de BSOD e Crashes:** Análise de Minidumps e códigos de BugCheck com um banco de dados embutido que traduz o código em **Causa Provável** e **Solução Sugerida**.
* **Monitor de Confiabilidade (WMI):** Extração e classificação de eventos (Crítico/Aviso/Informativo) sem depender do `perfmon`.
* **Relatório HTML Profissional:** Gera um relatório visual (tema dark) com todas as informações do sistema, plano de ação e logs, pronto para enviar ao cliente ou equipe L2/L3.
* **Pacote de Logs (ZIP):** Exporta um bundle completo com eventos, drivers, rede, Defender e minidumps para análise offline.

### 🛠️ Solução de Problemas (Troubleshooting)
* **Solucionador Automático:** Roda uma bateria de testes e oferece correções com "um clique" (ex: limpar disco, liberar RAM, resetar DNS, reativar Defender).
* **Ferramentas de Rede:** Teste de velocidade adaptativo (Cloudflare/Hetzner/MS), Traceroute, flush/renew IP, troca rápida de DNS e reset de Winsock.
* **Reparos Rápidos:** Reset profundo do Windows Update, reparo de fila de impressão (Spooler), correção de erros MSI (2502/2503) e reparo de WMI.
* **Integridade do Sistema:** Executa `DISM` e `SFC /scannow` com resumo inteligente do `CBS.log`.

### 🚀 Otimização e Performance
* **Perfis de Otimização com Rollback:** Aplica perfis (Extremo/Gaming, Equilibrado, Notebook) salvando um **Snapshot JSON do Registro** antes da alteração, permitindo restauração exata.
* **Debloat do Windows:** Remoção segura de Bloatwares (Xbox, Cortana, Clipchamp, Teams, Apps de Mídia).
* **Privacidade e Telemetria:** Desativa Copilot, Recall, Widgets, Web Search, Delivery Optimization e Sleep Study.
* **Modo Turbo:** Liberação agressiva de RAM (Working Set Trim), desativação do Algoritmo de Nagle (reduz latência/ping), Core Parking e otimização de Pagefile.
* **Benchmark Integrado:** Testes de CPU (Single/Multi-thread), RAM e Disco (Sequencial e 4K IOPS) para comparar antes/depois das otimizações.

### 💻 Hardware e Informações Detalhadas
* **Decodificação de RAM:** Identifica o fabricante real da memória (Kingston, Corsair, Samsung, etc.) lendo o *Part Number*, contornando falhas da BIOS.
* **Detecção de GPU e VRAM:** Lê o registro para descobrir a VRAM real, contornando erros de formatação do WMI.
* **Status de Bateria:** Saúde real da bateria (capacidade de fábrica vs. atual) para notebooks.
* **Informações de Firmware:** TPM, Secure Boot, Partição (GPT/MBR) e Ativação do Windows.

### 📦 Gerenciamento de Software (WinGet)
* Instalação de pacotes essenciais (Navegadores, 7-Zip, VLC, Sysinternals).
* Atualização em massa de todos os programas instalados.
* Busca, instalação e desinstalação limpa via repositório do WinGet.

---

## ⚙️ Como Usar e Instalação

A ferramenta foi compilada para um **Executável (.exe)** com ícone personalizado. Você **NÃO** precisa alterar políticas de execução do PowerShell, compilar código ou instalar dependências.

1. Vá até a aba **[Releases](https://github.com/opswesley/SupportWard/releases)** deste repositório.
2. Baixe o arquivo `.exe` (ou o `.zip` contendo ele).
3. **Clique com o botão direito** no arquivo e selecione **"Executar como Administrador"** (Obrigatório para alterações de sistema).
4. A interface de console (TUI) será carregada. Use as **Setas do Teclado** para navegar, **Enter** para selecionar e **ESC** para voltar.

---

## 🗺️ Roadmap (Futuras Atualizações)

A ferramenta é um projeto vivo. Pretendo manter atualizações de correção e estabilidade conforme novos cenários forem encontrados no dia a dia.
* [ ] **Interface Gráfica (GUI):** Migrar do console (CMD/PowerShell) para uma interface moderna e amigável.
* [ ] **Internacionalização:** Criar seletor de idioma (Português / Inglês).
* [ ] **Módulo de Backup/Restore:** Integração com imagens de disco e backup de perfis de rede.
* [ ] **Correções Contínuas:** Ajustes finos baseados no feedback da comunidade e testes em mais hardwares.

---

## ⚖️ Licença e Distribuição

Esta ferramenta é **FREWARE** (Gratuita para uso pessoal e profissional). 

**Todos os Direitos Reservados (All Rights Reserved) - Não é Open Source.**
* ✅ Você **PODE**: Baixar, usar e distribuir o arquivo `.exe` compilado livremente para clientes, amigos e empresas.
* ❌ Você **NÃO PODE**: Copiar o código-fonte, modificar, criar obras derivadas, ou redistribuir o código-fonte/compilado como parte de outro projeto proprietário ou open-source sem autorização expressa do autor.

---

## 🐛 Reportar Problemas

Encontrou um bug? O sistema travou em uma função específica?
Você pode reportar diretamente pela aba de **[Issues](https://github.com/opswesley/SupportWard/issues)** deste repositório no GitHub!

Por favor, detalhe:
1. A versão da ferramenta (v0.02a).
2. O Windows (10 ou 11) e a build.
3. O passo a passo do que causou o erro.
4. **Importante:** Anexe o `Relatorio_HTML` ou o `Pacote de Logs` gerado pela própria ferramenta (Menu > Utilitários / Gerar Relatório). Isso acelera muito a identificação do problema!

💬 *Prefere um suporte mais rápido ou tirar dúvidas? Entre no meu **[Discord](https://discord.gg/K3wMa8Dqsg)**!*

---

## 💬 Autor

Desenvolvido com ☕ e muita linha de código por **opswesley**.
* [GitHub](https://github.com/opswesley)
* [Discord](https://discord.gg/K3wMa8Dqsg) *(Comunidade, feedback e suporte)*

> *O tempo é o recurso mais valioso de um técnico de TI. Esta ferramenta foi criada para devolver esse tempo a você.*
