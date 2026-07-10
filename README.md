# 🛠️ Ward Toolkit - Ferramenta de Suporte Técnico

![Version](https://img.shields.io/badge/Versão-0.03a%20(ALPHA)-orange)
![OS](https://img.shields.io/badge/Sistema-Windows%2011-blue)
![Format](https://img.shields.io/badge/Formato-Executável%20(.exe)-green)
![Origem](https://img.shields.io/badge/Fonte-Script%20.PS1%20compilado-informational)
![License](https://img.shields.io/badge/Licença-Freeware%20(Todos%20os%20Direitos%20Reservados)-lightgrey)

> ⚠️ **AVISO IMPORTANTE: FASE ALPHA (v0.03a)**
> Esta ferramenta está em fase **ALPHA**. Embora tenha sido testada em ambientes controlados (VMs, Desktops e Notebooks), ela está sujeita a comportamentos inesperados.
> 🚨 **É ALTAMENTE RECOMENDÁVEL criar um Ponto de Restauração do Sistema** antes de utilizar qualquer função relacionada a otimizações, debloat ou remoção de ferramentas nativas. **Use por sua conta e risco!**

> 🖥️ **A partir da v0.03, a ferramenta requer Windows 11 (build 22000 ou superior).** O suporte a Windows 10 foi removido — se o build detectado for inferior a 22000, a ferramenta exibe um aviso claro e encerra a execução em vez de tentar seguir em frente e falhar de forma confusa no meio do uso.

---

## 📖 Sobre o Projeto

O **Ward Toolkit** (nossa suíte avançada de Suporte Técnico) é uma ferramenta extremamente leve e robusta desenvolvida para automatizar, centralizar e acelerar rotinas de suporte técnico, análise de sistemas, troubleshooting e otimização no Windows 11.

Criada inicialmente para uso corporativo com o objetivo de economizar horas de digitação de comandos manuais e navegação por painéis de controle, decidi disponibilizá-la gratuitamente para agregar valor à comunidade técnica. A ferramenta atua como um "canivete suíço", integrando desde a leitura profunda de SMART de discos e decodificação de fabricantes de RAM, até a aplicação de perfis de otimização de registro com **snapshot de rollback automático**, testes de estresse de CPU/RAM/Disco/GPU, e um solucionador automático de problemas.

---

## 📸 Capturas de Tela

<div align="center">

### 🖥️ Dashboard em 3 dispositivos diferentes

<table>
  <tr>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/e3bdfe84-81d8-450d-987e-7ea649514f5f" alt="Dashboard - Dispositivo 1" width="100%"/></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/ef70970c-8b20-4d4c-bc76-be9fc1a15045" alt="Dashboard - Dispositivo 2" width="100%"/></td>
    <td align="center" width="33%"><img src="https://github.com/user-attachments/assets/d3eca2db-9878-49d3-a4d8-e7843f4302c2" alt="Dashboard - Dispositivo 3" width="100%"/></td>
  </tr>
  <tr>
    <td align="center"><sub>Dispositivo 1</sub></td>
    <td align="center"><sub>Dispositivo 2</sub></td>
    <td align="center"><sub>Dispositivo 3</sub></td>
  </tr>
</table>

### ⚠️ Bloqueio de Compatibilidade (Windows 10)

<img src="https://github.com/user-attachments/assets/77c36839-5a9d-4a8a-83b5-cfc4967db1ec" alt="Erro de incompatibilidade com Windows 10" width="80%"/>

<sub>A ferramenta detecta o build do sistema e encerra com uma mensagem clara em vez de seguir em frente e falhar de forma confusa.</sub>

<br><br>

<table>
  <tr>
    <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/1b37c3de-2a56-4371-be27-50d83c3a2ecc" alt="Ações Recomendadas para seu PC" width="100%"/>
      <br><sub><b>Ações Recomendadas para seu PC</b></sub>
    </td>
    <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/efe6ef2b-aa75-42b3-99e3-a8f4a170ead8" alt="Teste de Estresse" width="100%"/>
      <br><sub><b>Teste de Estresse</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/3f641f6f-30dc-4d33-bcf6-c13612195053" alt="Resultado do Benchmark" width="100%"/>
      <br><sub><b>Resultado do Benchmark</b></sub>
    </td>
    <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/4b58e69a-b118-42d5-bffc-813a94548186" alt="Limpeza de Memória RAM" width="100%"/>
      <br><sub><b>Liberar Memória RAM Agora</b></sub>
    </td>
  </tr>
</table>

### 📄 Relatório HTML (Demonstração)

<img src="https://github.com/user-attachments/assets/4ba28de5-c649-4ae1-9fb8-a64ed447936c" alt="Demonstração do Relatório HTML" width="90%"/>

<sub>Relatório visual completo (tema dark), gerado pela própria ferramenta.</sub>

</div>

---

O código-fonte é um script **PowerShell (.ps1)**, sempre **compilado para `.exe`** (via `ps2exe`, com ícone personalizado) antes da distribuição — o usuário final não precisa alterar políticas de execução do PowerShell, instalar dependências ou tocar em linha de comando.

---

## 🚀 Funcionalidades Principais (Visão Geral)

### 🩺 Diagnóstico e Análise Avançada
* **Dashboard em Tempo Real:** Visão geral de CPU, RAM, GPU, Disco, Bateria, Rede e status de administrador — com redesenho por ANSI (sem "flicker" a cada tecla).
* **Ações Recomendadas para seu PC:** varredura de ~30s–2min (disco, RAM, drivers, updates, Defender, SMART, mini-benchmark de CPU) que sugere e **aplica** ações automaticamente, registrando o resultado (ex.: RAM antes/depois) no relatório HTML.
* **Solucionador de Problemas Automático:** roda uma bateria de testes e resolve problemas comuns sozinho.
* **Diagnóstico Rápido e Análise Completa:** varreduras que terminam em um **Plano de Ação** com recomendações práticas.
* **SMART Detalhado:** temperatura, horas ligadas, ciclos liga/desliga, erros de leitura/escrita e desgaste (SSD) via `Get-StorageReliabilityCounter`, com **fallback via contadores ATA brutos** para discos SATA/AHCI antigos.
* **Histórico de BSOD e Crashes:** análise de Minidumps e códigos de BugCheck com banco de dados embutido (Causa Provável + Solução Sugerida), base bastante ampliada na v0.03.
* **Monitor de Confiabilidade (WMI):** eventos classificados em Crítico/Aviso/Informativo com Índice de Estabilidade, sem depender do `perfmon`.
* **Relatório HTML Profissional:** tema dark, com plano de ação, tabela de módulos de RAM, SMART completo e logs — pronto para enviar ao cliente ou equipe L2/L3.
* **Pacote de Logs (ZIP) / Pacote de Diagnóstico Completo:** exporta bundle com eventos, drivers, rede, Defender, processos e minidumps para análise offline.

### 🌡️ Benchmark e Testes de Estresse (NOVO na v0.03a)
* **Benchmark Rápido:** CPU single-thread + disco sequencial (~15–30s).
* **Benchmark Completo:** CPU multi-thread (todos os núcleos), banda de memória RAM, disco sequencial de 1 GB e I/O aleatório 4K/IOPS (~1–2 min).
* **Testes de Estresse com intensidade selecionável (50%/70%/100%):** CPU, RAM, Disco (HD/SSD/NVMe), GPU/Gráficos e um **Teste Geral** (~5 min, todos juntos).

### 🛠️ Solução de Problemas (Troubleshooting)
* **Ferramentas de Rede:** teste de velocidade adaptativo (Cloudflare/Hetzner/MS), Traceroute, flush/renew IP, troca rápida de DNS (por categoria: Velocidade, Jogos, Privacidade), reset de Winsock, teste de DNS atual + comparação entre provedores.
* **Reparos Rápidos:** reset profundo do Windows Update, reparo de fila de impressão (Spooler), correção de erros MSI (2502/2503), reparo de WMI.
* **Integridade do Sistema:** `DISM` e `SFC /scannow` com resumo inteligente do `CBS.log`.

### 🚀 Otimização e Performance
* **Perfis de Otimização com Rollback:** Extremo/Gaming, Equilibrado, Notebook — salvando um **Snapshot JSON do Registro** antes da alteração, permitindo restauração exata.
* **Debloat do Windows:** remoção segura de Bloatwares (Xbox, Cortana, Clipchamp, Teams, Apps de Mídia, jogos pré-instalados).
* **Privacidade e Telemetria:** Copilot, Recall, Widgets, Web Search, Delivery Optimization, Background Apps e Sleep Study.
* **Modo Turbo:** liberação agressiva de RAM (Working Set Trim), desativação do Algoritmo de Nagle, Core Parking, otimização de Pagefile, priorização de processos.
* **BitLocker:** ativar, desativar permanentemente, pausar e retomar a proteção — direto no menu principal.

### 💻 Hardware e Informações Detalhadas
* **Decodificação de RAM:** identifica o fabricante real (Kingston, Corsair, Samsung, Crucial, G.Skill, SK Hynix, Micron, ADATA, Patriot, Team Group etc.) lendo o *Part Number*, contornando falhas da BIOS.
* **Detecção de GPU e VRAM:** lê o registro para VRAM real, contornando erros de formatação do WMI.
* **Status de Bateria:** saúde real (capacidade de fábrica vs. atual) para notebooks.
* **Firmware:** TPM, Secure Boot, estilo de partição (GPT/MBR), Ativação do Windows.
* **Busca de Atualizações de Drivers:** consulta o Windows Update via API COM nativa, sem ferramenta de terceiros.

### 📦 Gerenciamento de Software (WinGet)
* Instalação de pacotes essenciais (Navegadores, Utilitários, Ferramentas de Sistema, Comunicação).
* Atualização em massa de todos os programas instalados.
* Busca, instalação (direto da lista de resultados) e desinstalação limpa via repositório do WinGet.

---

## ⚙️ Como Usar e Instalação

A ferramenta é distribuída como **Executável (.exe)** com ícone personalizado (compilada a partir do `.ps1`). Você **NÃO** precisa alterar políticas de execução do PowerShell, compilar código ou instalar dependências.

1. Vá até a aba **[Releases](https://github.com/opswesley/SupportWard/releases)** deste repositório.
2. Baixe o arquivo `.exe` (ou o `.zip` contendo ele).
3. **Clique com o botão direito** no arquivo e selecione **"Executar como Administrador"** (Obrigatório — o script tem `#Requires -RunAsAdministrator`).
4. A interface de console (TUI) será carregada. Use as **Setas do Teclado** para navegar, **Enter** para selecionar e **ESC** para voltar/sair.

---

## 🗺️ Mapa Completo de Menus (Hierarquia da Ferramenta)

A partir da v0.03, o menu principal foi **reorganizado de 22 para 12 categorias** (9 "Hubs" numerados + BitLocker + Configurações + Ações Recomendadas), já que itens de otimização/privacidade estavam espalhados sem relação clara entre si. Abaixo está a árvore completa — todo item marcado com `[Menu]` abre um submenu; os demais executam a ação diretamente.

```
🏠 MENU PRINCIPAL (Dashboard)
│
├── 1. Diagnóstico e Solução de Problemas [Menu]
│   ├── Solucionador de Problemas (Automático) — detecta e resolve sozinho
│   ├── Diagnóstico Rápido
│   ├── Análise Completa do Sistema
│   ├── Solução de Problemas (Manual) [Menu]
│   │   ├── Áudio – Testar som / Solucionador
│   │   ├── Áudio – Reiniciar serviço de áudio
│   │   ├── Rede – Solucionador de problemas
│   │   ├── Rede – Redefinir adaptadores
│   │   ├── Wi-Fi – Exportar perfis salvos (senhas em XML)
│   │   ├── Impressão – Limpar fila
│   │   ├── Windows Update – Reset profundo
│   │   ├── Reiniciar Windows Explorer
│   │   ├── Reparar Erros 2502/2503 (permissões da pasta TEMP)
│   │   └── Microsoft Teams – Limpar cache
│   └── Diagnóstico de Falhas (BSOD/Vírus/Logs) [Menu]
│       ├── Histórico de BSOD / Desligamentos
│       ├── Arquivos de Minidump
│       ├── Configurar Dump de Memória Automático (Completo / Kernel / Minidump)
│       ├── Monitor de Confiabilidade (WMI ou nativo)
│       ├── Eventos Críticos Recentes
│       ├── Buscar Palavra-Chave nos Logs (últimos 7 dias)
│       ├── Status do Windows Defender
│       ├── Executar Scan do Defender (Rápido/Completo/Atualizar Definições)
│       ├── Ameaças Detectadas (Histórico)
│       ├── Processos Suspeitos (sem assinatura, rodando de pastas temp)
│       ├── Verificar Persistência (Autostart)
│       ├── Conexões de Rede por Processo
│       ├── Verificar Arquivo Hosts (sequestro de DNS)
│       ├── SMART Detalhado dos Discos
│       ├── Verificação de Integridade (SFC/DISM)
│       ├── Benchmark (Rápido ou Completo)
│       ├── Histórico de Sessões desta Ferramenta
│       └── Exportar Pacote de Diagnóstico Completo (.zip)
│
├── 2. Otimização e Desempenho [Menu]
│   ├── Perfis de Otimização Automática [Menu]
│   │   ├── Perfil Extremo (Gaming / FPS Máximo)
│   │   ├── Perfil Equilibrado (Uso Diário / Trabalho)
│   │   ├── Perfil Notebook (Bateria / Mobilidade)
│   │   └── Restaurar Padrões do Windows
│   ├── Modo Alta Performance
│   ├── Modo Jogo (Gaming)
│   ├── Liberar Memória RAM Agora
│   ├── Desativar / Ativar SuperFetch (SysMain)
│   ├── Desativar / Ativar NVIDIA Container
│   ├── Limpeza Geral (temp, cache, DNS, lixeira, navegadores)
│   ├── Limpeza Avançada (VSS/WinSxS) [Menu]
│   │   ├── Limpar Cópias de Sombra (VSS)
│   │   ├── Limpar WinSxS (Component Store)
│   │   └── Analisar Pastas Grandes (top 15 do perfil)
│   ├── Ajustes Avançados de Desempenho [Menu]
│   │   ├── Desativar Efeitos Visuais
│   │   ├── Desativar Transparências
│   │   ├── Desativar Histórico do Clipboard
│   │   ├── Desativar Descoberta Automática de Pastas
│   │   └── Ativar Mensagens de Status Detalhadas
│   ├── Otimizações Avançadas (Diversas) [Menu]
│   │   ├── Otimizar NTFS (desativa 8.3 e Last Access)
│   │   ├── Gerenciar Indexação de Busca [Menu]
│   │   │   ├── Desativar Indexação
│   │   │   ├── Ativar Indexação (Automático)
│   │   │   └── Indexação Manual
│   │   ├── Desativar Notificações de Dicas
│   │   ├── Desativar Advertising ID
│   │   ├── Desativar Telemetria do Office
│   │   ├── Desativar Telemetria do .NET
│   │   └── Modo Safe Mode [Menu]
│   │       ├── Sair do Safe Mode
│   │       ├── Safe Mode Normal
│   │       └── Safe Mode com Rede
│   ├── Otimização Avançada (Turbo) [Menu]
│   │   ├── [Turbo] MODO TURBO COMPLETO (aplica tudo abaixo)
│   │   ├── Liberar Memória RAM Agora
│   │   ├── Gerenciador de Processos (Top RAM)
│   │   ├── Desativar / Reativar Algoritmo de Nagle
│   │   ├── Otimizar Arquivo de Paginação
│   │   ├── Otimizar Discos (TRIM SSD / Desfrag HD)
│   │   ├── Desativar Core Parking
│   │   ├── Priorizar Programas em Primeiro Plano
│   │   └── Priorizar Serviços em Segundo Plano
│   └── Perfis de Energia [Menu]
│       ├── Economia de Energia
│       ├── Equilibrado (Padrão Windows)
│       ├── Alto Desempenho
│       ├── Desempenho Máximo (Ultimate)
│       ├── Silencioso / Limitar CPU (%)
│       └── Remover Limite de CPU
│
├── 3. Segurança e Privacidade [Menu]
│   ├── Segurança e Análise Avançada [Menu]
│   │   ├── Conexões Ativas (Netstat + PID)
│   │   ├── Tarefas Agendadas Recentes (últimos 7 dias)
│   │   ├── Usuários Administradores (via SID S-1-5-32-544)
│   │   ├── Verificar UAC
│   │   ├── Status do Windows Defender
│   │   ├── Scan Rápido com Defender
│   │   └── Configurar Mitigações de Segurança [Menu]
│   │       ├── Desativar Todas as Mitigações
│   │       ├── Restaurar Mitigações Padrão
│   │       ├── Desativar Fault Tolerant Heap
│   │       └── Reativar Fault Tolerant Heap
│   └── Privacidade e Telemetria [Menu]
│       ├── Microsoft Copilot [Menu] (Ativar/Desativar)
│       ├── Windows Recall [Menu] (Ativar/Desativar)
│       ├── Widgets (Notícias) [Menu] (Ativar/Desativar)
│       ├── Web Search no Menu Iniciar [Menu] (Ativar/Desativar)
│       ├── Delivery Optimization [Menu] (Ativar/Desativar)
│       ├── Background Apps [Menu] (Ativar/Desativar)
│       ├── Sleep Study [Menu] (Ativar/Desativar)
│       ├── Security Health Tray [Menu] (Remover/Adicionar da inicialização)
│       ├── Hibernação [Menu] (Ativar/Desativar)
│       ├── Desativar Power Saving (dispositivos)
│       └── Desativar / Ativar Game Bar / FSO
│
├── 4. Hardware e Rede [Menu]
│   ├── Hardware e SMART [Menu]
│   │   ├── SMART dos Discos
│   │   ├── Informações de RAM (slots + fabricante)
│   │   ├── Informações de GPU (VRAM real)
│   │   ├── Teste de Memória RAM (agenda para próximo boot)
│   │   ├── Relatório de Energia (60s)
│   │   ├── Número de Série e Garantia
│   │   └── Buscar Atualizações de Drivers
│   ├── Ferramentas de Rede [Menu]
│   │   ├── Teste de Conectividade
│   │   ├── Traceroute
│   │   ├── Teste de Velocidade (LAN + Internet)
│   │   ├── Renovar IP e Limpar DNS
│   │   ├── Resetar Pilha de Rede (Winsock)
│   │   ├── Trocar DNS [Menu]
│   │   │   ├── Testar DNS Atual
│   │   │   ├── Comparar Todos os DNS
│   │   │   ├── — Velocidade — (Cloudflare, Google)
│   │   │   ├── — Jogos — (Cloudflare Gaming, Google Gaming, Level3)
│   │   │   ├── — Privacidade/Segurança — (Quad9, OpenDNS, AdGuard)
│   │   │   └── Voltar para DHCP
│   │   ├── Teste de DNS (atual + comparar provedores)
│   │   ├── Reset do Firewall
│   │   └── Verificar Conflito de IP
│   └── Rede e Compartilhamento [Menu]
│       ├── Ativar / Desativar Compartilhamento de Arquivos
│       └── Ativar / Desativar Descoberta de Rede
│
├── 5. Configurações do Explorer [Menu]
│   ├── Compact View (Ativar/Desativar) — Windows 11
│   ├── Snap Assist (Ativar/Desativar)
│   ├── Show Type Overlay
│   ├── Remover Texto de Atalho ("Atalho para")
│   └── Menu de Contexto Clássico / Moderno (Windows 11)
│
├── 6. Gerenciar Programas [Menu]
│   ├── Atualizar Todos os Programas (WinGet)
│   ├── Instalar Programas Essenciais [Menu]
│   │   ├── Navegadores: Chrome, Firefox, Brave
│   │   ├── Utilitários: 7-Zip, VLC, Notepad++, WinSCP
│   │   ├── Ferramentas de Sistema: Process Explorer, CPU-Z, HWiNFO
│   │   └── Comunicação: Zoom, Teams, Discord
│   ├── Remover Bloatware do Windows [Menu]
│   │   ├── Remover Apps Xbox
│   │   ├── Remover Apps de Mídia
│   │   ├── Remover Apps Sociais (People, Mail, Calendar)
│   │   ├── Remover Jogos Pré-instalados
│   │   ├── Remover Clipchamp e OneNote
│   │   └── Remover Cortana
│   ├── Listar Programas Instalados
│   ├── Procurar e Instalar Programa (busca WinGet direto)
│   └── Desinstalar Programa
│
├── 7. Reparação e Recuperação [Menu]
│   ├── Reparo Completo (DISM + SFC + CHKDSK)
│   ├── Verificar Imagem (DISM Scan)
│   ├── Restaurar Imagem (DISM Restore)
│   ├── Verificar Arquivos (SFC)
│   ├── Verificar Disco (CHKDSK)
│   ├── Reparar Repositório WMI
│   ├── Reparar Apps UWP
│   ├── Reparar Microsoft Store
│   ├── Criar Ponto de Restauração
│   ├── Restauração do Sistema (GUI)
│   └── Reiniciar para WinRE
│
├── 8. Utilitários e Relatórios [Menu]
│   ├── Utilitários [Menu]
│   │   ├── Backup Rápido de Perfil (Desktop, Docs, Imagens, Favoritos)
│   │   ├── Gerar Pacote de Logs (.zip para chamado de suporte)
│   │   ├── Listar Usuários Locais
│   │   ├── Reparar Relação de Confiança (AD)
│   │   ├── Forçar GPO e Sincronizar Horário
│   │   └── Exportar Softwares Instalados (CSV)
│   ├── Informações Detalhadas (specs completas do sistema)
│   ├── Gerar Relatório HTML
│   └── Ferramentas Extras / Backup de Configuração [Menu]
│       ├── Programas na Inicialização
│       ├── Saúde de Tarefas Agendadas
│       ├── Saúde de Drivers (desinstalação em lote + rescan automático)
│       ├── Status do BitLocker
│       ├── Status do Firewall
│       ├── Reparar Spooler de Impressão
│       ├── Resetar Windows Update
│       └── Snapshots de Configuração (Rollback)
│
├── 9. Benchmark e Testes de Estresse [Menu]
│   ├── Benchmark Rápido (CPU single-thread + Disco sequencial)
│   ├── Benchmark Completo (CPU multi-thread + RAM + Disco seq. e 4K)
│   └── Testes de Estresse [Menu] (valida estabilidade sob carga)
│       ├── Estresse de CPU [Menu: 50% / 70% / 100%]
│       ├── Estresse de Memória RAM [Menu: 50% / 70% / 100%]
│       ├── Estresse de Disco (HD/SSD/NVMe) [Menu: 50% / 70% / 100%]
│       ├── Estresse de GPU / Gráficos [Menu: 50% / 70% / 100%]
│       └── Teste Geral (CPU+RAM+Disco+GPU, ~5 min, intensidade fixa)
│
├── 10. BitLocker (Ativar/Desativar/Pausar) — direto no menu principal
│   ├── Desativar BitLocker Permanentemente (recomendado p/ desempenho)
│   ├── Pausar Proteção (temporário, sem descriptografar)
│   ├── Retomar Proteção (despausar)
│   └── Ativar BitLocker
│
├── 11. Configurações da Ferramenta [Menu]
│   ├── Configurações do Windows / Painel de Controle / Editor do Registro
│   ├── Políticas de Grupo / Gerenciador de Dispositivos / Gerenciador de Tarefas
│   ├── Visualizador de Eventos / Serviços
│   ├── Prompt (Admin) / PowerShell (Admin)
│   └── Configurações da Ferramenta (log, etc.) [Menu]
│       ├── Log de Auditoria (.txt) — liga/desliga (grava em ProgramData)
│       ├── Abrir pasta de logs desta ferramenta
│       └── Abrir pasta de histórico de sessões
│
└── 12. Ações Recomendadas para seu PC — varredura + aplicação automática
```

> 💡 **Dica de navegação:** todo item com `[Menu]` no nome abre uma nova tela; os demais executam a ação assim que você aperta **Enter**. Use **ESC** a qualquer momento para voltar um nível.

---

## 🆕 O Que Mudou na v0.02a / v0.03a (Notas de Manutenção Completas)

### v0.03a — Patch de correções + novas funções
* **[CORRIGIDO]** Erro *"Não é possível excluir uma árvore de subchave..."* durante o Perfil Extremo — bug do provedor de registro do PowerShell com `Remove-Item -Recurse` (disparava mesmo quando a exclusão era concluída com sucesso). `Remove-RegKeySafe` agora usa `reg.exe`, que não sofre desse problema.
* **[CORRIGIDO]** Ao voltar nos menus, a tela ficava com "restos visuais" do item anterior. A causa era a sequência de escape `\e[0J`, que só funciona em PowerShell 7+; no Windows PowerShell 5.1 (usado pela maioria dos `.exe` gerados via `ps2exe`) aparecia como texto literal. Trocado por `[char]27` (ESC de verdade), funcionando em ambas as versões.
* **[NOVO]** "Liberar Memória RAM Agora" voltou a aparecer solta no menu de Otimização e Desempenho (antes só existia dentro do Turbo).
* **[NOVO]** Testes de Estresse (Benchmark > Testes de Estresse): CPU, RAM, Disco, GPU/Gráficos e um Teste Geral (~5 min, tudo junto). CPU/RAM/Disco/GPU têm intensidade selecionável (50%/70%/100%); o Geral roda fixo.
* **[NOVO]** "Ações Recomendadas para seu PC" no menu principal — varredura de ~30s–2min (disco, RAM, drivers, updates, Defender, SMART, mini-benchmark de CPU) que sugere e aplica ações, registrando o resultado no relatório HTML.
* **[NOVO]** Controle de BitLocker no menu principal — ativar, desativar permanentemente (marcado como recomendado para máquinas gamer/otimização), pausar e retomar a proteção.
* **[CORRIGIDO]** "Desempenho Máximo (Ultimate)" sempre reportava "não suportado" mesmo em Windows compatíveis, porque o código comparava com o GUID de origem do template e `/duplicatescheme` sempre cria um GUID novo. Agora o GUID novo é capturado e usado.
* **[NOVO]** Teste de DNS atual (mede o DNS realmente configurado no adaptador, não só o 1.1.1.1 fixo) e comparação entre provedores. Menu "Trocar DNS" ganhou mais opções (AdGuard, Level3) organizadas por categoria (Velocidade/Jogos/Privacidade).
* **[MELHORADO]** Submenus agora têm a tag `[Menu]` no nome para diferenciar de ações diretas.
* **[NOVO]** Atalho para abrir a página de drivers do fabricante da GPU/placa-mãe detectada (não baixa/instala nada, só evita procurar manualmente qual site é o certo).

### v0.03 — Exigência de Windows 11 + correções de campo
* **[REMOVIDO]** Suporte a Windows 10: a ferramenta agora assume Windows 11 e falha rápido com mensagem clara em build anterior a 22000.
* **[CORRIGIDO]** "Perfil Extremo"/"Restaurar Padrões" podiam derrubar a ferramenta com *"não é possível excluir uma árvore de subchave porque a subchave não existe"*. Toda remoção de chave/valor de registro agora passa por `Remove-RegKeySafe`/`Remove-RegValueSafe` (`Test-Path` + try/catch de verdade).
* **[CORRIGIDO]** "Desativar Mitigações" fechava o script inteiro com *"Error this script must be run on Windows 10 or greater."* — erro do próprio módulo `ProcessMitigation` do Windows, lançado como exceção. Agora em try/catch.
* **[CORRIGIDO]** "Fault Tolerant Heap" agora tem opção de **reativar** (antes só desativava).
* **[CORRIGIDO]** "Membros do grupo Administradores" falhava com "Erro de sistema 1376" em Windows não-inglês (nome do grupo varia por idioma). Agora usa o SID universal `S-1-5-32-544`.
* **[CORRIGIDO]** Saída de "Limpeza Avançada (VSS/WinSxS)" e "Forçar GPO" com acentos quebrados — bug conhecido do console legado do Windows com `chcp 65001` e escrita direta de `dism.exe`/`gpupdate.exe`. Agora passa pelo pipeline do PowerShell (`Invoke-LegacyConsoleTool`).
* **[CORRIGIDO]** "Gerar Pacote de Logs" mostrava erro de `powercfg /batteryreport` em desktops sem bateria. Agora verifica se é notebook antes de tentar.
* **[CORRIGIDO]** Detecção de "dispositivo com problema" usava `Status -eq 'Unknown'` (falso-positivo em hardware saudável). Unificado em `Get-ProblemDevices` (`Win32_PNPEntity` + `ConfigManagerErrorCode <> 0`).
* **[CORRIGIDO]** Relatório HTML de SMART não mostrava "Ciclos Liga/Desliga" e "Desgaste (SSD)".
* **[MELHORADO]** SMART com fallback via contadores ATA brutos (`MSStorageDriver_FailurePredictData`) para preencher Horas Ligado/Ciclos em discos SATA/AHCI antigos.
* **[MELHORADO]** Base de diagnóstico de BugCheck (BSOD) bastante ampliada.
* **[NOVO]** "Buscar Atualizações de Drivers" via API COM do Windows Update, sem ferramenta de terceiros.
* **[REORGANIZADO]** Menu principal reduzido de 22 para 9 categorias lógicas (hoje 12, com BitLocker/Configurações/Ações Recomendadas adicionados depois).
* **[NOVO]** "Saúde de Drivers" agora permite desinstalar dispositivos com problema **em lote**, dispara `pnputil /scan-devices` automaticamente após, e mostra quantos problemas restaram.

---

## 📜 Histórico Completo de Versões

### v0.02 — Patch de correções (testado em VM/Win10/Win11)
* **[CORRIGIDO]** "Análise Completa do Sistema" quebrava no PowerShell 7 (`Get-WmiObject` não existe mais). Trocado por `Get-CimInstance` (compatível com PS 5.1 e 7+).
* **[CORRIGIDO]** Fabricante da RAM aparecia como "0000" quando a BIOS não preenche o SMBIOS. Nova função `Get-RamManufacturer` identifica pela marca via prefixo do Part Number (Kingston, Crucial, Corsair, G.Skill, Samsung, SK Hynix, Micron, ADATA, Patriot, Team Group etc.). Mostrado no Menu Hardware, Informações Detalhadas e Relatório HTML (nova tabela dedicada com DDR3/4/5, velocidade nominal x configurada e Part Number).
* **[CORRIGIDO]** Relatório HTML "estourava" a tabela de Inicialização em telas pequenas. CSS ajustado (`table-layout: fixed` + `word-break` + `overflow-wrap`).
* **[CORRIGIDO]** A ferramenta criava um log (transcript) na Área de Trabalho toda vez que abria/fechava, sem opção de desativar. Agora é **opcional** (desativado por padrão), configurável em Configurações > "Configurações da Ferramenta"; quando ativado, grava em `ProgramData\SuporteTecnico\Logs`.
* **[MELHORADO]** Benchmark ganhou duas opções: Rápido (CPU single-thread + disco sequencial) e Completo (CPU multi-thread, banda de RAM, disco sequencial de 1GB, I/O aleatório 4K/IOPS). Disponível também via `-BenchmarkCompleto`.
* **[MELHORADO]** Novos dados de diagnóstico: status de ativação do Windows, estilo de partição de cada disco (GPT/MBR), slots de RAM ocupados, alerta de RAM rodando abaixo da velocidade nominal (XMP/DOCP desativado).
* Ícones/emojis decorativos removidos (mantidos `[OK]`/`[!]`/`[X]`) para reduzir ruído visual.
* Configuração de dump de memória (BSOD) ganhou opção entre Minidump, Kernel Memory Dump ou Complete Memory Dump.
* Teste de Velocidade de Internet passou a tentar múltiplos provedores (Cloudflare, Hetzner, Microsoft) com User-Agent de navegador.
* Diagnóstico Rápido e Análise Completa passaram a terminar com um "Plano de Ação".
* Nova base de diagnóstico de BugCheck (código BSOD → causa provável → solução).
* SMART real dos discos via `Get-StorageReliabilityCounter`.
* Verificação de Integridade do Windows integrada (DISM + SFC) com resumo do CBS.log.
* Benchmark rápido de CPU e disco.
* Histórico de sessões da ferramenta (JSON em ProgramData), comparando execução atual com a anterior.
* Modo não-interativo via parâmetros de linha de comando.
* Informações Detalhadas e Relatório HTML bem mais completos (placa-mãe, TPM, Secure Boot, pagefile, monitores, USB, impressoras, histórico de updates, saúde de bateria, SMART detalhado, plano de ação, histórico de sessões, log da sessão atual).

### v0.01b
* **[CORRIGIDO]** Acentos quebrados/ícones corrompidos em logs, CSV, HTML e console — console não estava fixado em UTF-8.
* **[CORRIGIDO]** Teste de Conectividade e latência do Teste de Velocidade não mostravam "ms" — PowerShell 7+ usa a propriedade `Latency`, não `ResponseTime`. Criada `Get-PingLatency` compatível com ambas as versões.
* **[CORRIGIDO]** Teste de Velocidade agora detecta download que falhou (0 MB, "0.1s") em vez de reportar como rápido demais; fallback via `Invoke-WebRequest` se `curl.exe` não estiver disponível.
* "Procurar Programa" (WinGet) passou a permitir selecionar um item da busca e instalar direto.
* Ameaças do Defender mostram nome real da ameaça e severidade (`Get-MpThreat`).
* Monitor de Confiabilidade ganhou extração/análise via WMI (`Win32_ReliabilityRecords`) dentro da própria ferramenta, com export em CSV.
* Configuração automática de coleta de Minidump (CrashControl no registro).
* Pacote de Logs e Relatório HTML bem mais completos.

### v0.01a
* Removido `$ErrorActionPreference` global `"SilentlyContinue"` — mascarava falhas reais (registros não escritos, serviços que não paravam) e ainda reportava "OK" na tela. Cada comando agora usa `-ErrorAction` pontualmente.
* Menus passaram a usar redesenho por ANSI (sem `Clear-Host` a cada tecla) para eliminar o "flicker".
* Perfis de otimização passaram a criar snapshot de rollback em JSON antes de alterar o registro (`Save-ConfigSnapshot`).

---

## 🧩 Funções Internas de Base (Engine da Ferramenta)

Essas não aparecem como itens de menu, mas sustentam todo o funcionamento:

| Função | Responsabilidade |
|---|---|
| `Remove-RegKeySafe` / `Remove-RegValueSafe` | Remoção segura de chaves/valores de registro (Test-Path + try/catch real, via `reg.exe`) |
| `New-RegKeySafe` / `Set-RegValueSafe` | Criação/gravação segura no registro |
| `Get-ProblemDevices` | Detecção unificada de dispositivos com erro (`Win32_PNPEntity` + `ConfigManagerErrorCode`) |
| `Invoke-LegacyConsoleTool` | Executa ferramentas legadas (dism.exe, gpupdate.exe) via pipeline do PowerShell, evitando bug de acentuação |
| `Restart-ExplorerShell` | Reinício controlado do `explorer.exe` |
| `Get-ToolConfig` / `Save-ToolConfig` | Leitura/gravação das configurações da própria ferramenta |
| `Add-SessionEvent` | Registro de eventos da sessão atual (usado no Plano de Ação e Relatório HTML) |
| `Show-MenuWithArrows` | Motor de navegação por setas usado em todos os submenus |
| `Get-PingLatency` | Medição de latência compatível com PowerShell 5.1 e 7+ |
| `Get-RamManufacturerFromPartNumber` / `Get-RamManufacturer` | Decodificação do fabricante real da RAM |
| `Get-GPUInfo` | Coleta de informações de hardware (GPU e VRAM real) |
| `Get-SystemOverview` | Dados agregados exibidos no Dashboard |
| `Get-BugcheckDatabase` / `Get-BugcheckDiagnosis` | Base de causas/soluções de BSOD |
| `Save-SessionSnapshot` / `Get-SessionHistory` | Histórico de execuções da ferramenta (JSON) |
| `Get-ActionPlan` / `Get-DetectedProblems` | Geração do Plano de Ação a partir de problemas detectados |
| `Save-ConfigSnapshot` / `Restore-LatestConfigSnapshot` | Sistema de rollback via snapshot JSON do registro |
| `Export-LogPackage` / `Export-DiagnosticBundle` | Geração dos pacotes ZIP de logs/diagnóstico |
| `Export-HTMLReport` | Geração do relatório visual em HTML |

---

## ⚖️ Licença e Distribuição

Esta ferramenta é **FREEWARE** (Gratuita para uso pessoal e profissional).

**Todos os Direitos Reservados (All Rights Reserved) - Não é Open Source.**
* ✅ Você **PODE**: Baixar, usar e distribuir o arquivo `.exe` compilado livremente para clientes, amigos e empresas.
* ❌ Você **NÃO PODE**: Copiar o código-fonte, modificar, criar obras derivadas, ou redistribuir o código-fonte/compilado como parte de outro projeto proprietário ou open-source sem autorização expressa do autor.

---

## 🐛 Reportar Problemas

Encontrou um bug? O sistema travou em uma função específica?
Você pode reportar diretamente pela aba de **[Issues](https://github.com/opswesley/SupportWard/issues)** deste repositório no GitHub!

Por favor, detalhe:
1. A versão da ferramenta (v0.03a).
2. O Windows (build) — lembrando que a partir da v0.03 apenas Windows 11 é suportado.
3. O passo a passo do que causou o erro.
4. **Importante:** Anexe o `Relatorio_HTML` ou o `Pacote de Logs` gerado pela própria ferramenta (Menu Utilitários > Gerar Relatório / Gerar Pacote de Logs). Isso acelera muito a identificação do problema!

💬 *Prefere um suporte mais rápido ou tirar dúvidas? Entre no meu **[Discord](https://discord.gg/K3wMa8Dqsg)**!*

---

## 🗺️ Roadmap (Futuras Atualizações)

A ferramenta é um projeto vivo. Pretendo manter atualizações de correção e estabilidade conforme novos cenários forem encontrados no dia a dia.
* [ ] **Interface Gráfica (GUI):** migrar do console (CMD/PowerShell) para uma interface moderna e amigável.
* [ ] **Internacionalização:** seletor de idioma (Português / Inglês).
* [ ] **Módulo de Backup/Restore:** integração com imagens de disco e backup de perfis de rede.
* [ ] **Correções Contínuas:** ajustes finos baseados no feedback da comunidade e testes em mais hardwares.

---

## 💬 Autor

Desenvolvido com ☕ e muita linha de código por **opswesley**.
* [GitHub](https://github.com/opswesley)
* [Discord](https://discord.gg/K3wMa8Dqsg) *(Comunidade, feedback e suporte)*

> *O tempo é o recurso mais valioso de um técnico de TI. Esta ferramenta foi criada para devolver esse tempo a você.*
