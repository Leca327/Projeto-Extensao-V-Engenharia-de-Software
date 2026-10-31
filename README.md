# ♻️ EcoDescarte — Sistema de Descarte de Eletrônicos

> Especificação e modelagem de um sistema que conecta cidadãos a pontos de coleta de lixo eletrônico, facilitando o descarte correto, a reciclagem e a logística reversa.

![Status](https://img.shields.io/badge/status-em%20andamento-yellow)
![ODS 12](https://img.shields.io/badge/ODS-12-BF8B2E)
![ODS 11](https://img.shields.io/badge/ODS-11-F99D26)

---

## 📌 Sobre o projeto

Projeto de Extensão desenvolvido no componente curricular **Engenharia de Software** da **Universidade Veiga de Almeida (UVA)**. O trabalho aplica o processo de Engenharia de Software para **especificar e modelar** um sistema com impacto social. Por isso, não há implementação de código.

| | |
|---|---|
| **Instituição** | Universidade Veiga de Almeida (UVA), Rio de Janeiro/RJ |
| **Disciplina** | Projeto de Extensão V – Engenharia de Software |
| **Cursos** | Sistemas de Informação, Engenharia da Computação e Ciências da Computação |
| **Orientador** | Prof. Cláudio Ribeiro da Silva |
| **Período** | 2º semestre de 2026 |

## 👩‍💻 Equipe

| Integrante | RA |
|---|---|
| Ágatha Santos de Souza | 1240112072 |
| Camile Pimenta Monteiro | 1240201525 |
| Dulce Maria dos Santos Barbosa | 1240207412 |
| Giovanna Rios de Lima Dantas | 1240112828 |
| Letícia dos Reis Prado | 1240207303 |

---

## ❗ Problema

O Brasil é o maior gerador de lixo eletrônico da América Latina: foram cerca de **2,4 milhões de toneladas em 2022**, segundo o *Global E-waste Monitor 2024*. Estima-se que apenas **cerca de 3%** desse volume seja reciclado. Celulares, computadores, pilhas e baterias acabam no lixo comum porque a população não sabe onde nem como descartá-los. Além disso, os pontos de coleta existentes são pouco divulgados e não têm controle do que recebem. O resultado é a contaminação do solo e da água por metais pesados e o desperdício de materiais que poderiam voltar à cadeia produtiva.

## 🎯 Missão do produto

Conectar cidadãos e pontos de coleta de resíduos eletrônicos: facilitar a localização de locais adequados, orientar o descarte correto e organizar as entregas por agendamento.

## 🌍 ODS relacionadas

- **ODS 12 – Consumo e Produção Responsáveis** (principal): contribui para as metas **12.5** (reduzir a geração de resíduos por meio da prevenção, redução, reciclagem e reúso) e **12.4** (manejo ambientalmente adequado dos resíduos).
- **ODS 11 – Cidades e Comunidades Sustentáveis** (complementar): incentiva práticas que reduzem os impactos ambientais do descarte inadequado.

🔗 https://brasil.un.org/pt-br/sdgs

---

## 👥 Atores

| Ator | Tipo | Descrição |
|---|---|---|
| **Cidadão** | Primário | Pessoa que deseja descartar equipamentos eletrônicos. Busca pontos de coleta, consulta orientações e agenda entregas. |
| **Ponto de Coleta** | Primário | ONG, cooperativa, loja ou órgão público que recebe os resíduos. Gerencia agendamentos e registra os materiais recebidos. |
| **Administrador** | Primário | Integrante da equipe do EcoDescarte que valida o cadastro dos pontos de coleta e gerencia o sistema. |

## 📐 Escopo

| ✅ O sistema faz | ❌ O sistema não faz |
|---|---|
| Cadastro e login de usuários | Coleta ou transporte dos resíduos |
| Busca de pontos de coleta no mapa, com filtro por tipo de resíduo | Reciclagem ou tratamento dos materiais |
| Guia de descarte | Compra, venda ou pagamento por equipamentos |
| Agendamento, remarcação e cancelamento de entregas | Apagamento dos dados dos aparelhos (apenas orienta) |
| Gestão de agendamentos e registro de materiais pelos pontos | Descarte industrial em grande escala |
| Aprovação de novos pontos de coleta pelo administrador | |

---

## 📋 Requisitos

### Requisitos funcionais

| Nº | Requisito | Descrição | Ator | Prioridade |
|---|---|---|---|---|
| RF01 | Manter cadastro e acesso | O sistema deve permitir o cadastro e o login com e-mail e senha para o cidadão e para o ponto de coleta. | Cidadão e Ponto de Coleta | Essencial |
| RF02 | Buscar pontos de coleta | O sistema deve permitir a busca de pontos de coleta próximos em um mapa, com filtro por tipo de eletrônico aceito, para o cidadão. | Cidadão | Essencial |
| RF03 | Consultar orientações | O sistema deve permitir a consulta de orientações de preparo e descarte correto de cada tipo de equipamento para o cidadão. | Cidadão | Desejável |
| RF04 | Agendar entrega | O sistema deve permitir o agendamento, a remarcação e o cancelamento da entrega de equipamentos em um ponto de coleta para o cidadão. | Cidadão | Essencial |
| RF05 | Gerenciar agendamentos | O sistema deve permitir a visualização, a confirmação e a recusa dos agendamentos recebidos para o ponto de coleta. | Ponto de Coleta | Essencial |
| RF06 | Registrar materiais e emitir relatório | O sistema deve permitir o registro dos materiais recebidos (tipo, quantidade e peso) e a emissão de relatório mensal para o ponto de coleta. | Ponto de Coleta | Desejável |
| RF07 | Aprovar ponto de coleta | O sistema deve permitir a aprovação ou a reprovação do cadastro de novos pontos de coleta para o administrador. | Administrador | Essencial |

### Requisitos não funcionais

| Nº | Tipo | Descrição |
|---|---|---|
| RNF01 | Produto | O sistema deve responder às buscas de pontos de coleta de forma rápida e eficiente. |
| RNF02 | Produto | O sistema deve estar disponível 24 horas por dia, 7 dias por semana, com disponibilidade mínima de 99% ao mês. |
| RNF03 | Produto | O sistema deve ter interface em português e responsiva, funcionando em celulares e computadores. |
| RNF04 | Externo | O sistema deve armazenar as senhas criptografadas e tratar os dados pessoais conforme a LGPD (Lei nº 13.709/2018). |
| RNF05 | Organizacional | O sistema deve ser especificado com a notação UML, e seus artefatos devem ser entregues ao fim de cada sprint de duas semanas. |

### Regras de negócio

| Regra | Descrição | Tipo | RF |
|---|---|---|---|
| RN01 | Um cidadão pode ter no máximo dois agendamentos pendentes ao mesmo tempo. | Rejeição | RF04 |
| RN02 | Um agendamento só pode ser remarcado ou cancelado até duas horas antes do horário marcado. | Rejeição | RF04 |
| RN03 | Ao confirmar um agendamento, o sistema deve notificar o cidadão por e-mail. | Projeção | RF05 |
| RN04 | Um ponto de coleta só aparece na busca depois de aprovado pelo administrador. | Rejeição | RF02 e RF07 |
| RN05 | O total recebido no mês é a soma dos pesos dos materiais registrados no período. | Produção | RF06 |

---

## 🧩 Diagrama de Casos de Uso

![Diagrama de Casos de Uso](diagramas/casos-de-uso.png)

| Requisito | Caso(s) de uso | Ator |
|---|---|---|
| RF01 | UC01 Cadastrar-se no sistema · UC02 Fazer login | Cidadão e Ponto de Coleta |
| RF02 | UC03 Buscar pontos de coleta | Cidadão |
| RF03 | UC04 Consultar orientações | Cidadão |
| RF04 | UC05 Agendar entrega · UC06 Remarcar ou cancelar entrega | Cidadão |
| RF05 | UC07 Gerenciar agendamentos | Ponto de Coleta |
| RF06 | UC08 Registrar materiais · UC09 Emitir relatório | Ponto de Coleta |
| RF07 | UC10 Aprovar ponto de coleta | Administrador |

## 🔄 Modelo de processo

O grupo adotou o **Scrum simplificado**, com sprints de duas semanas. A justificativa completa está no relatório (Desafio 3).

## 🗓️ Cronograma

| Etapa / tarefa | Ago | Set | Out | Nov |
|---|:---:|:---:|:---:|:---:|
| Definição do sistema, escolha da ODS 12 e justificativa | ✔ | | | |
| Pesquisa sobre descarte de eletrônicos e público-alvo | ✔ | | | |
| Documento de Visão (Sprint 1) | | ✔ | | |
| Escolha e justificativa do modelo de processo (Scrum) | | ✔ | | |
| Levantamento de requisitos funcionais e não funcionais (Sprint 2) | | ✔ | ✔ | |
| Diagrama de Casos de Uso no Draw.io (Sprint 3) | | | ✔ | |
| Protótipos das telas e validação com pontos de coleta (Sprint 4) | | | ✔ | |
| Plano de qualidade e casos de teste (Sprint 5) | | | | ✔ |
| Revisão e documento final em PDF | | | | ✔ |
| Postagem individual no Canvas (até 30/11) | | | | ✔ |

---

## ✅ Andamento dos desafios

- [x] **Desafio 1** – Cronograma de atividades
- [x] **Desafio 2** – Escolha e justificativa da ODS
- [ ] **Desafio 3** – Relatório do projeto *(em andamento)*
  - [x] Visão do sistema (problema, missão, atores, objetivos e escopo)
  - [x] Requisitos funcionais, não funcionais e regras de negócio
  - [x] Diagrama de Casos de Uso e rastreabilidade
  - [x] ODS
  - [ ] Justificativa do modelo de processo
  - [ ] Plano de qualidade e casos de teste
- [ ] **Desafio 4**
- [ ] **Desafio 5**

## 📁 Estrutura do repositório

```
📦 EcoDescarte
 ┣ 📂 docs
 ┃ ┣ 📄 desafio-1-cronograma.pdf
 ┃ ┣ 📄 desafio-2-ods.pdf
 ┃ ┗ 📄 desafio-3-relatorio.pdf
 ┣ 📂 diagramas
 ┃ ┣ 📄 casos-de-uso.drawio
 ┃ ┗ 🖼️ casos-de-uso.png
 ┗ 📄 README.md
```

## 🛠️ Ferramentas

- **Draw.io** – modelagem UML (Diagrama de Casos de Uso)
- **Microsoft Word** – documentação no padrão ABNT
- **GitHub** – versionamento e organização dos entregáveis

## 📚 Referências

- BALDÉ, C. P. et al. **The Global E-waste Monitor 2024**. Genebra; Bonn: ITU; UNITAR, 2024.
- BRASIL. Lei nº 12.305, de 2 de agosto de 2010. Política Nacional de Resíduos Sólidos.
- BRASIL. Lei nº 13.709, de 14 de agosto de 2018. Lei Geral de Proteção de Dados Pessoais (LGPD).
- NAÇÕES UNIDAS BRASIL. **Objetivos de Desenvolvimento Sustentável**. Disponível em: https://brasil.un.org/pt-br/sdgs.
- PRIZIBISCZKI, C. Produção mundial de lixo eletrônico é cinco vezes maior do que sua reciclagem, diz ONU. **Jornal do Brasil**, 21 mar. 2024.
- SILVA, C. R. da. **Engenharia de Software**: Unidades 1, 2 e 3. Notas de aula. UVA, 2026.

---

<p align="center">Projeto acadêmico de extensão · Universidade Veiga de Almeida · 2026</p>
