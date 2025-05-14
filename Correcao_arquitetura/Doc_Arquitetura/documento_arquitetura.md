# Documento de Arquitetura

## Histórico de Revisões desde Arquivo

| Data       | Versão | Descrição                | Autor  |
| ---------- | ------ | ------------------------ | ------ |
| 13/05/2025 | 1.0    | Versão inicial           | Moacyr |
| 13/05/2025 | 1.1    | Correção                 | Cesar A. Carvalho Rodrigues |

## 1. Introdução

### 1.1 Finalidade

Apresentar o modelo de arquitetura escolhido pelo grupo

### 1.2 Escopo

[Descrição do escopo da arquitetura]

### 1.3 Definições, Acrônimos e Abreviações

Definições:

Camada de Apresentação (Frontend): A camada responsável pela interação do usuário com a aplicação, exibindo a interface e recebendo entradas do usuário.

Camada de Lógica de Negócio (Backend): A camada que contém a lógica de aplicação, como validações, cálculos e manipulação dos dados que o sistema processa.

Camada de Acesso a Dados: A camada intermediária entre a lógica de negócios e o banco de dados, garantindo a abstração do acesso aos dados.

Banco de Dados (DB): Sistema utilizado para armazenar dados persistentes, como informações sobre jogos, usuários e histórico de downloads.

API (Interface de Programação de Aplicações): Conjunto de funções e métodos que permite que componentes do sistema se comuniquem entre si e com sistemas externos.

Segurança: Conjunto de práticas e tecnologias implementadas para proteger dados e a infraestrutura da aplicação.

Acrônimos:

UI (User Interface): Interface do usuário, referindo-se à camada de apresentação que interage com o usuário final.

UX (User Experience): Experiência do usuário, a percepção geral que um usuário tem ao interagir com o sistema.

DBMS (Database Management System): Sistema de gerenciamento de banco de dados, como MySQL ou PostgreSQL, usado para armazenar os dados do sistema.

API (Application Programming Interface): Interface que permite que sistemas e componentes se comuniquem entre si.

SQL (Structured Query Language): Linguagem de consulta estruturada usada para interagir com bancos de dados relacionais.

Abreviações:

HTTP (Hypertext Transfer Protocol): Protocolo de comunicação utilizado para a transferência de dados na web.

HTTPS (Hypertext Transfer Protocol Secure): Versão segura do HTTP, que utiliza criptografia para proteger os dados transmitidos.

## 2. Representação Arquitetural

### 2.1 Modelo Arquitetural

A arquitetura em camadas é um modelo usado para organizar sistemas de forma mais clara e funcional. Ela divide o sistema em partes chamadas camadas, e cada uma delas tem uma função específica. As três camadas mais comuns são: apresentação, lógica e dados.

A camada de apresentação é onde o usuário interage com o sistema, como as telas de um site ou aplicativo. Ela mostra as informações e recebe os comandos do usuário.

A camada de lógica (ou de regras de negócio) é onde o sistema toma decisões. Por exemplo, é aqui que se calcula um desconto, se valida um login ou se processam os dados recebidos da apresentação.

A camada de dados é onde as informações são armazenadas e buscadas, geralmente em um banco de dados. Essa camada se comunica com a lógica para guardar ou recuperar dados conforme necessário.

Esse tipo de organização facilita a manutenção do sistema, melhora a clareza do código e permite que cada parte seja modificada com menos risco de afetar as outras.

### 2.2 Justificativa
Escolhemos o modelo de arquitetura em camadas porque ele se encaixa perfeitamente na estrutura de aplicações web, permitindo uma separação clara entre interface, regras de negócio e acesso a dados. Isso facilita o desenvolvimento, a manutenção e a organização do sistema. Além disso, por ser um modelo amplamente utilizado.

## 3. Metas e Restrições da Arquitetura

### 3.1 Metas

* Garantir que cada parte do sistema (interface, lógica, dados) tenha uma função bem definida.

* Facilidade de manutenção

* Permitir que alterações em uma camada possam ser feitas sem afetar as outras.

* Reutilização de código

* Aproveitar componentes em diferentes partes do sistema ou em outros projetos.

* Escalabilidade

* Possibilitar o crescimento do sistema sem necessidade de grandes reestruturações.

* Facilidade de testes

* Isolar cada camada para realizar testes mais simples e eficientes.

* Padronização

* Utilizar um modelo amplamente conhecido, facilitando a colaboração entre desenvolvedores.

* Segurança e controle de acesso

* Proteger o acesso aos dados sensíveis com camadas intermediárias, evitando acesso direto ao banco de dados.

### 3.2 Restrições

