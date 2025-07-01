# VanillaCore

## Projeto de Software

---

## Stakeholders

| Nome | Cargo | E-mail |
| --- | --- | --- |
| Arthur Pietro Macaúbas da Silva | Gerente de Projeto | arthur.pietro@estudante.ifro.edu.br |
| Vanessa Vitória Cardoso | Colaborador(a) | schulercardoso123@gmail.com |
| Albert Murilo Cerozini da Silva | Colaborador(a) | murilocerozini@hotmail.com |
| Hillary Eduarda França Amaral Souza | Colaborador(a) | hillary.eduarda@estudante.ifro.edu.br |
| Pedro Candido Machado | Colaborador(a) | queila.ars@hotmail.com |

---

## Sumário

- Resumo do Projeto
- Introdução
  - Propósito deste Documento
- Descrição Geral
  - Usuários do Sistema
  - Abrangência e Sistemas Similares
  - Suposições e Dependências
- Metodologia Adotada no Desenvolvimento
- Requisitos do Software
  - Requisitos Funcionais
  - Requisitos Não Funcionais
- Prototipagem
- Diagrama de Classes
- Referências

---

## Resumo do Projeto

| Item | Descrição |
| --- | --- |
| **Nome do Projeto** | Vanilla |
| **Gerente do Projeto** | Arthur Pietro Macaúbas da Silva |
| **Principal Objetivo** | Desenvolver um sistema integrado para a GelatoItali, otimizando a gestão de vendas, estoque, pedidos e fidelização, com interfaces amigáveis. |
| **Benefícios Esperados** | - Controle eficiente de estoque com alertas automatizados;<br>- Redução de até 30% no tempo de atendimento ao cliente;<br>- Automatização de relatórios financeiros e operacionais;<br>- Aumento de 20% na retenção de clientes por meio de programas de fidelidade;<br>- Minimização de erros em pedidos presenciais e online. |
| **Início e Término Previstos** | 14/03/2025 - 07/12/2025 |

---

## Introdução

### Propósito deste Documento

Este documento detalha os requisitos, funcionalidades e restrições do **VanillaCore**, desenvolvido para a sorveteria GelatoItali. Destina-se a clientes, desenvolvedores, gerentes e stakeholders, fornecendo uma visão clara do escopo do projeto, incluindo requisitos funcionais e não funcionais, protótipos de interface e diagramas UML. Ele serve como base para o desenvolvimento, validação e entrega do sistema, alinhado às necessidades operacionais e estratégicas da GelatoItali.

---

## Descrição Geral

### Usuários do Sistema

| Usuário | Descrição |
| --- | --- |
| **Usuário Padrão** | Funcionário com acesso básico, incluindo login e visualização de pedidos. Todos os outros papéis herdam essas permissões. |
| **Gerente** | Responsável pela administração do sistema, incluindo cadastro/edição de produtos, funcionários, marcas, tamanhos, relatórios e permissões de acesso. |
| **Atendente** | Registra pedidos presenciais, aprova pedidos online e gerencia filas de atendimento. |
| **Estoquista** | Controla o estoque, registrando entradas/saídas e gerando relatórios de insumos. |
| **Cliente** | Acessa o sistema via web ou aplicativo para consultar o menu, realizar pedidos online, acompanhar status e participar de programas de fidelidade. |

### Abrangência e Sistemas Similares

O sistema Vanilla será implementado na **GelatoItali**, uma sorveteria artesanal focada em sorvetes, picolés e açaís de alta qualidade. O sistema abrangerá:

- Gestão de vendas presenciais e online com integração de pagamentos;
- Controle de estoque com rastreamento de insumos e produtos acabados;
- Relatórios detalhados de vendas, estoque e desempenho operacional;
- Programa de fidelidade para engajamento de clientes.

**Sistemas Similares**:

- **iFood**: Gestão de pedidos online e delivery, mas sem controle detalhado de estoque;
- **Trello/Jira**: Ferramentas de gestão de tarefas, sem foco em vendas ou estoque;
- **Nex/Consumer**: Sistemas de PDV para varejo, com menos ênfase em pedidos online.

### Suposições e Dependências

**Suposições**:

- A GelatoItali possui infraestrutura de internet com largura de banda mínima de 10 Mbps;
- Funcionários terão treinamento de 4 horas para uso do sistema;
- Clientes preferem acessar o sistema via smartphones (80% Android, 20% iOS).

**Dependências**:

- Integração com gateways de pagamento (Mercado Pago, PagSeguro, Stripe);
- Hardware para PDV (tablets com Android 10+ ou computadores com Windows 10+);
- APIs de entrega (ex.: Loggi, Rappi) para serviços de delivery, se implementado;
- Serviço de hospedagem em nuvem (ex.: AWS, Azure) para alta disponibilidade.

---

