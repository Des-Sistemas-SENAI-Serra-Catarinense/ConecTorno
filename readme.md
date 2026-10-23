# Monitor no Torno CNC — Roteiro do Aluno

> Encontro 1 · 22/10/2026 · Prof. Vitor

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
| Altura dos olhos do operador, em pé na posição de trabalho |  |
| Distância do operador até o ponto provável do monitor |  |
| Espaço livre ao lado do torno (largura × altura) |  |
| Distância até a tomada mais próxima |  |
| Distância até o ponto de rede mais próximo (se houver) |  |

As fotos vão para `docs/entrevista` no repositório, com nomes que digam o que mostram (`torno-frente.jpg`, `local-monitor.jpg`).

| O operador precisa ver | O que atrapalha hoje | Restrições da oficina |
| --- | --- | --- |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

Fechem a síntese com uma frase: **"O aluno que opera o torno precisa \_\_\_\_\_\_ porque \_\_\_\_\_\_."**

| Ideia | Onde fica a tela | Como o projeto chega | Como o aluno navega | Votos |
| --- | --- | --- | --- | --- |
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |

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


## Equipes e Responsabilidades

### Equipe 1 — TreteenTech

**Líder:** Fernanda

**Integrantes:** Fernanda, Laura e Isabella.

**Responsabilidades:**

- Realizar entrevistas para coletar informações necessárias ao projeto.
- Efetuar medições relacionadas ao projeto.
- Registrar as atividades por meio de fotografias e gravações de vídeos.
- Organizar as equipes.

---

### Equipe 2 — Comunic CNC

**Líder:** Lorenzo

**Integrantes:** Lorenzo, Victor Mota e Eduardo.

**Responsabilidades:**

- Desenvolver a parte de software do projeto.
- Trabalhar na implementação do servidor.
- Desenvolver e integrar as partes Frontend e Backend do sistema.

---

### Equipe 3 — Lakave

**Líder:** Lucas

**Integrantes:** Lucas, Vitor Rodrigues, Amabile, Kimberlie e Kauan.

**Responsabilidades:**

- Elaborar a documentação do projeto.
- Desenvolver e organizar a parte teórica.
- Registrar informações importantes sobre o desenvolvimento e as etapas do projeto.

---

### Equipe 4 — Axión

**Líder:** João

**Integrantes:** João, Paulo e Gabriel.

**Responsabilidades:**

- Planejar e realizar a montagem do contêiner para o Raspberry Pi, possivelmente utilizando impressão 3D.
- Instalar e configurar o sistema operacional no Raspberry Pi.
- Integrar o Raspberry Pi ao monitor.

---

### Equipe 5 — Neonix

**Líder:** Luiza

**Integrantes:** Luiza, Raissa e Maria.

**Responsabilidades:**

- Desenvolver o protótipo do projeto.
- Identificar, definir e organizar os requisitos necessários.
- Contribuir para o planejamento das funcionalidades e características do projeto.


Todo artefato leva no canto o nome da equipe e a marca **v1**.

5. O líder de projeto confere se cada equipe fez pelo menos um commit.
   
