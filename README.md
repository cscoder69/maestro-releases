# Maestro

Barra para Windows que mostra todas as suas sessões do **Claude Code** no VS Code, numa linha fina no alto da tela, e avisa quando uma delas precisa de você.

- Cada sessão aparece com o nome e o estado: **Pendente** (pediu permissão ou fez uma pergunta), **Aguardando** (terminou a etapa), **Livre**, **Pensando** ou **Ocupada**.
- As que precisam de você vêm primeiro.
- Clicar numa sessão leva direto à janela dela no VS Code.
- Avisa com som e pop-up quando uma sessão termina ou pede algo.
- Acha sozinho as sessões que já estavam abertas.

Este repositório tem só os instaladores (releases). O código é mantido à parte.

## Instalar

1. Baixe o **Maestro-Instalador.zip** do [último release](../../releases/latest).
2. Descompacte e dê dois cliques no **Instalar.cmd**.

O instalador faz tudo sozinho:

- instala o .NET 10 Desktop Runtime, se faltar (pode pedir permissão de administrador);
- copia o programa para `%USERPROFILE%\Maestro`;
- liga o Maestro ao Claude Code (hooks em `%USERPROFILE%\.claude\settings.json`, com backup e sem apagar o que já existe);
- faz o Maestro abrir com o Windows.

Sessões do Claude que já estavam abertas precisam ser fechadas e abertas de novo para começarem a avisar.

Na primeira vez, o Windows pode mostrar o aviso azul do SmartScreen: clique em **Mais informações** e depois em **Executar assim mesmo**.

## Atualizações

O Maestro se atualiza sozinho: ele confere os releases deste repositório ao abrir e a cada 6 horas, baixa a versão nova, confere o arquivo e reinicia. Para conferir na hora, use **Procurar atualização** no menu do ícone perto do relógio.

## Requisitos

- Windows 10 ou 11 (64 bits)
- Claude Code (no VS Code ou no terminal)

A fonte Ubuntu, embutida no programa, é distribuída sob a Ubuntu Font Licence 1.0 (`UFL.txt` no pacote).