## Metodologia Adotada no Desenvolvimento

O projeto seguirá a metodologia **Scrum**, com sprints de 2 semanas, entregas incrementais e revisões contínuas com a GelatoItali. Ferramentas como **Jira** para gestão de tarefas e **Slack** para comunicação serão utilizadas. As práticas incluem:

- **Daily Stand-ups**: Reuniões diárias de 15 minutos para acompanhamento;
- **Sprint Planning/Review**: Planejamento no início e validação ao final de cada sprint;
- **Backlog Refinement**: Ajuste contínuo das prioridades com base no feedback.

---

## Requisitos do Software

Os requisitos foram elaborados conforme a norma **IEEE Std-830-1998**, garantindo clareza, rastreabilidade e completude.

### Requisitos Funcionais

| ID | Nome | Descrição | Prioridade |
| --- | --- | --- | --- |
| RF-001 | Cadastro de Produtos | O sistema deve permitir ao gerente cadastrar, editar e excluir produtos (sorvetes, picolés, açaís), incluindo atributos como sabor, tamanho, preço, marca, caldas e acompanhamentos. Cada produto deve ter uma imagem associada. | Alta |
| RF-002 | Gestão de Marcas | O sistema deve permitir ao gerente cadastrar, editar e excluir marcas de produtos, associando-as a sorvetes, picolés ou açaís para facilitar a organização e relatórios. | Alta |
| RF-003 | Gestão de Tamanhos | O sistema deve permitir ao gerente definir tamanhos de potes (ex.: 250ml, 500ml, 1L) para sorvetes e açaís, com preços específicos por tamanho. | Alta |
| RF-004 | Gestão de Sabores | O sistema deve permitir ao gerente cadastrar, editar e excluir sabores, vinculando-os a produtos e definindo disponibilidade sazonal. | Alta |
| RF-005 | Gestão de Caldas e Acompanhamentos | O sistema deve permitir ao gerente cadastrar, editar e excluir caldas (ex.: chocolate, morango) e acompanhamentos (ex.: granulado, frutas), com controle de estoque associado. | Alta |
| RF-006 | Gestão de Pedidos | O sistema deve permitir que atendentes registrem pedidos presenciais e clientes realizem pedidos online, com status atualizáveis (recebido, em preparo, pronto, entregue). Deve incluir opção de personalização (ex.: escolha de caldas). | Alta |
| RF-007 | Processamento de Pagamentos | O sistema deve integrar gateways de pagamento para transações via cartão (crédito/débito), Pix e dinheiro, com confirmação automática e emissão de recibos digitais. | Alta |
| RF-008 | Gestão de Estoque | O sistema deve permitir ao estoquista registrar entradas/saídas de insumos e produtos, com alertas automáticos para níveis abaixo de 10% do estoque mínimo. | Alta |
| RF-011 | Gestão de Usuários | O sistema deve permitir ao gerente cadastrar, editar e excluir contas de funcionários, definindo papéis (gerente, atendente, estoquista) e permissões. | Alta |
| RF-013 | Menu Dinâmico | O sistema deve exibir um menu online atualizado em tempo real, com filtros por categoria (sorvetes, picolés, açaís), preço e disponibilidade. | Alta |
| RF-014 | Gestão de Promoções | O sistema deve permitir ao gerente criar, editar e excluir promoções (ex.: 20% de desconto em açaís às terças-feiras), com aplicação automática no checkout. | Média |
| RF-015 | Gestão de Mesas | O sistema deve permitir ao atendente associar pedidos presenciais a mesas específicas, com visualização do status de ocupação (livre, ocupada, aguardando pagamento). | Média |
| RF-017 | Gestão de Fornecedores | O sistema deve permitir ao gerente cadastrar, editar e excluir fornecedores, associando-os a insumos para rastreamento de compras. | Média |
| RF-018 | Dashboard de Monitoramento | O sistema deve oferecer um dashboard em tempo real para o gerente, exibindo métricas como pedidos pendentes, estoque crítico e vendas do dia. | Alta |

### Requisitos Não Funcionais

