# Documento de Requisitos  
## Projeto Integrador - Engenharia de Software  
**Equipe:** [Nome da Equipe]  
**Data:** Invalid Date  

---

## Tabela de Conteúdo  
- [Histórico de Revisões](#histórico-de-revisões)  
- [Introdução](#introdução)  
- [Descrição Geral](#descrição-geral)  
- [Requisitos Específicos](#requisitos-específicos)  
- [Interfaces Externas](#interfaces-externas)  
- [Outros Requisitos](#outros-requisitos)  
- [Apêndices](#apêndices)  

---

## Histórico de Revisões

| Versão | Data       | Descrição       | Autor         |
|--------|------------|------------------|----------------|
| 1.0    | 11/03/2025 | Versão inicial   | Cesar Augusto  |

---

## Introdução

### 1.1 Propósito do Documento  
Este documento tem como objetivo definir os requisitos do sistema do Projeto Pangeia, garantindo um entendimento comum entre todos os envolvidos no desenvolvimento do sistema.

### 1.2 Escopo do Projeto  
O Projeto Pangeia é um site que disponibilizará jogos retrô e jogos indie para download, buscando atingir o público jovem e adulto que gosta de conteúdo relacionado a games.  
O site oferecerá uma plataforma segura para aquisição de jogos, categorização de títulos e suporte técnico básico.

**Fora do escopo:**  
- O projeto não incluirá desenvolvimento de jogos próprios.  
- O projeto não incluirá serviços de streaming de jogos.

### 1.3 Definições, Acrônimos e Abreviações  

| Termo         | Definição                                      |
|---------------|-------------------------------------------------|
| Jogos retrô   | Jogos clássicos lançados em plataformas antigas |
| Jogos indie   | Jogos desenvolvidos de forma independente       |
| Download      | Ação de obter um jogo para armazenamento local  |
| Plataforma    | O site do Projeto Pangeia                       |

### 1.4 Visão Geral do Documento  
Este documento contém a definição dos requisitos do sistema, incluindo a descrição geral, requisitos funcionais e não funcionais, regras de negócio e interfaces externas.

---

## Descrição Geral

### 2.1 Contexto do Produto  
O Projeto Pangeia nasce da necessidade de criar um ambiente acessível para entusiastas de jogos retrô e indie, fornecendo um meio seguro e organizado para download desses jogos. A plataforma será intuitiva e otimizada para atender diferentes perfis de jogadores.

### 2.2 Funções do Produto  
- Disponibilizar jogos retrô e indie para download  
- Oferecer filtros e categorias para facilitar a busca por jogos  
- Permitir cadastro de usuários para acesso personalizado  

### 2.3 Características dos Usuários  

| Tipo de Usuário | Descrição                    | Responsabilidades                     | Nível Técnico |
|------------------|------------------------------|----------------------------------------|----------------|
| Jogadores        | Usuários que fazem download  | Buscar, baixar e avaliar jogos         | Básico         |
| Desenvolvedores  | Criadores de jogos indie     | Publicar jogos e gerenciar conteúdos   | Básico         |
| Administradores  | Gerenciamento da plataforma  | Moderar conteúdo e gerenciar usuários  | Intermediário  |

### 2.4 Restrições Gerais  
- Apenas desenvolvedores cadastrados poderão subir novos jogos  
- A plataforma só suportará jogos grátis  

### 2.5 Suposições e Dependências  
- O sistema dependerá de servidores confiáveis para armazenar e disponibilizar os jogos para download.  
- Os jogos disponibilizados na plataforma serão fornecidos por desenvolvedores parceiros ou adquiridos de fontes autorizadas.  
- O sistema exigirá uma conexão com a internet para acessar o catálogo de jogos e efetuar downloads.  
- A manutenção e atualização do site dependerão de uma equipe técnica responsável.

---

## Requisitos Específicos

### 3.1 Requisitos Funcionais  

| ID     | Descrição                                                    | Prioridade | Origem     |
|--------|---------------------------------------------------------------|------------|------------|
| RF001  | O sistema deve permitir o download de jogos                  | Alta       | Usuários   |
| RF002  | O sistema deve possibilitar a busca por jogos                | Alta       | Usuários   |
| RF003  | O sistema deve permitir a categorização de jogos por gênero e popularidade | Média | Plataforma |

#### 3.1.1 Área Funcional 1  

| ID     | Descrição                                    | Prioridade | Origem    |
|--------|-----------------------------------------------|------------|-----------|
| RF004  | O sistema deve permitir o cadastro de usuários | Alta       | Plataforma|
| RF005  | O sistema deve garantir autenticação segura    | Alta       | Segurança |

### 3.2 Requisitos Não-Funcionais  

#### 3.2.1 Requisitos de Desempenho  

| ID      | Descrição                          | Critério de Aceitação                | Prioridade |
|---------|------------------------------------|--------------------------------------|------------|
| RNF001  | O site deve carregar em menos de 3 segundos | Tempo médio de carregamento ≤ 3s | Alta       |
| RNF002  | Suportar até 10.000 acessos simultâneos     | Testes de carga devem ser aprovados | Média      |

#### 3.2.2 Requisitos de Segurança  

| ID      | Descrição                          | Critério de Aceitação         | Prioridade |
|---------|------------------------------------|-------------------------------|------------|
| RNF004  | Proteção contra ataques de injeção SQL | Testes de segurança aprovados | Alta       |

#### 3.2.3 Requisitos de Usabilidade  

| ID      | Descrição                                  | Critério de Aceitação          | Prioridade |
|---------|---------------------------------------------|--------------------------------|------------|
| RNF005  | Interface responsiva para dispositivos móveis | Testado em múltiplos dispositivos | Alta    |
| RNF006  | Design intuitivo para fácil navegação       | Testes de usabilidade aprovados  | Média    |

### 3.3 Regras de Negócio  

| ID    | Descrição                                                                |
|-------|-------------------------------------------------------------------------|
| RN001 | Apenas usuários cadastrados podem baixar jogos pagos                    |
| RN002 | Desenvolvedores devem passar por validação antes de publicar jogos      |
| RN003 | A plataforma apenas disponibiliza downloads e não executa jogos         |

---

## Interfaces Externas

### 4.1 Interfaces de Usuário  
- Interface web responsiva com menus intuitivos  
- Páginas de jogos com descrições e botões de download  

### 4.2 Interfaces de Hardware  
- Compatível com computadores e dispositivos móveis  

### 4.3 Interfaces de Software  
- Integração com gateways de pagamento  
- Integração com APIs de autenticação  

### 4.4 Interfaces de Comunicação  
- Notificações por e-mail para atualizações de jogos  

---

## Outros Requisitos  
- Política de privacidade e termos de uso devem ser apresentados aos usuários  

---

## Apêndices

### 6.1 Glossário  
**Download:** Ação de obter um jogo para armazenamento local  

### 6.2 Modelo Conceitual  
*[Inclua diagramas do modelo conceitual, como diagrama de classes, modelo ER, etc.]*  

### 6.3 Protótipos de Interface  
*[Inclua mockups ou protótipos da interface do usuário, se aplicável.]*  

### 6.4 Material de Suporte  
*[Liste qualquer material de suporte ou referências utilizadas na elaboração deste documento]*  

## Por que escolhemos esse modelo

Escolhemos o **Modelo em Camadas** por ser uma abordagem consolidada, de fácil implementação e adequada ao escopo do Projeto Pangeia. Este modelo oferece diversas vantagens que o tornam ideal para nosso caso:

- **Separação de responsabilidades:** facilita a manutenção, teste e evolução de cada parte do sistema de forma independente.

- **Facilidade de desenvolvimento em equipe:** como as camadas são bem definidas, diferentes membros da equipe podem trabalhar simultaneamente em partes distintas do sistema.

- **Escalabilidade:** o modelo permite futuras expansões, como a adição de novos módulos ou funcionalidades, sem comprometer a estrutura atual.

- **Aderência aos requisitos técnicos:** considerando que o projeto envolve interface web, autenticação, categorização e gerenciamento de conteúdo, o modelo em camadas garante a organização ideal para atender esses requisitos com clareza e eficiência.

## Componentes e Módulos

### O que são Componentes e Módulos?

- **Módulo:** uma unidade lógica do sistema, geralmente agrupada por responsabilidade ou funcionalidade.  
  Ex: *"módulo de autenticação"*, *"módulo de catálogo de jogos"*.

- **Componente:** um bloco físico ou técnico (classe, serviço, pacote ou micro serviço) que implementa as funcionalidades de um ou mais módulos.

> Em muitos contextos, os termos são usados como sinônimos, mas é útil pensar que **"módulo" é a visão lógica** e **"componente" é a visão mais concreta/implementada**.

---

### Exemplos para o Projeto Pangeia

Para o site de jogos retrô e indie, uma possível divisão de módulos e componentes seria:

| Módulo                     | Responsabilidade                                       | Componentes Possíveis                          |
|----------------------------|--------------------------------------------------------|------------------------------------------------|
| **Catálogo de Jogos**      | Listar, filtrar e categorizar jogos                   | Componente de busca, componente de exibição de jogos |
| **Gestão de Usuários**     | Cadastro, login, edição de perfil                     | API de autenticação, base de dados de usuários |
| **Gerenciamento de Conteúdo** | Desenvolvedores publicam e atualizam jogos          | Painel do desenvolvedor, upload handler        |
| **Download de Jogos**      | Permitir que usuários façam download seguro           | Servidor de arquivos, verificador de integridade |
| **Administração da Plataforma** | Moderação de conteúdo, gerenciamento de usuários | Painel do admin, logs e alertas                |
| **Notificações**           | Enviar e-mails com novidades e atualizações           | Serviço de e-mail, fila de mensagens           |

---

### Benefícios de Definir Componentes e Módulos

- **Organização:** facilita entender o sistema como um todo.
- **Escalabilidade:** permite dividir tarefas entre equipes ou escalar partes específicas.
- **Reutilização:** módulos podem ser reaproveitados em outros projetos.
- **Manutenção:** mais fácil corrigir ou atualizar partes isoladas do sistema.

## Interfaces por Funcionalidade

### 1. Cadastro de Usuário
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** O usuário acessa uma tela de cadastro, insere e-mail e senha.
- **Lógica de Negócio (Negócio):** Os dados são validados (formato do e-mail, força da senha), verificados se já existem no sistema, e é acionada a lógica de envio de confirmação.
- **Acesso a Dados (Dados):** A senha é criptografada e os dados são salvos no banco de dados.
- **Serviço Externo (Email):** É disparado um e-mail de confirmação ao usuário.

### 2. Login Seguro
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** Tela de login com campos de e-mail e senha.
- **Lógica de Negócio (Negócio):** Autentica os dados, verifica tentativas falhas e bloqueia se necessário.
- **Acesso a Dados (Dados):** Verifica o usuário e a senha no banco de dados.
- **Serviço Externo (Email):** Envia e-mail de redefinição de senha caso solicitado.

### 3. Download de Jogos
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** O usuário clica no botão de download de um jogo.
- **Lógica de Negócio (Negócio):** Verifica permissões e inicia o processo de download.
- **Acesso a Dados (Dados):** Busca o arquivo e registra o download.
- **Serviço Externo:** Notifica o usuário com mensagem de conclusão do download.

### 4. Busca de Jogos
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** O usuário digita termos no campo de busca e aplica filtros.
- **Lógica de Negócio (Negócio):** Interpreta os filtros e monta a consulta.
- **Acesso a Dados (Dados):** Executa a busca no banco e retorna os jogos.

### 5. Categorização de Jogos
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** O usuário acessa o menu de categorias.
- **Lógica de Negócio (Negócio):** Solicita as categorias e jogos vinculados.
- **Acesso a Dados (Dados):** Retorna os jogos organizados por categoria.

### 6. Avaliação de Jogos
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** O usuário preenche nota e comentário.
- **Lógica de Negócio (Negócio):** Valida a nota, grava o comentário e recalcula a média.
- **Acesso a Dados (Dados):** Armazena a avaliação e atualiza a média.

### 7. Interface Responsiva
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** Adapta automaticamente o layout ao dispositivo.
- **Lógica de Negócio (Negócio):** Sem interação direta.
- **Acesso a Dados (Dados):** Sem interação direta.

### 8. Segurança de Downloads
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** Sem interação direta.
- **Lógica de Negócio (Negócio):** Realiza verificação de segurança nos arquivos.
- **Acesso a Dados (Dados):** Permite download apenas de arquivos verificados.
- **Serviço Externo:** Notifica administradores sobre riscos ou bloqueios.

### 9. Histórico de Downloads
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** Usuário visualiza a lista de downloads anteriores.
- **Lógica de Negócio (Negócio):** Solicita o histórico com base no ID do usuário.
- **Acesso a Dados (Dados):** Retorna todos os jogos baixados anteriormente.

### 10. Notificações de Novos Jogos
**Fluxo de Interação entre Camadas:**
- **Interface Visual (Apresentação):** Exibe notificações no painel ou permite ativar/desativar alertas.
- **Lógica de Negócio (Negócio):** Compara preferências com novos jogos adicionados.
- **Acesso a Dados (Dados):** Busca jogos novos e dados do usuário.
- **Serviço Externo (Email/Site):** Envia notificações por e-mail ou exibe internamente no site.

## 6. Infraestrutura e Tecnologia

### 6.1 O que é Infraestrutura?

A infraestrutura envolve os ambientes onde o sistema será executado e os recursos necessários para isso, como:

- **a) Servidores:** Onde a aplicação será hospedada (ex: Heroku, AWS, DigitalOcean). Pode ser físico (local) ou na nuvem (recomendado).
- **b) Banco de Dados:** Local onde serão armazenadas as informações (usuários, jogos, downloads). Exemplos: PostgreSQL, MySQL, MongoDB, Firebase.
- **c) Serviços de Armazenamento:** Para armazenar os arquivos dos jogos. Exemplos: Amazon S3, Google Cloud Storage, servidor FTP.
- **d) Hospedagem de Front-End:** Onde a interface do usuário (HTML, CSS, JS) ficará disponível. Exemplos: Vercel, Netlify, GitHub Pages.
- **e) Monitoramento e Logs:** Para acompanhar erros, acessos e saúde do sistema. Exemplos: Loggly, Grafana, Sentry.

### 6.2 O que é Tecnologia?

Tecnologia são as linguagens, frameworks, bibliotecas e ferramentas utilizadas no desenvolvimento e manutenção do sistema.

#### a) Tecnologias de Desenvolvimento

| Camada        | Tecnologias Comuns                       |
|---------------|------------------------------------------|
| Front-End     | React, Vue, Angular, HTML/CSS/JS         |
| Back-End      | Node.js, Django, Flask, Spring Boot      |
| Banco de Dados| PostgreSQL, MySQL, MongoDB, Firebase     |
| Armazenamento | Amazon S3, Google Drive API, Firebase Storage |

#### b) Tecnologias de Suporte

- **Controle de Versão:** Git (GitHub, GitLab)
- **CI/CD:** GitHub Actions, GitLab CI, Jenkins
- **Docker:** Para containerização do app, se necessário
- **APIs:** Para autenticação, pagamento, envio de e-mails etc.

### 6.3 Exemplo para o Projeto Pangeia

| Componente              | Tecnologia Escolhida        | Justificativa                                      |
|-------------------------|-----------------------------|----------------------------------------------------|
| Front-End               | React + Tailwind            | Interface moderna, responsiva e escalável          |
| Back-End                | Node.js com Express         | Leve, rápido e fácil de integrar com APIs          |
| Banco de Dados          | PostgreSQL                  | Relacional, robusto e gratuito                     |
| Armazenamento de Jogos  | Firebase Storage            | Fácil de integrar e seguro                         |
| Hospedagem              | Vercel (front) + Render (API)| Fácil de usar e gratuito para estudantes           |
| Autenticação            | Firebase Auth ou Auth0      | Gestão segura de usuários                          |
| CI/CD                   | GitHub Actions              | Deploy automático em push                          |

### 6.4 Descrição Resumida

A infraestrutura será baseada em serviços em nuvem gratuitos e escaláveis. O front-end será desenvolvido em React e hospedado no Vercel. O back-end usará Node.js com Express e será hospedado na plataforma Render. O banco de dados será PostgreSQL hospedado na própria Render. Os jogos serão armazenados no Firebase Storage. A autenticação será feita via Firebase Authentication. O pipeline de CI/CD será implementado com GitHub Actions.

## 7. Aspectos Transversais

Aspectos transversais são preocupações comuns a todo o sistema, independentemente de funcionalidades específicas. Eles não são funcionalidades centrais, mas são essenciais para garantir segurança, estabilidade, desempenho e manutenção eficiente.

### 7.1 Segurança

- **Autenticação:** Verifica a identidade do usuário (ex: login seguro).
- **Autorização:** Define o que o usuário pode ou não fazer (ex: apenas desenvolvedores podem publicar jogos).
- **Criptografia:** Protege dados sensíveis tanto em trânsito quanto em repouso.
- **Validação de entradas:** Evita ataques como injeção de SQL, XSS, entre outros.

**No Projeto Pangeia:**  
Autenticação segura com Firebase Auth, validação de dados de usuários e desenvolvedores, e proteção contra ataques.

### 7.2 Escalabilidade

Capacidade do sistema de crescer e atender a um número maior de usuários e requisições sem perda de desempenho.

- **Técnicas usadas:** balanceamento de carga, cache, filas de mensagens, uso de microserviços.

**No Projeto Pangeia:**  
O sistema deverá suportar até 10.000 acessos simultâneos, inclusive múltiplos downloads ao mesmo tempo.

### 7.3 Resiliência

Capacidade de continuar funcionando ou se recuperar de falhas inesperadas.

- **Técnicas comuns:** circuit breaker, timeouts, retries automáticos, fallbacks.

**Exemplo:**  
Se o serviço de envio de e-mails falhar, o sistema continua funcionando e tenta reenviar mais tarde.

### 7.4 Observabilidade

Capacidade de monitorar e entender o comportamento interno do sistema.

- **Inclui:**
  - Logs detalhados
  - Métricas de desempenho (CPU, memória, tempo de resposta, etc.)
  - Tracing de requisições em sistemas distribuídos

**No Projeto Pangeia:**  
Monitoramento dos jogos mais baixados, identificação de falhas, análise de tempo de resposta e uso de recursos.

---

### Por que cuidar desses aspectos?

- Garantem **qualidade**, **confiabilidade** e **escalabilidade** do sistema.
- São fundamentais para **produção** com muitos usuários.
- Facilitam **manutenção**, **suporte técnico**, **auditorias** e conformidade com legislações como a **LGPD**.

## 8. Deployment e CI/CD

### O que é Deployment?

Deployment (implantação) é o processo de colocar a aplicação pronta e testada em um ambiente acessível pelos usuários, como um servidor na nuvem ou local.

#### Tipos de Deployment:
- **Manual:** Feito manualmente, com uploads e configurações — **não recomendado**.
- **Automatizado:** Utiliza ferramentas para empacotar, testar e implantar a aplicação com rapidez e segurança.

---

### O que é CI/CD?

CI/CD significa:

- **CI (Continuous Integration):** Integração contínua. Toda vez que há uma mudança no código, testes e verificações são executados automaticamente.
- **CD (Continuous Delivery/Deployment):**
  - **Delivery:** Sistema fica pronto para ser implantado.
  - **Deployment:** Sistema é implantado automaticamente após os testes.

---

### Como planejar o CI/CD e Deployment?

#### 1. Controle de Versão

- **Git** com serviços como GitHub, GitLab ou Bitbucket.

#### 2. Ferramenta de CI/CD

- GitHub Actions  
- GitLab CI  
- Jenkins  
- CircleCI  
- Bitbucket Pipelines  

#### 3. Pipeline de CI/CD (Exemplo)

```yaml
name: Deploy Pangeia

on:
  push:
    branches: [main]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install dependencies
        run: npm install
      - name: Run tests
        run: npm test
      - name: Deploy to server
        run: ssh user@server 'cd /app && git pull && npm install && pm2 restart pangeia'

## 9. Documentação da Arquitetura

### Por que documentar a arquitetura?

- Facilita a comunicação entre membros da equipe.
- Acelera o processo de onboarding de novos desenvolvedores.
- Deixa claro o raciocínio por trás das decisões técnicas.
- Serve como referência futura para manutenção ou apresentação acadêmica.

---

### O que incluir na documentação de arquitetura?

#### 1. Visão Geral da Arquitetura

Exemplo:  
*“A arquitetura do Projeto Pangeia segue o modelo em camadas, com front-end em React, back-end em Node.js (Express), banco de dados relacional PostgreSQL e armazenamento de arquivos no Firebase Storage. A aplicação é hospedada em serviços em nuvem como Vercel (front) e Render (API).”*

---

#### 2. Visões Arquiteturais (Modelos e Diagramas)

- **a) Diagrama de Componentes (ou C4 - Nível 2):**  
  Mostra como os principais contêineres (front-end, API, banco de dados, autenticação etc.) se comunicam.

- **b) Diagrama de Sequência:**  
  Mostra o fluxo detalhado de uma funcionalidade, como "download de jogo" ou "login seguro".

- **c) Diagrama de Implantação:**  
  Exibe como os serviços estão distribuídos na infraestrutura: servidores, nuvem, containers etc.

- **d) Diagrama de Classes (opcional):**  
  Se a aplicação for orientada a objetos, esse diagrama mostra as entidades e seus relacionamentos.

---

#### 3. Decisões Arquiteturais

Exemplos:

- “Escolhemos **Node.js** por ser leve e ter uma comunidade ativa.”
- “Optamos por **Render** e **Vercel** por oferecerem planos gratuitos e integrarem bem com GitHub.”
- “Decidimos não usar microsserviços, visando simplicidade e facilidade de manutenção.”

---

#### 4. Tecnologias Utilizadas

| Camada         | Tecnologias               |
|----------------|---------------------------|
| Front-End      | React + Tailwind CSS      |
| Back-End       | Node.js com Express       |
| Banco de Dados | PostgreSQL                |
| Armazenamento  | Firebase Storage          |
| Autenticação   | Firebase Authentication   |
| CI/CD          | GitHub Actions            |

---

#### 5. Aspectos Transversais

- **Segurança:** autenticação, criptografia, validação de entrada.
- **Escalabilidade:** estrutura pensada para crescimento (ex: cloud, CI/CD).
- **Resiliência:** tentativa de reenvio de e-mails, tratamento de falhas.
- **Observabilidade**
