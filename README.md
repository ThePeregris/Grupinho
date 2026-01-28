
# 🛡️ Grupinho - Gestor de Grupo Avançado

O **Grupinho** é a ferramenta definitiva de gestão de raids para o **Turtle WoW (1.12.1)**. Desenhado para líderes que precisam de precisão cirúrgica no "recall" do grupo e organização visual de prontidão através de uma interface intuitiva e automatizada.

---

## ⚡ Quickstart (Início Rápido)

1. **Abrir:** Digita `/grupinho` no chat.
2. **Preparar:** Clica em **Capturar** para listar o teu grupo atual ou cola os nomes na caixa.
3. **Organizar:** Clica em **Formar Grupo** para enviar os convites e converter para raid.
4. **Verificar:** Clica em **Todos Prontos?** e observa quem fica **Verde** na lista lateral.
5. **Executar:** Clica em **Iniciar Protocolo** para o ciclo de reconvite automático.

---

## 🚀 Comandos de Acesso

Para mostrar ou esconder a central de comando:

`/grupinho`

---

## 🛠️ Explicação dos Botões e Controlos

### 🎚️ Configurações de Ambiente

* **Contagem Gritada (Checkbutton):** * *Marcado:* A contagem regressiva e os avisos de protocolo serão feitos via `/yell` (público).
* *Desmarcado:* Os avisos serão enviados de forma privada para o canal da **Raid** ou **Grupo**.

* **Reconvite em: (Slider 30s - 55s):** * Define o tempo alvo () para o envio dos convites. Toda a contagem sonora e de chat ajusta-se dinamicamente com base neste valor.

### 📋 Gestão de Nomes e Formação

* **Campo de Entrada:** Local para inserir ou editar nomes manualmente (suporta espaços, vírgulas ou `;`).
* **Capturar:** Copia os nomes de todos os membros da raid/party atual (exceto o seu).
* **Limpar:** Esvazia a caixa de nomes e limpa a lista lateral.
* **Formar Grupo:** Envia convites imediatos e faz a conversão para Raid automaticamente se houver mais de 5 nomes.

### ⏳ Iniciar Protocolo (O Ciclo de Reconvite)

Ao clicar neste botão, o cronómetro inicia com base no tempo definido no Slider ():

1. **Saída:** O líder abandona o grupo atual imediatamente.
2. **T - 2s:** Toca o som de *Ready Check* para alertar o líder.
3. **Tempo T:** Envio automático de convites + Grito inicial "6...".
4. **T + 1s a 5s:** Contagem regressiva visual de "5" a "1" no chat selecionado.
5. **T + 6s:** Grito final "AVANTE!" + Emote de investida (`/charge`).

### 🚂 Ready Check (Visual & Sonoro)

* **Todos Prontos?:** Reseta os status e pede ao grupo para usar o comando `/train`.
* **READY!:** Atalho para o líder executar o seu próprio emote `/train` e sinalizar prontidão.
* **Painel Lateral de Status:** * `[..] Nome` (Vermelho): Jogador ainda não confirmou.
* `[OK] Nome` (Verde): Jogador confirmou através do som do comboio.

### 🔄 Sistema de RESET

* **Botão RESET:** Utilizado para "zerar" a operação.
* Expulsa todos os membros atuais do grupo ou raid um a um.
* Interrompe qualquer cronómetro de protocolo em curso.
* Limpa a lista de prontidão lateral.
* **Nota:** Este botão *não* apaga os nomes da sua caixa de texto principal.

---

## 📂 Instalação Técnica

Para o funcionamento correto, a estrutura de pastas deve ser:

1. **Pasta:** `World of Warcraft/Interface/AddOns/Grupinho/`
2. **Ficheiro `Grupinho.toc`:** Deve conter obrigatoriamente a linha `## SavedVariables: Grupinho_Config`.
3. **Ficheiro `Grupinho.lua`:** O código fonte revisado.

> [!CAUTION]
> **Atenção:** O nome da pasta e dos ficheiros deve ser idêntico (`Grupinho`). Se houver discrepância, o WoW não carregará o addon. Certifica-te de ativar "Load out of date AddOns" no menu de personagens.

---

## 💾 Persistência de Dados

O addon utiliza memória local para guardar as suas preferências entre sessões:

* A posição exata da janela no ecrã.
* O valor de tempo definido no Slider.
* O estado da opção "Contagem Gritada".

---

*Assinatura de autoria integrada no software: **ThePeregris(c)***

---

**Comandante Bannion**, a documentação está agora em total conformidade com a sua interface. Gostaria que eu preparasse um ficheiro de "Changelog" (Registo de Alterações) para você manter o histórico de todas essas evoluções que fizemos?
