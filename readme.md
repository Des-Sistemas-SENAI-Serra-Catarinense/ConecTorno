# Monitor no Torno CNC — Roteiro do Aluno

> Encontro 1 · 22/10/2026 · Prof. Vitor

## O desafio

Vocês vão projetar e instalar um monitor junto ao torno CNC, ligado a um Raspberry Pi, que mostra o projeto da peça para quem está operando a máquina. Hoje vocês não constroem nada ainda: hoje vocês descobrem o problema, levantam os materiais e fazem a primeira versão da modelagem.

**Pergunta-guia:** como podemos deixar o projeto da peça sempre à vista no torno CNC, sem atrapalhar a operação nem a segurança?

**O que sai daqui hoje:**

- Respostas da entrevista e medidas do local do torno.
- Quadro de necessidades e as 3 ideias mais votadas.
- Lista de materiais preenchida, com o que temos e o que falta.
- Um artefato de modelagem v1 por equipe, salvo no repositório.

**Regras do encontro:**

1. Na oficina, vocês seguem as regras do instrutor de usinagem e usam os EPIs exigidos.
2. Ninguém encosta no torno, no painel ou nas ferramentas sem autorização.
3. O Raspberry Pi nunca vai ser ligado ao comando do CNC; ele só exibe o projeto.
4. Toda decisão vale só se estiver registrada (foto, arquivo ou issue no repositório).

## Formem as equipes (10 min)

A turma se divide em cinco equipes de 3 a 5 pessoas; cada equipe é dona de uma parte do sistema, mas todas participam de todos os passos. Escrevam os nomes na tabela.

| Equipe | Do que cuida | Entrega de hoje | Integrantes |
| --- | --- | --- | --- |
| Campo e Usuário | Entrevista, observação, fotos e medidas na oficina | Respostas da entrevista e medidas |  |
| Hardware e Montagem | Raspberry Pi, monitor, fonte, cabos, suporte e proteção | Lista de materiais preenchida |  |
| Software | Sistema operacional, como o projeto chega ao Pi e como o aluno navega na tela | 2 ou 3 jeitos de carregar e exibir o projeto |  |
| Modelagem e Documentação | Requisitos, diagramas e repositório | Diagrama de blocos v1 e lista de requisitos |  |
| Segurança e Oficina | Regras da oficina, posição do monitor, energia e EPIs | Checklist de segurança com o instrutor |  |

**Líder de projeto (troca a cada encontro):** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

O líder cria agora o repositório `monitor-torno-cnc` no GitHub, adiciona todos como colaboradores e cria as pastas `docs/entrevista`, `docs/materiais` e `docs/modelagem` (com um arquivo `.gitkeep` em cada uma, porque o Git não guarda pasta vazia).

## Passo 1 — Imersão na oficina (40 min)

Vocês vão até o torno para ver como ele é usado de verdade, antes de pensar em qualquer solução. Antes de entrar, a equipe de Segurança confirma com o instrutor quais EPIs são obrigatórios e por onde a turma pode circular.

**1.1 Observem uma usinagem (10 min).** Anotem em que momentos o operador olha o desenho da peça, onde ele está parado quando olha e o que ele faz com as mãos.

**1.2 Entrevistem (15 min).** A equipe Campo conduz, as outras escutam e anotam. Preencham as respostas aqui mesmo.

| Pergunta | Instrutor de usinagem | Aluno que opera o torno |
| --- | --- | --- |
| Que informação vocês precisam olhar durante a usinagem? |  |  |
| Como consultam hoje e o que dá errado? |  |  |
| Em que formato o projeto existe hoje (papel, PDF, DWG, STEP, foto)? |  |  |
| Em que momento olham o projeto: máquina parada, entre operações, durante o ciclo? |  |  |
| Onde um monitor ficaria sem cobrir a peça, o painel e o botão de emergência? |  |  |
| Com mão suja ou de luva, qual o jeito mais fácil de trocar de página ou dar zoom? |  |  |
| Quem coloca o projeto da aula no sistema, e quando? |  |  |
| Tem tomada e rede perto da máquina? Pode fixar algo nela? |  |  |

