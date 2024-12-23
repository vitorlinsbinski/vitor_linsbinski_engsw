# vitor_linsbinski_engsw

Repositório destinado aos estudos relacionados à disciplina de Engenharia de Software na UNEMAT

# Sumário

- [vitor_linsbinski_engsw](#vitor_linsbinski_engsw)
- [Sumário](#sumário)
- [1. Descrição do sistema](#1-descrição-do-sistema)
- [2. Problema e descrição do negócio](#2-problema-e-descrição-do-negócio)
  - [2.1. Requisitos](#21-requisitos)
    - [Requisitos Funcionas e Não Funcionais](#requisitos-funcionas-e-não-funcionais)
- [3. Visão geral do sistema.](#3-visão-geral-do-sistema)
- [4. Diagrama ER](#4-diagrama-er)
- [5. Diagrama de classes](#5-diagrama-de-classes)
- [6. Casos de uso](#6-casos-de-uso)
  - [6.1 Histórias de usuário](#61-histórias-de-usuário)
    - [Histórias de Usuário para a Clínica Veterinária](#histórias-de-usuário-para-a-clínica-veterinária)
      - [Cadastro de Clientes e Animais](#cadastro-de-clientes-e-animais)
      - [Informar Condições do Animal](#informar-condições-do-animal)
      - [Informar Tipo de Ração](#informar-tipo-de-ração)
      - [Informar Hábitos do Animal](#informar-hábitos-do-animal)
      - [Agendamento de Atendimento](#agendamento-de-atendimento)
      - [Atendimento e Ficha do Animal](#atendimento-e-ficha-do-animal)
      - [Colocar na Fila de Espera](#colocar-na-fila-de-espera)
      - [Realizar Entrevista](#realizar-entrevista)
      - [Registrar Resultados da Entrevista](#registrar-resultados-da-entrevista)
      - [Examinar Animal e Registrar Observações](#examinar-animal-e-registrar-observações)
      - [Gerar Receita](#gerar-receita)
      - [Comprar Brinquedos](#comprar-brinquedos)
      - [Buscar Prontuários Antigos](#buscar-prontuários-antigos)
      - [Agendar Retorno](#agendar-retorno)
      - [Enviar Lembretes Automáticos](#enviar-lembretes-automáticos)
      - [Gerar Relatórios de Atendimentos](#gerar-relatórios-de-atendimentos)
      - [Realizar Pagamento](#realizar-pagamento)
      - [Manter Histórico de Pagamentos](#manter-histórico-de-pagamentos)
- [7. Diagrama de componentes](#7-diagrama-de-componentes)
- [8. Diagrama de implantação](#8-diagrama-de-implantação)
- [9. Diagramas C4](#9-diagramas-c4)
  - [9.1. Diagrama de contexto](#91-diagrama-de-contexto)
  - [9.2. Diagrama de container](#92-diagrama-de-container)
  - [9.2. Diagrama de componente](#92-diagrama-de-componente)
  - [9.2. Diagrama de código](#92-diagrama-de-código)
- [10. Protótipo de telas](#10-protótipo-de-telas)
- [11. Diagrama de navegação de telas](#11-diagrama-de-navegação-de-telas)
- [12. Pilha tecnológica](#12-pilha-tecnológica)
- [13. Requisitos de sistemas](#13-requisitos-de-sistemas)
  - [13.1. Requisitos do Cliente](#131-requisitos-do-cliente)
    - [1. Navegador Web Compatível:](#1-navegador-web-compatível)
    - [2. Conexão à Internet:](#2-conexão-à-internet)
    - [3. Dispositivos Suportados:](#3-dispositivos-suportados)
      - [Desktop:](#desktop)
      - [Dispositivos Móveis:](#dispositivos-móveis)
    - [4. Software Adicional:](#4-software-adicional)
  - [13.2.2 Requisitos do Server Side](#1322-requisitos-do-server-side)
    - [1. Hardware da Máquina Virtual](#1-hardware-da-máquina-virtual)
    - [2. Software e Tecnologias](#2-software-e-tecnologias)
      - [Sistema Operacional:](#sistema-operacional)
      - [Servidor Web:](#servidor-web)
      - [Banco de Dados:](#banco-de-dados)
      - [Ambiente de Execução:](#ambiente-de-execução)
      - [Gerenciamento de Dependências:](#gerenciamento-de-dependências)
      - [Ferramentas de Containerização:](#ferramentas-de-containerização)
      - [Serviços de Email:](#serviços-de-email)
      - [Segurança e Autenticação:](#segurança-e-autenticação)
      - [Serviços de Cache:](#serviços-de-cache)
- [14. Considerações sobre segurança](#14-considerações-sobre-segurança)
  - [14.1. Lado Cliente](#141-lado-cliente)
    - [1. Regras de Senha](#1-regras-de-senha)
    - [2. Proteção contra XSS e CSRF](#2-proteção-contra-xss-e-csrf)
    - [3. Comunicação Segura](#3-comunicação-segura)
    - [4. Armazenamento Seguro de Dados](#4-armazenamento-seguro-de-dados)
  - [14.2. Lado Servidor](#142-lado-servidor)
    - [1. Sistema Operacional Seguro](#1-sistema-operacional-seguro)
    - [2. Política de Backups](#2-política-de-backups)
    - [3. Gerenciamento de Acesso](#3-gerenciamento-de-acesso)
    - [4. Proteção de Dados](#4-proteção-de-dados)
    - [5. Monitoramento e Logs](#5-monitoramento-e-logs)
    - [6. Atualizações e Patches](#6-atualizações-e-patches)
    - [7. Firewall e Segurança de Rede](#7-firewall-e-segurança-de-rede)
    - [8. Proteção contra Ataques DDoS](#8-proteção-contra-ataques-ddos)
- [15. Manutenção e instalação](#15-manutenção-e-instalação)
  - [15.1. Instalado no servidor](#151-instalado-no-servidor)
  - [15.2. Manutenção](#152-manutenção)
    - [1. Atualizações de Software](#1-atualizações-de-software)
    - [2. Monitoramento de Performance](#2-monitoramento-de-performance)
    - [3. Gerenciamento de Backups](#3-gerenciamento-de-backups)
    - [4. Correção de Bugs](#4-correção-de-bugs)
    - [5. Otimização de Banco de Dados](#5-otimização-de-banco-de-dados)
    - [6. Segurança Contínua](#6-segurança-contínua)
    - [7. Documentação Atualizada](#7-documentação-atualizada)
    - [8. Suporte Técnico](#8-suporte-técnico)
  - [15.3. Novas Funcionalidades](#153-novas-funcionalidades)
    - [1. Formalização do Pedido](#1-formalização-do-pedido)
    - [2. Feedback do Cliente](#2-feedback-do-cliente)
    - [3. Análise de Viabilidade](#3-análise-de-viabilidade)
      - [Critérios de Avaliação:](#critérios-de-avaliação)
    - [4. Planejamento e Desenvolvimento](#4-planejamento-e-desenvolvimento)
    - [5. Implantação e Treinamento](#5-implantação-e-treinamento)
    - [6. Monitoramento e Feedback](#6-monitoramento-e-feedback)
- [16. Treinamento](#16-treinamento)
  - [16.1. Usuário](#161-usuário)
  - [16.1. Treinamento de Usuários](#161-treinamento-de-usuários)
    - [Vídeos Tutoriais na Web](#vídeos-tutoriais-na-web)
    - [Manuais de Usuário](#manuais-de-usuário)
    - [Webinars e Sessões de Treinamento ao Vivo](#webinars-e-sessões-de-treinamento-ao-vivo)
    - [Suporte Online](#suporte-online)
    - [Feedback e Melhorias](#feedback-e-melhorias)
  - [16.2. Admin](#162-admin)
    - [Sessões Presenciais e Online](#sessões-presenciais-e-online)
    - [Documentação Técnica Detalhada](#documentação-técnica-detalhada)
    - [Acesso a Ferramentas de Monitoramento e Gestão](#acesso-a-ferramentas-de-monitoramento-e-gestão)
    - [Políticas de Segurança e Compliance](#políticas-de-segurança-e-compliance)
    - [Suporte Continuado e Atualizações](#suporte-continuado-e-atualizações)
- [17. Glossário](#17-glossário)
- [18. Script SQL](#18-script-sql)
  - [18.1. Comandos CREATE TABLE:](#181-comandos-create-table)
  - [18.2. Comandos INSERT gerando dados fictícios](#182-comandos-insert-gerando-dados-fictícios)

[Início](#sumário)

# 1. Descrição do sistema

O projeto a seguir apresenta um sistema desenvolvido para um petshop. A empresa é considerada micro e iniciou as atividades recentemente. Ao possuir serviços exclusivos, os sistemas presentes no mercado não se enquadra, desta forma, os proprietários decidiram desenvolver uma solução própria. Esta solução é detelhada a seguir:

[Início](#sumário)

# 2. Problema e descrição do negócio

1. Clínica veterinária atende apenas os animais: gatos e cachorros.
2. Clientes devem fazer um cadastro de si e dos animais.
3. Clientes devem informar as condições nas quais os animais chegam.
4. Clientes devem informar o tipo de ração que o animal come.
5. Cliente deve informar hábitos do animal.
6. Para cada animal, mais de um veterinário pode atendê-lo.
7. Animais podem ser atendidos de acordo com uma agenda do dia.
8. Cada animal atendido recebe uma ficha e um prontuário.
9. Outros donos podem querer marcar horários de atendimento futuro.
10. O atendimento gera uma receita para o animal.
11. Quando um cliente chega, é atendido por um atendente.
12. Atendente deve verificar se existe agenda disponível com um veterinário.
13. Atendente deve colocar o cliente e seu animal na fila de espera, se necessário.
14. Atendente deve levar o cliente e o animal até o veterinário.
15. Veterinário deve realizar uma entrevista com o dono do animal.
16. Resultado da entrevista deve ser registrado em um formulário.
17. Veterinário deve examinar o animal e anotar em prontuário suas observações.
18. Dependendo da situação, o animal receberá uma receita.
19. Clientes podem comprar brinquedos para seus animais
20. O sistema deve permitir buscar prontuários antigos para consulta.
21. Veterinários podem agendar retornos para acompanhamento do animal.
22. O sistema deve enviar lembretes automáticos aos donos sobre retornos agendados.
23. O sistema deve gerar relatórios sobre atendimentos realizados por veterinário.
24. Clientes podem pagar pelos serviços da clínica através de cartão ou dinheiro.
25. A clínica deve manter um histórico de pagamentos e faturamento dos clientes.

## 2.1. Requisitos

### Requisitos Funcionas e Não Funcionais

| **Tipo de Requisito**         | **Descrição**                                                                                        |
| ----------------------------- | ---------------------------------------------------------------------------------------------------- |
| **Requisitos Funcionais**     |                                                                                                      |
| RF01                          | A clínica deve atender apenas gatos e cachorros.                                                     |
| RF02                          | Clientes devem realizar o cadastro pessoal e dos animais.                                            |
| RF03                          | Clientes devem informar as condições nas quais os animais chegam à clínica.                          |
| RF04                          | Clientes devem informar o tipo de ração que o animal consome.                                        |
| RF05                          | Clientes devem informar hábitos específicos do animal.                                               |
| RF06                          | O sistema deve permitir o atendimento de cada animal por múltiplos veterinários.                     |
| RF07                          | O sistema deve gerenciar a agenda de atendimentos diários.                                           |
| RF08                          | O sistema deve registrar uma ficha e um prontuário para cada animal atendido.                        |
| RF09                          | O sistema deve permitir que donos agendem horários futuros.                                          |
| RF10                          | O atendimento deve gerar uma receita para o animal.                                                  |
| RF11                          | O cliente deve ser recebido e atendido por um atendente ao chegar.                                   |
| RF12                          | O atendente deve verificar se há disponibilidade na agenda com um veterinário.                       |
| RF13                          | O atendente deve colocar o cliente e o animal na fila de espera, se necessário.                      |
| RF14                          | O atendente deve acompanhar o cliente e o animal até o veterinário.                                  |
| RF15                          | O veterinário deve realizar uma entrevista com o dono do animal e registrar em formulário.           |
| RF16                          | O veterinário deve examinar o animal e anotar observações no prontuário.                             |
| RF17                          | O sistema deve permitir a emissão de receita para o animal, quando necessário.                       |
| RF18                          | O sistema deve permitir a compra de brinquedos pelos clientes.                                       |
| RF19                          | O sistema deve permitir a consulta a prontuários antigos.                                            |
| RF20                          | O sistema deve permitir o agendamento de retornos para acompanhamento dos animais.                   |
| RF21                          | O sistema deve enviar lembretes automáticos para donos sobre retornos agendados.                     |
| RF22                          | O sistema deve gerar relatórios de atendimentos realizados por veterinário.                          |
| RF23                          | O sistema deve registrar pagamentos realizados por cartão ou dinheiro.                               |
| RF24                          | O sistema deve manter um histórico de pagamentos e faturamento dos clientes.                         |
| **Requisitos Não Funcionais** |                                                                                                      |
| RNF01                         | O sistema deve ser seguro para proteger dados dos clientes e dos animais.                            |
| RNF02                         | O sistema deve ter alta disponibilidade para garantir o funcionamento durante o horário da clínica.  |
| RNF03                         | O sistema deve ser fácil de usar, permitindo uma experiência intuitiva para clientes e funcionários. |
| RNF04                         | O sistema deve enviar lembretes automáticos no prazo definido para retornos.                         |
| RNF05                         | O sistema deve ser escalável para suportar o aumento de clientes e animais.                          |
| RNF06                         | O sistema deve permitir acessibilidade em diferentes dispositivos, como desktops e tablets.          |
| RNF07                         | O sistema deve garantir a integridade e consistência dos dados.                                      |
| RNF08                         | O sistema deve ter um tempo de resposta rápido para as operações principais.                         |
| RNF09                         | O sistema deve seguir as regulamentações de segurança e privacidade de dados.                        |

[Início](#sumário)

# 3. Visão geral do sistema.

O sistema para a clínica veterinária tem como objetivo principal facilitar a gestão de atendimentos e serviços para animais de estimação, especificamente cães e gatos. Ele proporciona um ambiente digital onde clientes podem cadastrar seus animais, agendar consultas e acompanhar o histórico médico dos pets. Por outro lado, a equipe da clínica, composta por atendentes e veterinários, pode gerenciar o fluxo de atendimento, realizar avaliações, registrar prontuários e gerar receitas médicas.

A plataforma é projetada para atender às necessidades de uma clínica de pequeno porte, automatizando tarefas administrativas e médicas, como a manutenção de agendas, o gerenciamento de filas de espera, a consulta de prontuários antigos e o envio de lembretes automáticos para os clientes. Além disso, o sistema oferece funcionalidades para a compra de produtos e serviços, bem como para o registro e acompanhamento de pagamentos, visando proporcionar uma experiência completa tanto para os profissionais da clínica quanto para os clientes.

Essa solução abrange a integração de diversas áreas, como administração, saúde animal e comércio, permitindo à clínica operar de forma mais eficiente e com maior qualidade no atendimento aos seus clientes.

[Início](#sumário)

# 4. Diagrama ER

```mermaid

erDiagram
    CLIENTE {
        int id_cliente PK
        string nome
        string endereco
        string telefone
    }

    ANIMAL {
        int id
        string nome
        string especie
        string condicoes
        string racao
        string habitos
    }

    VETERINARIO {
        int id
        string nome
        string especialidade
    }

    ATENDENTE {
        int id
        string nome
        string turno
    }

    AGENDA {
        int id
        date data
        time hora
        int id_animal
        int id_veterinario
    }

    PRONTUARIO {
        int id
        int id_animal
        text observacoes
        text receita
        date data
    }

    PAGAMENTO {
        int id
        int id_cliente
        float valor
        date data
        string metodo
    }

    CLIENTE ||--o{ ANIMAL : "possui"
    ANIMAL ||--o{ VETERINARIO : "atendido por"
    CLIENTE ||--o{ PAGAMENTO : "realiza"
    ANIMAL ||--o{ AGENDA : "agendado para"
    VETERINARIO ||--o{ AGENDA : "realiza"
    AGENDA ||--o{ PRONTUARIO : "gera"
    CLIENTE ||--o{ PAGAMENTO : "paga"
    CLIENTE ||--o{ ANIMAL : "tem"
    ANIMAL ||--o{ PRONTUARIO : "possui"
    CLIENTE ||--o{ ATENDENTE : "atendido por"

```

[Início](#sumário)

# 5. Diagrama de classes

```mermaid
classDiagram
    class Cliente {
        +String nome
        +String endereco
        +String telefone
        +String email
        +listarAnimais()
    }

    class Animal {
        +String nome
        +String especie
        +String condicoes
        +String racao
        +String habitos
        +obterProntuario()
    }

    class Veterinario {
        +String nome
        +String especialidade
        +realizarEntrevista(Cliente)
        +examinarAnimal(Animal)
        +gerarProntuario(Animal)
        +emitirReceita(Animal)
        +agendarRetorno(Animal)
        +gerarRelatorioAtendimentos()
    }

    class Atendente {
        +String nome
        +String turno
        +verificarAgenda()
        +colocarNaFila(Cliente, Animal)
        +levarAoVeterinario(Cliente, Animal)
    }

    class Agenda {
        +Date data
        +Time hora
        +marcarConsulta(Animal, Veterinario)
    }

    class Prontuario {
        +Date data
        +String observacoes
        +String receita
        +consultarHistorico()
    }

    class Pagamento {
        +Float valor
        +Date data
        +String metodo
        +registrarPagamento(Cliente)
    }

    class Compra {
        +String descricao
        +Float valor
        +Date data
        +realizarCompra(Cliente)
    }

    Cliente "1" --> "0..*" Animal : possui
    Animal "1" --> "1" Prontuario : tem
    Veterinario "0..*" --> "1" Animal : atende
    Agenda "1" --> "0..*" Animal : agendaConsulta
    Atendente "0..*" --> "0..*" Cliente : atende
    Pagamento "0..*" --> "1" Cliente : pertence
    Compra "0..*" --> "1" Cliente : pertence
```

[Início](#sumário)

# 6. Casos de uso

<img src="./diagrama_casos_de_uso.jpg"/>

## 6.1 Histórias de usuário

### Histórias de Usuário para a Clínica Veterinária

#### Cadastro de Clientes e Animais

- **Como** um cliente,
- **Quero** me cadastrar e cadastrar meu animal,
- **Para que** eu possa utilizar os serviços da clínica.

#### Informar Condições do Animal

- **Como** um cliente,
- **Quero** informar as condições nas quais meu animal chega,
- **Para que** o veterinário possa realizar uma avaliação adequada.

#### Informar Tipo de Ração

- **Como** um cliente,
- **Quero** informar o tipo de ração que meu animal come,
- **Para que** o veterinário tenha informações relevantes sobre a dieta do meu animal.

#### Informar Hábitos do Animal

- **Como** um cliente,
- **Quero** informar os hábitos do meu animal,
- **Para que** o veterinário possa entender melhor o comportamento dele.

#### Agendamento de Atendimento

- **Como** um cliente,
- **Quero** agendar um horário para atendimento do meu animal,
- **Para que** eu possa garantir que serei atendido em um momento conveniente.

#### Atendimento e Ficha do Animal

- **Como** um atendente,
- **Quero** verificar a agenda disponível com um veterinário,
- **Para que** eu possa agendar o atendimento do cliente e seu animal.

#### Colocar na Fila de Espera

- **Como** um atendente,
- **Quero** colocar o cliente e seu animal na fila de espera,
- **Para que** eles sejam atendidos assim que houver disponibilidade.

#### Realizar Entrevista

- **Como** um veterinário,
- **Quero** realizar uma entrevista com o dono do animal,
- **Para que** eu possa coletar informações relevantes para o atendimento.

#### Registrar Resultados da Entrevista

- **Como** um veterinário,
- **Quero** registrar os resultados da entrevista em um formulário,
- **Para que** haja um histórico documentado do atendimento.

#### Examinar Animal e Registrar Observações

- **Como** um veterinário,
- **Quero** examinar o animal e registrar minhas observações no prontuário,
- **Para que** eu possa acompanhar a saúde do animal ao longo do tempo.

#### Gerar Receita

- **Como** um veterinário,
- **Quero** gerar uma receita para o animal, se necessário,
- **Para que** o cliente possa adquirir os medicamentos ou tratamentos recomendados.

#### Comprar Brinquedos

- **Como** um cliente,
- **Quero** comprar brinquedos para meu animal,
- **Para que** eu possa proporcionar momentos de diversão para ele.

#### Buscar Prontuários Antigos

- **Como** um veterinário,
- **Quero** buscar prontuários antigos para consulta,
- **Para que** eu possa verificar o histórico de atendimentos do animal.

#### Agendar Retorno

- **Como** um veterinário,
- **Quero** agendar retornos para acompanhamento do animal,
- **Para que** eu possa garantir que o animal receba a atenção contínua necessária.

#### Enviar Lembretes Automáticos

- **Como** um sistema,
- **Quero** enviar lembretes automáticos aos donos sobre retornos agendados,
- **Para que** eles não esqueçam dos compromissos.

#### Gerar Relatórios de Atendimentos

- **Como** um gerente da clínica,
- **Quero** gerar relatórios sobre atendimentos realizados por veterinário,
- **Para que** eu possa analisar o desempenho e as operações da clínica.

#### Realizar Pagamento

- **Como** um cliente,
- **Quero** pagar pelos serviços da clínica através de cartão ou dinheiro,
- **Para que** eu tenha flexibilidade nas formas de pagamento.

#### Manter Histórico de Pagamentos

- **Como** um sistema,
- **Quero** manter um histórico de pagamentos e faturamento dos clientes,
- **Para que** a clínica possa ter controle financeiro e histórico de serviços prestados.

[Início](#sumário)

# 7. Diagrama de componentes

<img src="diagrama_de_componentes.jpg">

[Início](#sumário)

# 8. Diagrama de implantação

<img src="diagrama_de_implantacao.jpg">

[Início](#sumário)

# 9. Diagramas C4

## 9.1. Diagrama de contexto

```mermaid
graph TD
    Cliente -->|Realiza cadastro e agenda| SistemaClinicaVeterinaria
    SistemaClinicaVeterinaria -->|Envio de lembretes| Cliente
    SistemaClinicaVeterinaria -->|Relatórios e prontuários| Veterinario
    Veterinario -->|Atende animal e registra prontuário| SistemaClinicaVeterinaria
    Atendente -->|Gereciamento de agenda e fila de espera| SistemaClinicaVeterinaria
    SistemaClinicaVeterinaria -->|Histórico de pagamentos| Financeiro
    SistemaClinicaVeterinaria -->|Consulta e emissão de receita| Cliente
    Cliente -->|Realiza pagamento| SistemaClinicaVeterinaria
```

## 9.2. Diagrama de container

```mermaid
graph TD
    subgraph SistemaClinicaVeterinaria
        AgendaSistema
        CadastroSistema
        ProntuarioSistema
        PagamentoSistema
        RelatorioSistema
    end

    Cliente -->|Acessa e agenda atendimento| AgendaSistema
    Cliente -->|Faz cadastro| CadastroSistema
    Veterinario -->|Consulta e registra| ProntuarioSistema
    Atendente -->|Gerencia fila de espera| AgendaSistema
    Cliente -->|Realiza pagamento| PagamentoSistema
    ProntuarioSistema -->|Gera relatórios de atendimentos| RelatorioSistema
    PagamentoSistema -->|Histórico de pagamentos| Financeiro
```

## 9.2. Diagrama de componente

```mermaid
graph TD
    subgraph CadastroSistema
        CadastroCliente
        CadastroAnimal
    end

    subgraph AgendaSistema
        AgendamentoConsulta
        FilaDeEspera
        NotificacaoAutomatica
    end

    subgraph ProntuarioSistema
        FichaAtendimento
        FormularioEntrevista
        RegistroProntuario
        EmissaoReceita
    end

    subgraph PagamentoSistema
        RegistroPagamento
        HistoricoFinanceiro
    end

    CadastroCliente --> CadastroAnimal
    CadastroAnimal --> AgendamentoConsulta
    AgendamentoConsulta --> FilaDeEspera
    FilaDeEspera --> NotificacaoAutomatica
    RegistroProntuario --> EmissaoReceita
    ProntuarioSistema --> RelatorioSistema
    RegistroPagamento --> HistoricoFinanceiro
```

## 9.2. Diagrama de código

```mermaid
classDiagram
    class Cliente {
        id: Int
        nome: String
        endereco: String
        telefone: String
        email: String
        animais: List<Animal>
    }

    class Animal {
        id: Int
        nome: String
        idade: Int
        tipo: String
        habitos: String
        tipoRacao: String
        ficha: Ficha
        prontuario: Prontuario
    }

    class Veterinario {
        id: Int
        nome: String
        especialidade: String
    }

    class Ficha {
        id: Int
        detalhes: String
        data: Date
    }

    class Prontuario {
        id: Int
        observacoes: String
        data: Date
    }

    class Agendamento {
        id: Int
        data: Date
        hora: Time
        veterinario: Veterinario
    }

    class Pagamento {
        id: Int
        data: Date
        valor: Float
        forma: String
    }

    Cliente --> Animal
    Animal --> Ficha
    Animal --> Prontuario
    Prontuario --> Agendamento
    Agendamento --> Veterinario
    Cliente --> Pagamento
```

[Início](#sumário)

# 10. Protótipo de telas

<img src="print1.png">
<img src="print2.png">
<img src="print3.png">
<img src="print4.png">

[Início](#sumário)

# 11. Diagrama de navegação de telas

```mermaid
graph TD
    Login[Login] --> Menu[Menu Principal]
    Menu --> CadastroCliente[Cadastro de Cliente]
    Menu --> CadastroAnimal[Cadastro de Animal]
    Menu --> Agenda[Agenda de Atendimentos]
    Menu --> Atendimento[Atendimento]
    Menu --> Prontuario[Consulta de Prontuários]
    Menu --> Relatorios[Relatórios]
    Menu --> Pagamentos[Pagamentos e Faturamento]
    Menu --> Lembretes[Lembretes Automáticos]
    Menu --> Loja[Loja de Produtos]

    Atendimento --> Ficha[Ficha de Atendimento]
    Atendimento --> Receita[Emissão de Receita]
    Atendimento --> Entrevista[Entrevista com o Dono]
    Atendimento --> Exame[Exame do Animal]

    Agenda --> AgendarHorario[Agendar Horário]
    Agenda --> VerificarDisponibilidade[Verificar Disponibilidade]
    Agenda --> FilaDeEspera[Fila de Espera]

    Prontuario --> ConsultaAntigos[Consultar Prontuários Antigos]

    Pagamentos --> HistoricoPagamentos[Histórico de Pagamentos]
    Pagamentos --> FormaPagamento[Forma de Pagamento]

    Lembretes --> EnvioLembretes[Envio de Lembretes]

    Relatorios --> RelatorioVeterinario[Relatório por Veterinário]
    Relatorios --> RelatorioAtendimentos[Relatório de Atendimentos]

    Loja --> CompraBrinquedos[Compra de Brinquedos]
```

[Início](#sumário)

# 12. Pilha tecnológica

```mermaid
graph TD
    subgraph Frontend
        A1[Navegador Web]
        A2[App Mobile]
    end

    subgraph Backend
        B1[Aplicação Web - Node.js/Express]
        B2[API REST - Node.js]
        B3[Gerenciamento de Autenticação - JWT/OAuth]
        B4[Serviço de Lembretes - Node.js/CRON]
    end

    subgraph Database
        C1[Banco de Dados Relacional - PostgreSQL]
        C2[Cache - Redis]
    end

    subgraph Infrastructure
        D1[Servidor Web - Nginx]
        D2[Servidor de Email - SMTP]
        D3[Servidor de Aplicação - Docker]
        D4[Hospedagem - AWS]
    end

    A1 --> B1
    A2 --> B1
    B1 --> B2
    B2 --> C1
    B2 --> C2
    B4 --> C1
    B4 --> D2
    D1 --> B1
    B1 --> D3
    D3 --> D4
```

[Início](#sumário)

# 13. Requisitos de sistemas

## 13.1. Requisitos do Cliente

Para garantir o correto funcionamento do sistema na parte do cliente, os seguintes requisitos são necessários:

### 1. Navegador Web Compatível:

O sistema é acessível através de navegadores modernos que suportem as tecnologias HTML5, CSS3 e JavaScript. Recomenda-se o uso das versões mais recentes dos seguintes navegadores:

- **Google Chrome** (versão 90 ou superior)
- **Mozilla Firefox** (versão 88 ou superior)
- **Microsoft Edge** (versão 90 ou superior)
- **Safari** (versão 14 ou superior)

### 2. Conexão à Internet:

É necessário ter uma conexão estável à internet para acessar o sistema, realizar cadastros, agendar atendimentos e utilizar todas as funcionalidades disponíveis.

### 3. Dispositivos Suportados:

O sistema é responsivo e pode ser acessado tanto em desktops quanto em dispositivos móveis, como smartphones e tablets. As seguintes especificações mínimas são recomendadas:

#### Desktop:

- **Processador**: Intel Core i3 ou equivalente
- **Memória RAM**: 4 GB
- **Resolução de Tela**: 1366x768 pixels

#### Dispositivos Móveis:

- **Sistema Operacional**: Android 8.0 ou superior, iOS 12 ou superior
- **Navegadores Compatíveis**: Versões móveis dos navegadores mencionados acima

### 4. Software Adicional:

- **JavaScript Ativado**: Necessário para o funcionamento dinâmico das páginas.
- **Cookies Habilitados**: Utilizados para manter sessões de usuários e personalizar a experiência.

## 13.2.2 Requisitos do Server Side

O ambiente de servidor deve atender aos seguintes requisitos para hospedar e operar o sistema de forma eficiente:

### 1. Hardware da Máquina Virtual

- **Memória RAM**: Mínimo de 2 GB
- **Processador**: 2 vCPUs
- **Armazenamento**: 20 GB de disco SSD
- **Largura de Banda**: 1 TB de transferência mensal

### 2. Software e Tecnologias

#### Sistema Operacional:

- **Linux** (preferencialmente distribuições como **Ubuntu 20.04 LTS** ou **Debian 10**)

#### Servidor Web:

- **Apache** (versão 2.4 ou superior)

#### Banco de Dados:

- **MySQL** (versão 5.7 ou superior)

#### Ambiente de Execução:

- **Node.js** (versão 14 ou superior) para a aplicação backend

#### Gerenciamento de Dependências:

- **npm** (Node Package Manager) ou **yarn**

#### Ferramentas de Containerização:

- **Docker** para facilitar a implantação e escalabilidade da aplicação

#### Serviços de Email:

- **SMTP Server** configurado para envio de notificações e lembretes automáticos

#### Segurança e Autenticação:

- **JWT/OAuth** para gerenciamento de autenticação e autorização

#### Serviços de Cache:

- **Redis** para otimização de desempenho e armazenamento de sessões

[Início](#sumário)

# 14. Considerações sobre segurança

## 14.1. Lado Cliente

Para garantir a segurança dos dados e a integridade das operações no lado cliente, as seguintes medidas são implementadas:

### 1. Regras de Senha

- **Complexidade**: Senhas devem conter no mínimo 8 caracteres, incluindo letras maiúsculas, minúsculas, números e caracteres especiais.
- **Validação de Captcha**: Implementação de Captcha nos formulários de cadastro e login para prevenir ataques de força bruta e bots automatizados.
- **Autenticação de Dois Fatores (2FA)**: Opção para os usuários habilitarem a 2FA, adicionando uma camada extra de segurança ao processo de login.
- **Recuperação de Senha**: Processo seguro de recuperação de senha através de links temporários enviados para o email registrado, garantindo que apenas o proprietário do email possa redefinir a senha.

### 2. Proteção contra XSS e CSRF

- **Sanitização de Inputs**: Todos os dados inseridos pelos usuários são sanitizados para prevenir ataques de **Cross-Site Scripting (XSS)**.
- **Tokens CSRF**: Implementação de tokens CSRF em formulários para prevenir ataques de **Cross-Site Request Forgery (CSRF)**.

### 3. Comunicação Segura

- **HTTPS**: Todas as comunicações entre o cliente e o servidor são criptografadas utilizando **SSL/TLS** para proteger os dados em trânsito.

### 4. Armazenamento Seguro de Dados

- **Criptografia de Dados Sensíveis**: Informações sensíveis armazenadas no navegador, como tokens de sessão, são criptografadas para evitar acessos não autorizados.

## 14.2. Lado Servidor

No lado do servidor, as seguintes práticas e políticas de segurança são adotadas:

### 1. Sistema Operacional Seguro

- Utilização de **Linux** com atualizações regulares para corrigir vulnerabilidades.

### 2. Política de Backups

- **Backup Completo**: Realizado uma vez por mês.
- **Backup Completo Quinzenal**: Realizado a cada 15 dias.
- **Backup Incremental Diário**: Realizado no final de cada dia para garantir a recuperação de dados atualizados.

### 3. Gerenciamento de Acesso

- **Princípio do Menor Privilégio**: Administradores e usuários do sistema possuem apenas as permissões necessárias para desempenhar suas funções.
- **Autenticação e Autorização**: Utilização de **JWT/OAuth** para garantir que apenas usuários autenticados e autorizados tenham acesso a determinadas funcionalidades e dados.

### 4. Proteção de Dados

- **Criptografia em Descanso**: Dados sensíveis armazenados no banco de dados são criptografados.
- **Política de Não Acesso de Admin**: Administradores do sistema não têm acesso direto aos dados dos usuários, garantindo a privacidade e confidencialidade das informações.

### 5. Monitoramento e Logs

- **Logs de Acesso e Erros**: Monitoramento contínuo dos logs para identificar e responder a atividades suspeitas ou anômalas.

### 6. Atualizações e Patches

- Aplicação regular de **atualizações de segurança** e patches para todos os softwares e dependências utilizados no servidor.

### 7. Firewall e Segurança de Rede

- **Configuração de firewall** para permitir apenas o tráfego necessário e bloquear tentativas de acesso não autorizadas.

### 8. Proteção contra Ataques DDoS

- Implementação de medidas para mitigar **ataques de negação de serviço distribuída (DDoS)**, garantindo a disponibilidade do sistema.

[Início](#sumário)

# 15. Manutenção e instalação

## 15.1. Instalado no servidor

## 15.2. Manutenção

A manutenção do sistema é essencial para garantir seu funcionamento contínuo, seguro e eficiente. As atividades de manutenção incluem:

### 1. Atualizações de Software

- Aplicação regular de atualizações de segurança para o sistema operacional, servidores web, banco de dados e dependências da aplicação.

### 2. Monitoramento de Performance

- Utilização de ferramentas de monitoramento para acompanhar a performance do servidor, identificando e resolvendo gargalos ou problemas de desempenho.

### 3. Gerenciamento de Backups

- Verificação periódica dos backups para garantir que estão sendo realizados corretamente e que os dados podem ser restaurados quando necessário.

### 4. Correção de Bugs

- Identificação e resolução de erros reportados pelos usuários ou detectados através de logs e monitoramento.

### 5. Otimização de Banco de Dados

- Realização de manutenções no banco de dados, como otimização de índices, limpeza de registros obsoletos e verificação de integridade.

### 6. Segurança Contínua

- Realização de auditorias de segurança regulares para identificar e mitigar novas vulnerabilidades.

### 7. Documentação Atualizada

- Manutenção e atualização da documentação técnica e de usuário para refletir as mudanças e atualizações no sistema.

### 8. Suporte Técnico

- Disponibilização de canais de suporte para atender dúvidas e solucionar problemas enfrentados pelos usuários.

## 15.3. Novas Funcionalidades

A adição de novas funcionalidades ao sistema deve seguir um processo estruturado para garantir sua viabilidade e alinhamento com os objetivos da clínica. As etapas para a implementação de novas funcionalidades incluem:

### 1. Formalização do Pedido

- **Requisição Formal**: Todas as solicitações de novas funcionalidades devem ser documentadas formalmente, detalhando os requisitos e os benefícios esperados.

### 2. Feedback do Cliente

- **Evitar Influências Estéticas**: O cliente pode sugerir funcionalidades com base em preferências estéticas, mas o foco deve ser na usabilidade e na funcionalidade do sistema.

### 3. Análise de Viabilidade

#### Critérios de Avaliação:

- **Disponibilidade da Equipe**: Verificar se a equipe de desenvolvimento possui tempo e recursos para implementar a nova funcionalidade.
- **Viabilidade Econômica**: Avaliar se a implementação é financeiramente viável, considerando custos e benefícios.
- **Viabilidade Tecnológica**: Determinar se a tecnologia necessária para implementar a funcionalidade está disponível e é compatível com o sistema existente.

### 4. Planejamento e Desenvolvimento

- **Design da Funcionalidade**: Criação de diagramas e protótipos para visualizar a nova funcionalidade.
- **Desenvolvimento**: Implementação da funcionalidade conforme as melhores práticas de desenvolvimento.
- **Testes**: Realização de testes rigorosos para garantir que a nova funcionalidade não introduza bugs ou vulnerabilidades no sistema.

### 5. Implantação e Treinamento

- **Deploy**: Implementação da nova funcionalidade no ambiente de produção.
- **Treinamento**: Atualização da documentação e treinamento dos usuários sobre a nova funcionalidade.

### 6. Monitoramento e Feedback

- **Avaliação de Uso**: Monitoramento do uso da nova funcionalidade para identificar possíveis melhorias.
- **Coleta de Feedback**: Recebimento de feedback dos usuários para ajustes e refinamentos futuros.

[Início](#sumário)

# 16. Treinamento

## 16.1. Usuário

## 16.1. Treinamento de Usuários

Para garantir que os usuários finais (clientes e funcionários da clínica) possam utilizar o sistema de forma eficiente e sem dificuldades, serão fornecidos os seguintes materiais e métodos de treinamento:

### Vídeos Tutoriais na Web

- **Introdução ao Sistema**: Vídeos explicando as funcionalidades básicas, como cadastro de clientes e animais, agendamento de atendimentos e consulta de prontuários.
- **Uso Avançado**: Tutoriais sobre funcionalidades mais complexas, como geração de relatórios, gestão de pagamentos e envio de lembretes automáticos.

### Manuais de Usuário

- **Documentação Detalhada**: Guias escritos que descrevem passo a passo como realizar diversas operações dentro do sistema.
- **FAQs**: Seção de perguntas frequentes para resolver dúvidas comuns dos usuários.

### Webinars e Sessões de Treinamento ao Vivo

- **Sessões Interativas**: Webinars periódicos onde os usuários podem aprender sobre novas funcionalidades e tirar dúvidas em tempo real.
- **Gravações Disponíveis**: Todas as sessões serão gravadas e disponibilizadas para consulta posterior.

### Suporte Online

- **Chat de Suporte**: Disponibilização de um canal de chat para suporte imediato durante o horário de funcionamento.
- **Sistema de Tickets**: Plataforma para que os usuários possam reportar problemas ou solicitar ajuda de forma estruturada.

### Feedback e Melhorias

- **Formulários de Feedback**: Coleta de opiniões dos usuários sobre a experiência de uso e sugestões de melhorias.
- **Atualizações Baseadas no Feedback**: Implementação de melhorias contínuas com base nas sugestões recebidas.

## 16.2. Admin

Os administradores do sistema, responsáveis pela gestão e manutenção da plataforma, receberão um treinamento mais aprofundado para garantir o pleno domínio das ferramentas e procedimentos necessários. O treinamento incluirá:

### Sessões Presenciais e Online

- **Workshops Práticos**: Sessões hands-on onde os administradores aprendem a configurar, monitorar e gerenciar o sistema.
- **Webinars Técnicos**: Palestras online sobre temas avançados, como segurança, backup e recuperação de dados.

### Documentação Técnica Detalhada

- **Guias de Administração**: Documentos que descrevem detalhadamente as tarefas administrativas, incluindo configuração de servidores, gerenciamento de usuários e monitoramento de performance.
- **Procedimentos de Backup e Recuperação**: Instruções passo a passo para realizar backups e restaurar dados em caso de necessidade.

### Acesso a Ferramentas de Monitoramento e Gestão

- **Dashboard de Administração**: Interface centralizada para monitorar o estado do sistema, visualizar logs e gerenciar recursos.
- **Ferramentas de Diagnóstico**: Software e scripts para identificar e resolver problemas técnicos rapidamente.

### Políticas de Segurança e Compliance

- **Treinamento em Segurança da Informação**: Educação sobre melhores práticas de segurança, incluindo gerenciamento de senhas, controle de acesso e proteção contra ameaças.
- **Compliance com Regulamentações**: Orientações sobre como garantir que o sistema esteja em conformidade com legislações e normas aplicáveis, como a LGPD (Lei Geral de Proteção de Dados).

### Suporte Continuado e Atualizações

- **Acesso a Suporte Técnico Especializado**: Disponibilidade de suporte para resolver dúvidas técnicas e problemas complexos.
- **Atualizações Regulares de Conhecimento**: Informações sobre novas funcionalidades, atualizações de software e mudanças na infraestrutura.

[Início](#sumário)

# 17. Glossário

[Início](#sumário)

# 18. Script SQL

## 18.1. Comandos CREATE TABLE:

```SQL
-- Tabela de Clientes
CREATE TABLE Cliente (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    endereco VARCHAR(255),
    telefone VARCHAR(20),
    email VARCHAR(100),
    CONSTRAINT UC_Cliente UNIQUE (email)
);

-- Tabela de Animais
CREATE TABLE Animal (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    especie ENUM('gato', 'cachorro') NOT NULL,
    condicoes TEXT,
    racao VARCHAR(100),
    habitos TEXT,
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id) ON DELETE CASCADE
);

-- Tabela de Veterinários
CREATE TABLE Veterinario (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    especialidade VARCHAR(100)
);

-- Tabela de Atendentes
CREATE TABLE Atendente (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    turno VARCHAR(50)
);

-- Tabela de Agenda para atendimento de animais
CREATE TABLE Agenda (
    id INT AUTO_INCREMENT PRIMARY KEY,
    data DATE NOT NULL,
    hora TIME NOT NULL,
    id_animal INT,
    id_veterinario INT,
    FOREIGN KEY (id_animal) REFERENCES Animal(id) ON DELETE CASCADE,
    FOREIGN KEY (id_veterinario) REFERENCES Veterinario(id) ON DELETE CASCADE
);

-- Tabela de Prontuários
CREATE TABLE Prontuario (
    id INT AUTO_INCREMENT PRIMARY KEY,
    id_animal INT,
    observacoes TEXT,
    receita TEXT,
    data DATE NOT NULL,
    FOREIGN KEY (id_animal) REFERENCES Animal(id) ON DELETE CASCADE
);

-- Tabela de Pagamentos
CREATE TABLE Pagamento (
    id INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    valor DECIMAL(10, 2) NOT NULL,
    data DATE NOT NULL,
    metodo ENUM('cartao', 'dinheiro') NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id) ON DELETE CASCADE
);

-- Tabela de Compras (por exemplo, brinquedos para animais)
CREATE TABLE Compra (
    id INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    descricao VARCHAR(255),
    valor DECIMAL(10, 2),
    data DATE NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id) ON DELETE CASCADE
);

-- Relacionamento de atendimento de mais de um veterinário por animal
CREATE TABLE Veterinario_Animal (
    id_veterinario INT,
    id_animal INT,
    PRIMARY KEY (id_veterinario, id_animal),
    FOREIGN KEY (id_veterinario) REFERENCES Veterinario(id) ON DELETE CASCADE,
    FOREIGN KEY (id_animal) REFERENCES Animal(id) ON DELETE CASCADE
);
```

## 18.2. Comandos INSERT gerando dados fictícios

```SQL
  -- Inserindo Clientes
INSERT INTO Cliente (nome, endereco, telefone, email)
VALUES
('João Silva', 'Rua A, 123', '11999999999', 'joao.silva@email.com'),
('Maria Souza', 'Rua B, 456', '11888888888', 'maria.souza@email.com'),
('Carlos Pereira', 'Rua C, 789', '11777777777', 'carlos.pereira@email.com');

-- Inserindo Animais
INSERT INTO Animal (nome, especie, condicoes, racao, habitos, id_cliente)
VALUES
('Rex', 'cachorro', 'Saudável', 'Ração Premium', 'Corre muito no parque', 1),
('Mimi', 'gato', 'Problema renal', 'Ração especial para rins', 'Gosta de dormir muito', 2),
('Bobby', 'cachorro', 'Sobrepeso', 'Ração light', 'Gosta de comer o dia todo', 3);

-- Inserindo Veterinários
INSERT INTO Veterinario (nome, especialidade)
VALUES
('Dr. Ricardo Lima', 'Clínico Geral'),
('Dra. Ana Torres', 'Dermatologia'),
('Dr. Marcos Almeida', 'Ortopedia');

-- Inserindo Atendentes
INSERT INTO Atendente (nome, turno)
VALUES
('Carla Mendes', 'Manhã'),
('Paulo Santos', 'Tarde');

-- Inserindo Agenda
INSERT INTO Agenda (data, hora, id_animal, id_veterinario)
VALUES
('2024-09-20', '10:30:00', 1, 1),
('2024-09-20', '14:00:00', 2, 2),
('2024-09-21', '09:00:00', 3, 3);

-- Inserindo Prontuários
INSERT INTO Prontuario (id_animal, observacoes, receita, data)
VALUES
(1, 'Animal saudável, sem alterações.', 'Vermífugo de 6 em 6 meses', '2024-09-20'),
(2, 'Animal com problemas renais, prescrito dieta especial.', 'Dieta renal e exames mensais', '2024-09-20'),
(3, 'Animal com sobrepeso. Prescrito ração light e exercícios.', 'Ração light e caminhadas diárias', '2024-09-21');

-- Inserindo Pagamentos
INSERT INTO Pagamento (id_cliente, valor, data, metodo)
VALUES
(1, 200.00, '2024-09-20', 'cartao'),
(2, 300.00, '2024-09-20', 'dinheiro'),
(3, 150.00, '2024-09-21', 'cartao');

-- Inserindo Compras
INSERT INTO Compra (id_cliente, descricao, valor, data)
VALUES
(1, 'Brinquedo de morder para cachorro', 50.00, '2024-09-20'),
(2, 'Arranhador para gatos', 80.00, '2024-09-20'),
(3, 'Coleira para cachorro', 30.00, '2024-09-21');

-- Inserindo Relacionamento entre Veterinários e Animais
INSERT INTO Veterinario_Animal (id_veterinario, id_animal)
VALUES
(1, 1),
(2, 2),
(3, 3),
(1, 3);  -- O animal 'Bobby' também é atendido por Dr. Ricardo Lima
```
