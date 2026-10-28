# BoostPing

**Uma ferramenta gratuita que ajusta as configurações de rede do Windows para jogos com um único botão e deixa os jogos online mais responsivos.**

[English](README.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [Español](README.es.md) · Português (Brasil) · [Français](README.fr.md)

> Este documento é uma tradução. Em caso de divergência, a [versão em coreano](README.ko.md) prevalece.

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20(64--bit)-0078D4)
![License](https://img.shields.io/badge/license-Freeware-brightgreen)
[![Download](https://img.shields.io/badge/download-kilho.net-orange)](https://down.kilho.net/boostping?lang=pt)

![Tela do BoostPing](images/boostping-en.png)

A interface do programa é exibida em inglês.

## Visão geral

Por padrão, o Windows junta os dados de rede por um instante e os envia em lote. Isso é eficiente para baixar arquivos ou navegar na web, mas em jogos online — onde cada tecla pressionada precisa chegar ao servidor na hora — faz o jogo responder mais tarde.

O BoostPing altera cinco dessas configurações para deixá-las adequadas a jogos. Pressione **Start Boost** e ele encontra a rede pela qual você está conectado à internet, aplica as configurações e reconecta a rede. Pressione **Turn Off Boost** e ele devolve exatamente os valores que você tinha antes. Você escolhe quais itens alterar, e os itens desmarcados nunca são tocados.

## Principais recursos

- **Um só botão** — Sem configurações complicadas; basta pressionar Start Boost uma vez.
- **Encontra automaticamente a rede em uso** — Escolhe o adaptador realmente conectado à internet e mostra o nome e o IP dele na parte de baixo da janela. Adaptadores de rede virtuais são ignorados.
- **Cinco itens, aplicados como você escolher** — Instant ACK, No ACK Delay, Disable Nagle's Algorithm, Remove Network Throttling, Prioritize Games.
- **Restauração exata** — Memoriza os valores de antes do boost e os devolve quando você o desliga. Configurações que não existiam são removidas, e valores que você mesmo tinha alterado voltam a esses valores.
- **Continua valendo depois de fechar** — As configurações são aplicadas ao Windows, então o efeito continua depois de fechar a janela ou reiniciar. Ao abrir de novo, ele mostra o estado aplicado como está.
- **9 idiomas na interface** — Coreano · Inglês · Japonês · Chinês · Russo · Italiano · Francês · Árabe · Espanhol. Segue o idioma de exibição do Windows.

## Download / Instalação

| Tipo | Link |
|---|---|
| Instalador | [Download](https://down.kilho.net/boostping?lang=pt) |
| Portable (ZIP) | [Download](https://down.kilho.net/boostping?lang=pt&nosetup) |

A versão instalada abre assim que a instalação termina. Na versão portátil, descompacte o ZIP e execute `BoostPing.exe`. Em ambos os casos, ele pede **direitos de administrador**.

## Como usar

### Primeiros passos

1. Execute o BoostPing. Como ele altera configurações do Windows, aparece uma janela de confirmação de permissão de administrador — clique em **Sim**.
2. Confira se o nome e o IP da rede que você está usando aparecem na linha de baixo. (ex.: `Ethernet (Realtek PCIe GbE Family Controller) · 192.168.0.10`)
3. Para escolher quais itens alterar, clique no **ícone de ajustes** no canto superior direito para abrir a tela **TUNING**. No início, os cinco estão ligados.
4. Clique em **Start Boost**. O status muda para **BOOST** e aparece "Reconnecting the network…". Nesse momento a internet cai rapidamente e se reconecta.
5. Quando a internet volta, o status muda para **ON** com "Optimization is applied". Agora é só abrir o jogo.
6. Para voltar ao que era antes, clique em **Turn Off Boost**. A rede se reconecta mais uma vez e o status volta para **READY**.

### Elementos da tela

**Tela principal**

| Elemento | Descrição |
|---|---|
| Logotipo **BOOST//PING** | Abre a página do BoostPing |
| Ícone de ajustes (canto superior direito) | Abre a tela TUNING |
| **STATUS** | **READY** = em espera, **BOOST** = aplicando, **ON** = aplicado |
| 5 barras · **%d / 5 items** | Número de itens ligados; uma barra por item |
| **Start Boost** / **Turn Off Boost** | Aplicar / restaurar as configurações originais |
| Linha de baixo | Nome · IP da rede em uso, versão do programa |

**Tela TUNING** — Clique em um item para ligá-lo ou desligá-lo. As mudanças são salvas na hora.

| Item | O que faz |
|---|---|
| **Instant ACK** | Envia as confirmações na hora, sem agrupá-las |
| **No ACK Delay** | Zera o temporizador de confirmação atrasada |
| **Disable Nagle's Algorithm** | Envia pacotes pequenos na hora, sem juntá-los |
| **Remove Network Throttling** | Remove o limite de transferência aplicado durante a reprodução de mídia |
| **Prioritize Games** | Deixa de reservar tempo de CPU para tarefas em segundo plano |

### Situações comuns

**Quando seus comandos no jogo parecem chegar um pouco atrasados**
Clique em Start Boost no BoostPing antes de abrir o jogo. Jogos online que trocam pequenos dados com frequência são onde mais se nota a diferença. Como a internet se reconecta rapidamente ao aplicar o boost, é melhor ligá-lo **antes** de entrar numa partida.

**Quando você quer ligar uma vez e deixar assim**
Depois de ligar o boost, você pode fechar a janela do BoostPing. As configurações ficam no Windows e continuam aplicadas mesmo depois de reiniciar. Ao abrir o BoostPing de novo, o status aparece como **ON**.

**Quando você joga com música ou uma live tocando**
O Windows limita as transferências de rede enquanto há mídia em reprodução. Com **Remove Network Throttling** ligado, esse limite não se aplica mesmo com música ou vídeo tocando.

**Quando você quer só alguns dos itens**
Com o boost desligado (READY), vá ao ícone de ajustes → tela TUNING e clique nos itens que não quer para desligá-los. As barras e o **%d / 5 items** da tela principal mudam na hora. Os itens desligados nunca são tocados, nem ao iniciar nem ao desligar.

**Quando você quer trocar itens com o boost ligado**
Enquanto o boost está ligado, a tela TUNING fica bloqueada e mostra "You can change these after turning off the boost.". Faça nesta ordem: Turn Off Boost → trocar os itens → Start Boost.

**Quando você quer comparar a diferença**
Jogue uma partida no estado original com Turn Off Boost e outra com Start Boost. Ao desligar, os valores de antes são restaurados exatamente, então você pode alternar e comparar quantas vezes quiser.

**Quando você já tinha alterado as configurações de rede por conta própria**
O BoostPing memoriza os valores atuais antes de começar. Ao desligar, ele volta para **os valores que você tinha definido**, e não para os padrões do Windows.

**Quando você alterna entre Wi‑Fi e cabo no notebook**
O boost é aplicado à rede que estava em uso quando você o iniciou. Se trocou de rede, clique em Turn Off Boost, feche o BoostPing e abra-o de novo. Quando a nova rede aparecer na linha de baixo, clique em Start Boost. Ao desligar, ele sempre restaura a rede à qual foi aplicado no início, mesmo que você tenha trocado de rede depois.

**Quando terminou de jogar e quer deixar tudo como antes**
Abra o BoostPing e clique em Turn Off Boost. Antes de desinstalar o programa, desligue o boost primeiro também.

**Quando você não encontra a janela do BoostPing**
Só um BoostPing roda por vez. Executá-lo de novo com ele já aberto traz a janela existente para a frente (e a restaura se estiver minimizada).

## Configuração

Alterada na tela TUNING e salva na hora. As configurações são mantidas nas atualizações.

| Item | Padrão |
|---|---|
| Instant ACK | Ligado |
| No ACK Delay | Ligado |
| Disable Nagle's Algorithm | Ligado |
| Remove Network Throttling | Ligado |
| Prioritize Games | Ligado |

O idioma da interface segue o idioma de exibição do Windows (coreano · inglês · japonês · chinês · russo · italiano · francês · árabe · espanhol; inglês nos demais casos, inclusive português). O árabe é exibido da direita para a esquerda.

## Requisitos

- Windows 10 · Windows 11 (64 bits)
- Direitos de administrador — como altera as configurações de rede do Windows, aparece uma janela de confirmação de permissão ao abrir.
- Nenhum runtime adicional é necessário.

## Atualizações

O BoostPing **não** se atualiza sozinho. Ao iniciar, verifica se há uma versão nova e mostra um aviso; ao pressionar **Sim**, a página de download é aberta e o programa é encerrado. As novas versões são publicadas manualmente após verificação interna e anunciadas na [página do BoostPing](https://kilho.net/boostping). Veja o [aviso sobre a política de atualização](https://en.kilho.net/archives/notice/2940).

## Licença

O BoostPing é **freeware**. Você pode usá-lo gratuitamente em qualquer lugar — no trabalho, em casa, em órgãos públicos ou na escola — e redistribuí-lo livremente.

## Links

- Site: <https://kilho.net/boostping>
- Fórum: <https://kilho.top/forum/qna>
- X (Twitter): <https://www.twitter.com/kilhonet>

© KILHO.NET