**1.3 Meçam e fotografem (15 min).** Usem trena; fotografem o torno de frente, dos dois lados e o local onde o monitor poderia ficar.

| Medida | Valor (cm) |
| --- | --- |
| Altura dos olhos do operador, em pé na posição de trabalho | 1,54m  |
| Distância do operador até o ponto provável do monitor | 1,5m  |
| Espaço livre ao lado do torno (largura × altura) | 21cm  |
| Distância até a tomada mais próxima | 3,10m |
| Distância até o ponto de rede mais próximo (se houver) | 3,69  |

As fotos vão para `docs/entrevista` no repositório, com nomes que digam o que mostram (`torno-frente.jpg`, `local-monitor.jpg`).

## Passo 2 — Síntese e ideias (50 min)

De volta à sala, vocês transformam o que viram em necessidades e, só depois, em ideias. Depois deste passo, intervalo de 15 minutos.

**2.1 Quadro de necessidades (25 min).** Cada pessoa escreve post-its com o que viu e ouviu e cola na coluna certa. Depois, juntem os repetidos e passem para a tabela os mais importantes.

| O operador precisa ver | O que atrapalha hoje | Restrições da oficina |
| --- | --- | --- |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

Fechem a síntese com uma frase: **"O aluno que opera o torno precisa \_\_\_\_\_\_ porque \_\_\_\_\_\_."**

**2.2 Crazy 8s (25 min).**

1. Cada pessoa dobra uma folha A4 em 8 partes.
2. Em 8 minutos, desenha 8 ideias diferentes, uma por quadro, sem se preocupar com capricho.
3. Cada ideia precisa mostrar três coisas: onde fica a tela, como o projeto chega até ela e como o aluno troca de página ou dá zoom.
4. Cada um apresenta suas 2 melhores ideias em 1 minuto.
5. Votação: cada pessoa tem 3 votos (bolinhas) e pode colocar mais de um na mesma ideia.
6. Registrem as 3 mais votadas abaixo e fotografem as folhas para `docs/entrevista`.

| Ideia | Onde fica a tela | Como o projeto chega | Como o aluno navega | Votos |
| --- | --- | --- | --- | --- |
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |

## Passo 3 — Levantamento de materiais (45 min)

A equipe de Hardware conduz, mas cada equipe confere os itens da sua parte com o professor e o almoxarifado. Na coluna "Temos?", escrevam **Sim**, **Não** ou **Verificar** em cada linha; o que ficar como "Não" vira lista de compras.

| Item | Para quê | Temos? | Onde está ou preço + link |
| --- | --- | --- | --- |
| Raspberry Pi (3B+, 4 ou 5) | Computador que exibe o projeto |  |  |
| Cartão microSD 32 GB | Sistema operacional |  |  |
| Fonte oficial do modelo de Pi | Energia estável para o Pi |  |  |
| Monitor com HDMI e furação VESA | Tela do projeto |  |  |
| Cabo HDMI ou micro-HDMI → HDMI | Ligar o Pi ao monitor |  |  |
| Case com ventilação para o Pi | Proteger e resfriar o Pi |  |  |
| Suporte VESA (braço, parede ou pedestal) | Fixar o monitor |  |  |
| Caixa de proteção com frente transparente | Proteger contra fluido de corte e cavaco |  |  |
| Filtro de linha | Energia em tomada própria |  |  |
| Acesso à rede (Wi-Fi ou cabo) | Atualizar o projeto exibido |  |  |
| Canaleta e abraçadeiras | Organizar os cabos |  |  |
| Botões grandes + jumpers, ou teclado numérico USB | Trocar página e dar zoom |  |  |
| Teclado e mouse USB | Configuração inicial |  |  |

**Itens que a ideia escolhida de vocês precisa a mais:**

| Item | Para quê | Temos? | Onde está ou preço + link |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

**Dicas para decidir:**

