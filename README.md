# Linketinder CLI

O projeto Linketinder é uma aplicação desenvolvida em Groovy por **Vinícius Menezes Pontes**, cujo objetivo é facilitar a conexão entre empresas e candidatos cujas competências sejam compatíveis. A plataforma permite que empresas definam as habilidades desejadas para suas vagas e que candidatos com essas qualificações tenham maior visibilidade, aumentando as chances de um alinhamento eficiente no processo seletivo.

Além das funcionalidades básicas, como listar, cadastrar e excluir usuários (empresas e candidatos), o sistema também oferece a opção de "Listar Compartibilidade Empresa/Candidatos". Nessa funcionalidade, cada empresa cadastrada terá uma lista de candidatos classificados por ordem de compatibilidade. Quanto maior o número de competências em comum, maior será a posição do candidato no ranking da empresa.

No sistema, existe uma estrutura de testes unitários que garante a qualidade do código. O package tests contém o RunTests, ponto de entrada para a execução dos testes, e subpackages que avaliam as entidades (Candidate e Enterprise), o gerenciador de usuários (UserManager), além de oferecer mocks e utilitários, como o FakeScanner, para simular interações.

## Estrutura
### 📂 **data** - Dados estáticos
- `CandidatesData`: Armazena dados estáticos de candidatos (apenas para testes)
- `EnterprisesData`: Armazena dados estáticos de Empresas (apenas para testes)

### 📂 **entities** - Entidades
- `Candidate`: Classe responsável por métodos e parâmetros da entidade Candidato
- `Enterprise`: Classe responsável por métodos e parâmetros da entidade Empresa
- `User`: Interface base para usuários do sistema (candidatos e empresas)
- `SkillsList`: Define e valida as competências técnicas

### 📂 **managers** - Gerenciadores
- `UserManager`: Controla operações de CRUD para usuários (criação/exclusão)

### 📂 **services** - Lógica de negócios
- `CompatibilityService`: Implementa algoritmo de compatibilidade entre candidatos e vagas

### 📂 **utils** - Utilitários
- `GenericUtils`: Oferece funções auxiliares para processamento genérico

### 📂 **view** - Interface do usuário
- `Cli`: Implementa a interface de linha de comando (CLI) interativa

### ⚙️ **Main.groovy** - Ponto de entrada
- Classe principal que inicia a aplicação

## Estrutura - Testes Unitários

### 📂 **tests** - Testes unitários
- `RunTests`: Ponto de entrada para execução dos testes

### 📂 **tests.entities** - Testes do package entities
- `CandidateTest`: testes de todos os métodos da classe Candidate
- `EnterpriseTest`: testes de todos os métodos da classe Enterprise

### 📂 **tests.managers** - Testes do package managers
- `UserManagerTest`: testes de todos os métodos da classe UserManager

### 📂 **tests.mocks** - Mocks para os testes
- `UsersMock`: disponibiliza dados válidos e inválidos para testar as entidades Candidate e Enterprise

### 📂 **tests.utils** - Utilitários para testes
- `FakeScanner`: Simula entradas do usuário

### ⚙️ **./tests/RunTests** - Ponto de entrada
- Classe principal que inicia os testes unitários


## Pré-requisitos
- Java JDK 8+ instalado
- Groovy 4.0+ instalado

## Como Executar o Projeto
### 1. Clone o repositório

Abra o terminal e execute o comando abaixo:

```bash
git clone [URL_DO_SEU_REPOSITORIO]
```

### 2. Acesse a pasta do projeto

Navegue até o diretório do projeto clonado:

```bash
cd linketinder
```

### 3. Execute a aplicação ou os testes

Inicie a aplicação com o seguinte comando:

```bash
groovy Main.groovy
```

Para os testes unitários, inicie com o seguinte comando:

```bash
groovy ./tests/RunTests.groovy
```

### 4. Primeiros passos após a execução

Após executar a aplicação, siga as orientações abaixo:

- **Navegação:** Utilize números para navegar pelos menus.
- **Sair:** Pressione `0` para voltar ou sair de qualquer menu.