| ID | Nome | Descrição | Prioridade |
| --- | --- | --- | --- |
| RNF-001 | Usabilidade | O sistema deve ter uma interface intuitiva, com navegação clara e tempo de aprendizado inferior a 30 minutos para funcionários e 10 minutos para clientes. Deve seguir diretrizes de UX (ex.: WCAG 2.1 para acessibilidade). | Alta |
| RNF-002 | Disponibilidade | O sistema deve garantir 99,9% de disponibilidade, com manutenções programadas em horários de baixa demanda (ex.: 2h às 4h). | Alta |
| RNF-003 | Desempenho | O sistema deve processar pedidos e transações em menos de 1 segundo em condições normais e suportar picos de até 1.000 requisições simultâneas. | Alta |
| RNF-004 | Segurança | Dados sensíveis (clientes, transações) devem ser protegidos com criptografia TLS 1.3, autenticação multifator para gerentes e conformidade com LGPD. | Alta |
| RNF-005 | Escalabilidade | O sistema deve suportar crescimento de 50% no volume de pedidos anuais, com arquitetura baseada em microsserviços hospedada em nuvem. | Média |
| RNF-006 | Portabilidade | O sistema deve ser acessível em navegadores (Chrome, Firefox, Safari) e dispositivos móveis (Android 10+, iOS 14+), com design responsivo. | Alta |
| RNF-007 | Manutenibilidade | O código deve seguir padrões de qualidade (ex.: Clean Code), com cobertura de testes unitários acima de 80% e documentação técnica completa. | Média |
| RNF-008 | Interoperabilidade | O sistema deve integrar-se com APIs externas (pagamentos, entregas) usando padrões RESTful e documentação Swagger/OpenAPI. | Média |
| RNF-009 | Backup e Recuperação | O sistema deve realizar backups diários automáticos, com tempo de recuperação (RTO) inferior a 4 horas em caso de falhas. | Alta |
| RNF-010 | Confiabilidade | O sistema deve garantir que 99,95% das transações sejam concluídas sem erros, com logs detalhados para auditoria. | Alta |
| RNF-011 | Internacionalização | O sistema deve suportar múltiplos idiomas (português e inglês inicialmente), com opção de expansão para espanhol, para atender turistas. | Baixa |
| RNF-012 | Consumo de Recursos | O sistema deve operar eficientemente, com uso de memória RAM inferior a 2GB e CPU abaixo de 50% em servidores padrão (ex.: AWS t3.medium). | Média |
| RNF-013 | Suporte Offline | O sistema deve permitir que atendentes registrem pedidos presenciais offline, sincronizando automaticamente quando a conexão for restaurada. | Média |
| RNF-014 | Auditoria | O sistema deve registrar todas as ações críticas (ex.: alterações de estoque, exclusão de pedidos) em logs auditáveis, com acesso restrito ao gerente. | Alta |

---

## Prototipagem

Os protótipos, desenvolvidos no **Figma**, refletem a identidade visual da GelatoItali, com paleta de cores pastéis (ex.: tons de rosa, azul claro e bege) e imagens de alta qualidade dos produtos. As principais telas incluem:

- **Página Inicial**: Menu interativo com filtros de produtos e carrinho integrado;
- **Checkout**: Interface simplificada para seleção de pagamento e personalização de pedidos;
- **Dashboard Gerencial**: Gráficos de vendas, estoque e desempenho, com exportação de relatórios;
- **Tela de Estoque**: Lista de insumos com alertas visuais para níveis críticos;
- **Área do Cliente**: Histórico de pedidos e pontos de fidelidade;
- **Tela de Promoções**: Visualização de promoções ativas e resgate de recompensas;
- **Tela de Mesas**: Mapa visual para gestão de ocupação de mesas.

Os protótipos serão validados com a GelatoItali em sprints iniciais, com ajustes baseados em feedback.

---

## Diagrama de Classes

O diagrama UML inclui as seguintes entidades principais:

- **Produto**: Atributos (id_produto, nome, sabor, tamanho, preço, marca, estoque, imagem);
- **Pedido**: Atributos (id_pedido, cliente, itens, status, valorTotal, data, canal, mesa, agendamento);
- **Cliente**: Atributos (id_cliente, nome, email, telefone, pontosFidelidade, avaliacoes);
- **Funcionário**: Atributos (id_funcionarios, nome, cargo, login, senha, permissões);
- **Marca**: Atributos (id_Marca, nome, descrição);
- **Estoque**: Atributos (id_estoque, produto, quantidade, nivelMinimo, nivelCritico);
- **Fornecedor**: Atributos (id_fornecedor, nome, contato, produtos);
- **Promocao**: Atributos (id_promocao, nome, desconto, dataInicio, dataFim, produtos).

**Relações**:

- Um **Cliente** pode ter muitos **Pedidos** (1:N);
- Um **Pedido** contém vários **Produtos** (1:N);
- Um **Funcionário** gerencia **Produtos**, **Pedidos** e **Estoque** (1:N);
- Um **Produto** pertence a uma **Marca** (N:1);
- Um **Produto** está associado a um **Estoque** (1:1);
- Um **Fornecedor** fornece vários **Insumos** (1:N);
- Uma **Promocao** aplica-se a vários **Produtos** (1:N).

---

## Referências

- UML 2.5 Specification. Object Management Group (OMG).
- IEEE Std-830-1998: Recommended Practices for Software Requirements Specifications.
- WCAG 2.1: Web Content Accessibility Guidelines.
- LGPD: Lei Geral de Proteção de Dados (Lei nº 13.709/2018).
