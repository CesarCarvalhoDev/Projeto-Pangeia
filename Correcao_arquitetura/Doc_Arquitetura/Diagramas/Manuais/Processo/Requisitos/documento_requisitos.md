# Documento de Requisitos

## Histórico de Revisões - Projeto Pangeia

| Data       | Versão | Descrição                | Autor         |
| ---------- | ------ | ------------------------ | ------------- |
| 11/03/2025 | 1.0    | Versão inicial           | Cesar Augusto |
| 13/05/2025 | 1.1    | Correção do documento    | Arthur        |

## 1. Introdução

### 1.1 Propósito

Este documento tem como objetivo definir os requisitos do sistema do projeto Pangiea, garantindo um entendimento comum entre todos os envolvidos no desenvolvimento do sistema.

### 1.2 Escopo

O Projeto Pangeia é um site que disponibilizará jogos retrô e jogos indie para download, buscando atingir o público jovem e adulto que gosta de conteúdo relacionado a games.  
O site oferecerá uma plataforma segura para aquisição de jogos, categorização de títulos e suporte técnico básico.

### 1.3 Definições, Acrônimos e Abreviações

[Lista de termos, definições, acrônimos e abreviações utilizados no documento]

## 2. Descrição Geral

O Projeto Pangeia nasce do desejo da criação de um ambiente acessível para entusiastas de jogos retrô e indie, fornecendo um meio seguro e organizado para download desses jogos. A plataforma será intuitiva e otimizada para atender diferentes perfis de jogadores. Nosso projeto também contará com um serviço de assinatura premium, que oferece ao usuário descontos (não cumulativos) exclusivos em determinados produtos e a experiência sem anúncios.

### 2.1 Perspectiva do Produto

- O sistema dependerá de servidores confiáveis para armazenar e disponibilizar os jogos para download.  
- Os jogos disponibilizados na plataforma serão fornecidos por desenvolvedores parceiros ou adquiridos de fontes autorizadas.  
- O sistema exigirá uma conexão com a internet para acessar o catálogo de jogos e efetuar downloads.  
- A manutenção e atualização do site dependerão de uma equipe técnica responsável.

### 2.2 Funcionalidades do Produto

- Disponibilizar jogos retrô e indie para download  
- Oferecer filtros e categorias para facilitar a busca por jogos  
- Permitir cadastro de usuários para acesso personalizado  

### 2.3 Características dos Usuários

| Tipo de Usuário  | Descrição                    | Responsabilidades                      | Nível Técnico |
|------------------|------------------------------|----------------------------------------|----------------|
| Jogadores        | Usuários que fazem download  | Buscar, baixar e avaliar jogos         | Básico         |
| Desenvolvedores  | Criadores de jogos indie     | Publicar jogos e gerenciar conteúdos   | Básico         |
| Administradores  | Gerenciamento da plataforma  | Moderar conteúdo e gerenciar usuários  | Intermediário  |

### 2.4 Restrições

- Apenas desenvolvedores cadastrados poderão subir novos jogos  
- A plataforma só suportará jogos licenciados

## 3. Requisitos Específicos

### 3.1 Requisitos Funcionais

| ID     | Descrição                                                                  | Prioridade | Origem     |
|--------|----------------------------------------------------------------------------|------------|------------|
| RF001  | O sistema deve permitir o download de jogos                                | Alta       | Usuários   |
| RF002  | O sistema deve possibilitar a busca por jogos                              | Alta       | Usuários   |
| RF003  | O sistema deve permitir a categorização de jogos por gênero e popularidade | Média      | Plataforma |

#### 3.1.1 Área Funcional 1  

| ID     | Descrição                                      | Prioridade | Origem    |
|--------|------------------------------------------------|------------|-----------|
| RF004  | O sistema deve permitir o cadastro de usuários | Alta       | Plataforma|
| RF005  | O sistema deve garantir autenticação segura    | Alta       | Segurança |

### 3.2 Requisitos Não Funcionais

#### 3.2.1 Requisitos de Desempenho  

| ID      | Descrição                                   | Critério de Aceitação               | Prioridade |
|---------|---------------------------------------------|-------------------------------------|------------|
| RNF001  | O site deve carregar em menos de 3 segundos | Tempo médio de carregamento ≤ 3s    | Alta       |
| RNF002  | Suportar até 10.000 acessos simultâneos     | Testes de carga devem ser aprovados | Média      |

#### 3.2.2 Requisitos de Segurança  

| ID      | Descrição                          | Critério de Aceitação             | Prioridade |
|---------|------------------------------------|-----------------------------------|------------|
| RNF004  | Proteção contra ataques de injeção SQL | Testes de segurança aprovados | Alta       |

#### 3.2.3 Requisitos de Usabilidade  

| ID      | Descrição                                  | Critério de Aceitação          | Prioridade |
|---------|---------------------------------------------|--------------------------------|------------|
| RNF005  | Interface responsiva para dispositivos móveis | Testado em múltiplos dispositivos | Alta    |
| RNF006  | Design intuitivo para fácil navegação       | Testes de usabilidade aprovados  | Média    |


## 4. Visão Geral do Sistema

O Projeto Pangeia é uma plataforma online para download de jogos retrô e indie, voltada a jovens e adultos. Oferece filtros de busca, cadastro de usuários, e assinatura premium com benefícios como descontos e navegação sem anúncios.
Usuários incluem jogadores, desenvolvedores e administradores. O sistema será seguro, rápido e responsivo, com foco em usabilidade e desempenho.

## 5. Casos de Uso

Cadastrar Usuário – Visitante cria uma conta.
Autenticar Usuário – Usuário faz login na plataforma.
Buscar Jogos – Usuário pesquisa jogos por nome, gênero ou popularidade.
Baixar Jogo – Jogador baixa jogos disponíveis.
Publicar Jogo – Desenvolvedor envia um novo jogo.
Gerenciar Conteúdo – Administrador modera jogos e usuários.
Assinar Premium – Jogador adquire plano premium para benefícios extras.

## 6. Priorização de Requisitos

Prioridade Alta:
Download de jogos
Busca por jogos
Cadastro e login seguro
Site rápido (≤ 3s)
Proteção contra ataques
Interface responsiva

Prioridade Média:
Categorização por gênero/popularidade
Suporte a 10.000 acessos simultâneos
Design intuitivo

Prioridade Baixa:
Melhorias e customizações

## 7. Aprovação

| Nome          | Papel        | Assinatura | Data       |
| ------------- | ------------ | ---------- | ---------- |
| Cesar Augusto | Scrum Master |            | 13/05/2025 |
| Arthr         | P.O.         |            | 13/05/2025 |

>[!NOTE]
>Este documento será atualizado incrementalmente ao longo do desenvolvimento do projeto.