* Uso obrigatório da arquitetura em camadas

  - O sistema deve seguir a separação entre apresentação, lógica e dados.

* Tecnologias definidas previamente

 - Por exemplo: usar HTML/CSS e JavaScript na interface, Node.js ou Java na lógica, e MySQL ou PostgreSQL para os dados.

* Camadas não devem se comunicar diretamente

  - A camada de apresentação não pode acessar diretamente o banco de dados; toda comunicação deve passar pela camada de lógica.

## 4. Visão de Casos de Uso

### 4.1 Diagrama de Casos de Uso

[[Diagrama ou referência para o diagrama]](https://lucid.app/lucidchart/88ac1d04-4bfc-4dbe-82de-ed5ab5d183a2/edit?invitationId=inv_64c8dded-a238-4290-aaf9-77ffc8851854)

### 4.2 Descrição dos Casos de Uso Significativos

A arquitetura em camadas foi escolhida para dar suporte a casos de uso que exigem organização, segurança e separação de responsabilidades. Os principais casos de uso que influenciaram a escolha desta arquitetura são:

Autenticação de Usuário (Login e Logout)
Este caso de uso exige que os dados do usuário sejam validados com segurança. A camada de apresentação exibe os campos de login, a camada de lógica verifica as credenciais, e a camada de dados acessa o banco para confirmar as informações. A separação em camadas garante segurança e organização nesse processo.

Cadastro e Atualização de Dados
Tanto para cadastro de usuários quanto para atualização de informações, a arquitetura em camadas permite que a interface colete os dados, a lógica valide e aplique as regras de negócio, e a camada de dados realize o armazenamento de forma segura e eficiente.

Consulta de Informações (ex: listagem de produtos, usuários, registros)
A busca por informações exige boa organização entre camadas: a apresentação solicita os dados, a lógica trata filtros e regras de exibição, e a camada de dados realiza a consulta no banco. Isso garante flexibilidade e facilidade de manutenção.

Controle de Acesso por Permissões
Com a lógica de negócio separada, é possível implementar facilmente regras que limitam o que cada tipo de usuário pode ver ou fazer, sem expor diretamente os dados na interface.

Validação de Regras de Negócio
Regras como “não permitir cadastro com e-mail repetido” ou “calcular desconto automático” são tratadas na camada lógica, mantendo a lógica centralizada e fácil de modificar sem afetar outras partes do sistema.

## 5. Visão Lógica

### 5.1 Visão Geral

Descrição Geral da Organização Lógica do Sistema – Projeto Pangeia
O Projeto Pangeia será organizado em camadas para garantir que o sistema funcione de forma eficiente e fácil de manter. Cada camada tem uma tarefa específica, o que ajuda a manter tudo organizado e seguro.

Camada de Apresentação (Interface do Usuário)

Aqui, os usuários vão navegar no catálogo de jogos, procurar títulos, fazer login e iniciar downloads. A interface será simples e adaptada para funcionar bem em qualquer dispositivo, seja computador, tablet ou celular.

Camada de Lógica de Negócio

Esta camada cuida das regras principais do sistema, como realizar pesquisas, aplicar filtros e verificar se os arquivos para download são seguros. Também é onde o sistema controla o histórico de downloads e favoritos do usuário.

Camada de Acesso a Dados

É responsável por buscar e atualizar as informações do catálogo de jogos e dados do usuário. Quando um usuário faz uma pesquisa ou vê um jogo, é aqui que as informações são recuperadas de forma rápida e segura.

Camada de Persistência (Banco de Dados e Armazenamento de Arquivos)

Nessa camada, os dados como jogos, avaliações e informações de usuários são guardados. Também será onde os arquivos dos jogos estão armazenados, garantindo que tudo esteja seguro e disponível para download.

### 5.2 Pacotes de Design Significativos

[Descrição dos pacotes/módulos principais]

### 5.3 Diagramas de Classes

[Diagramas ou referências para os diagramas]

## 6. Visão de Processos

Descrição dos Processos e Threads do Sistema – Projeto Pangeia
No Projeto Pangeia, o sistema será estruturado para garantir que todas as operações ocorram de maneira fluida e eficiente, utilizando processos e threads para gerenciar tarefas simultâneas.

1. Processos do Sistema
Processo de Autenticação: Quando um usuário faz login, um processo será iniciado para validar as credenciais no banco de dados. Esse processo pode ser independente para garantir que o sistema continue funcionando enquanto o usuário é autenticado.

Processo de Busca e Filtros: Cada vez que o usuário realiza uma pesquisa ou aplica filtros no catálogo de jogos, um novo processo é criado para buscar as informações de maneira rápida e sem travar a interface.

Processo de Download de Arquivos: Quando um usuário inicia o download de um jogo, um processo separado gerencia o envio dos arquivos para garantir que o download aconteça sem interferir nas outras ações do sistema.

2. Threads do Sistema
Thread de Interface do Usuário (UI): A interface do usuário será gerenciada por uma thread principal. Essa thread será responsável por lidar com interações, como cliques, preenchimento de formulários e exibição de resultados de pesquisas.

Threads de Verificação de Segurança: Quando o usuário solicita o download de um jogo, o sistema cria threads para verificar se os arquivos estão livres de malware ou ameaças antes de permitir o download. Essas threads são essenciais para garantir a segurança dos usuários.

Thread de Notificação de Novos Jogos: Sempre que um novo jogo for adicionado ao catálogo, uma thread pode ser ativada para notificar os usuários ou atualizar o conteúdo de forma dinâmica na interface.

3. Gerenciamento de Conexões e Downloads Simultâneos
Para lidar com múltiplos usuários realizando downloads ao mesmo tempo, o sistema utilizará um processo de gerenciamento de conexões simultâneas. Isso garante que a plataforma seja capaz de suportar um grande número de downloads sem sobrecarregar o servidor.

## 7. Visão de Implantação

### 7.1 Diagrama de Implantação

[Diagrama ou referência para o diagrama]

### 7.2 Descrição dos Nós

[Descrição dos nós de implantação]

## 8. Visão de Implementação

### 8.1 Visão Geral

[Visão geral da implementação]

### 8.2 Camadas

1. Camada de Apresentação (Frontend)
Responsabilidade: Lida com a interação do usuário. É a interface com a qual o usuário final interage.

Função: Exibe os dados ao usuário e captura as entradas, como cliques, digitação e outras interações. Realiza a comunicação com o backend para enviar e receber dados.

2. Camada de Negócio (Backend / Lógica de Aplicação)
Responsabilidade: Processa a lógica de negócios. Essa camada executa as regras de negócios, validações e cálculos necessários para o funcionamento da aplicação.

Função: Recebe as solicitações da camada de apresentação, realiza as operações de negócio necessárias e retorna os resultados.

3. Camada de Dados (Banco de Dados)
Responsabilidade: Gerencia o armazenamento e a recuperação de dados. É onde a informação é persistida e consultada.

Função: Recebe as solicitações de leitura ou escrita de dados provenientes da camada de negócios. Garante que os dados sejam salvos de forma segura e eficiente.

4. Camada de Acesso a Dados
Responsabilidade: Fornece uma interface entre a camada de negócios e a camada de dados, facilitando a manipulação de dados de forma abstrata.

Função: Faz a tradução entre os dados que o sistema usa internamente e como esses dados são armazenados no banco. Essa camada evita que a lógica de negócios precise se preocupar com detalhes de banco de dados.

5. Camada de Segurança
Responsabilidade: Protege os dados e a infraestrutura da aplicação.

Função: Garante que as interações com a aplicação sejam feitas de forma segura, autenticando usuários, criptografando dados sensíveis e protegendo contra acessos não autorizados.

6. Camada de Integração (APIs e Serviços Externos)
Responsabilidade: Facilita a comunicação entre sistemas diferentes e integrações com serviços externos.

Função: Permite que a aplicação se conecte com serviços externos, como gateways de pagamento, APIs de redes sociais, etc. Facilita a troca de dados com outras plataformas ou sistemas.

7. Camada de Infraestrutura
Responsabilidade: Cuida da parte física ou virtual onde a aplicação é executada.

Função: Gerencia a execução e o desempenho da aplicação. Inclui servidores de aplicação, monitoramento, backup e escalabilidade.

8. Camada de Monitoramento e Logs
Responsabilidade: Monitora o desempenho da aplicação, coleta métricas e registros de eventos.

Função: Ajuda a detectar falhas, analisar o desempenho da aplicação, identificar problemas de infraestrutura ou de código e gerar relatórios de uso.

## 9. Visão de Dados

### 9.1 Modelo de Dados

## 10. Tamanho e Performance

[Objetivos e restrições de tamanho e performance]

## 11. Qualidade

[Atributos de qualidade e como são atendidos pela arquitetura]

## 12. Princípios SOLID Aplicados

[Descrição de como os princípios SOLID foram aplicados na arquitetura]

## 13. Padrões de Design Utilizados

[Descrição dos padrões de design utilizados e em quais componentes]

>[!TIP]
>Ao longo do desenvolvimento, revise este documento para garantir que a implementação esteja alinhada com a arquitetura planejada. Documente as decisões arquiteturais importantes, incluindo as alternativas consideradas e os motivos da escolha final.