- O tamanho do monitor sai da distância que vocês mediram no passo 1: quanto mais longe o operador, maior a tela e a letra.
- Para só mostrar PDF e imagem, um Raspberry Pi de 1 ou 2 GB já resolve; antes de pedir compra, perguntem se a escola tem algum parado.
- Para cotar, usem revendedores autorizados de Raspberry Pi no Brasil, como RoboCore, FilipeFlop, Eletrogate e UsinaInfo, e colem o link na tabela.

## Passo 4 — Modelagem v1 (60 min)

Cada equipe transforma a ideia mais votada em um artefato de modelagem, usando só o que foi visto, medido e respondido na oficina. O que ficar em dúvida não é inventado: vira uma pergunta escrita no próprio diagrama.

| Equipe | O que produzir | O artefato precisa responder | Ferramenta |
| --- | --- | --- | --- |
| Modelagem e Documentação | Diagrama de blocos do sistema | Quais partes existem, como se ligam, de onde vêm a energia e o projeto? | Papel ou draw.io |
| Software | Diagrama de casos de uso e diagrama de atividades | Quem usa o sistema, o que cada um faz e qual o caminho do projeto até a peça conferida? | draw.io ou PlantUML |
| Hardware e Montagem | Esboço físico, vista frontal e lateral | Onde fica o monitor, em que altura e distância, por onde passam os cabos? | Papel quadriculado, Tinkercad ou SketchUp |
| Campo e Usuário | Wireframe da tela | O que aparece na tela e o que dá para ler da posição do operador? | Papel ou Figma |
| Segurança e Oficina | Checklist de segurança validado com o instrutor | A ideia escolhida pode ser instalada sem risco? | Este documento |

**Lista de requisitos** (equipe Modelagem, com sugestões de todas as equipes). Usem este formato no README do repositório:

- RF01 — O sistema deve \_\_\_\_\_\_. (requisito funcional: o que o sistema faz)
- RNF01 — O sistema deve \_\_\_\_\_\_. (requisito não funcional: em que condições ou com que qualidade)

**Checklist da equipe de Segurança** (marquem só o que o instrutor confirmou):

- [ ] O local escolhido não cobre a peça, o painel de comando nem o botão de emergência.
- [ ] O monitor e o suporte não impedem abrir as portas e proteções do torno.
- [ ] A fixação não usa a carcaça, as portas ou as proteções da máquina.
- [ ] A energia vem de uma tomada própria, fora do painel elétrico do torno.
- [ ] Os cabos podem passar longe de partes móveis e da área de circulação.
- [ ] Tela e Raspberry Pi podem ficar protegidos de fluido de corte e cavaco.
- [ ] A consulta ao projeto pode ser feita com a máquina parada ou com as portas fechadas.

Todo artefato leva no canto o nome da equipe e a marca **v1**.

## Passo 5 — Apresentação e registro (15 min)

Cada equipe mostra o que produziu em 2 minutos, e tudo vai para o repositório antes de sair da sala.

1. Cada equipe apresenta seu artefato v1: o que decidiu e qual dúvida ficou.
2. A turma faz no máximo uma pergunta por equipe.
3. Cada dúvida aberta vira uma issue no GitHub, com o nome da equipe no título.
4. Fotografem ou exportem os artefatos e façam commit em `docs/modelagem`, com mensagem clara (ex.: `modelagem: diagrama de blocos v1`).
5. O líder de projeto confere se cada equipe fez pelo menos um commit.

## Checklist de saída

O encontro só termina quando todos os itens abaixo estiverem marcados.

- [ ] Equipes e líder de projeto definidos.
- [ ] Repositório `monitor-torno-cnc` criado, com todos como colaboradores.
- [ ] Tabela da entrevista preenchida pelas duas pessoas entrevistadas.
- [ ] Medidas anotadas e fotos do torno no repositório.
- [ ] Quadro de necessidades e frase de síntese prontos.
- [ ] 3 ideias mais votadas registradas.
- [ ] Lista de materiais com "Temos?" marcado em todas as linhas.
- [ ] Um artefato v1 por equipe no repositório.
- [ ] Checklist de segurança revisado com o instrutor.
- [ ] Dúvidas abertas registradas como issues.
