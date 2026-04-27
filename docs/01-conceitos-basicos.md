# Conceitos Básicos de Git e GitHub

<!-- Este arquivo introduz os conceitos fundamentais de controle de versão, Git e GitHub -->

## 📋 Objetivos de Aprendizagem

<!-- Liste aqui os objetivos de aprendizagem deste capítulo -->
<!-- TODO: Adicione 3-5 objetivos de aprendizagem -->

Ao final deste capítulo, você será capaz de:

- Compreender a filosofia do controle de versão distribuído e sua importância em projetos de IA.

- Diferenciar com precisão as responsabilidades do Git (ferramenta local) e do GitHub (plataforma remota).

- Instalar, configurar sua identidade e navegar pelos estados fundamentais do Git.

- Executar o fluxo básico de preservação de histórico através de repositórios e commits.

## 🎯 Introdução

<!-- Escreva uma introdução geral sobre controle de versão e sua importância -->
<!-- Por que aprender Git? Onde é usado? -->
Imagine treinar um modelo de Deep Learning por 48 horas e, ao tentar otimizar um hiperparâmetro, você corrompe acidentalmente o script de treinamento. Sem controle de versão, seu trabalho estaria perdido. O controle de versão é a "máquina do tempo" do desenvolvedor.
Aprender Git é essencial porque a engenharia de software moderna é inerentemente colaborativa; é o padrão da indústria usado desde startups até gigantes como Google e OpenAI. Dominar essas ferramentas separa os amadores dos profissionais que conseguem gerenciar bases de código complexas e experimentos científicos de forma reprodutível e segura.

<!-- Mantenha entre 100-200 palavras -->

## O que é Controle de Versão?

<!-- TODO: Explique o que é controle de versão -->
Controle de versão (VCS) é um sistema que registra as mudanças em um arquivo ou conjunto de arquivos ao longo do tempo para que você possa recuperar versões específicas mais tarde.
<!-- Dicas:-->
- Por que precisamos de controle de versão?
Para evitar a perda de progresso e permitir que múltiplas pessoas trabalhem no mesmo arquivo sem sobrescrever o trabalho umas das outras.

- Quais problemas ele resolve?
O fim dos arquivos "projeto_final_v2_atua_REAIS.py". Ele resolve conflitos de edição e fornece auditoria (quem fez o quê e quando).

- Exemplos do dia a dia (Google Docs histórico, Ctrl+Z, etc.)
O histórico de revisões do Google Docs ou o "Ctrl+Z" persistente que sobrevive mesmo após fechar o computador.

- Diferença entre controle de versão local vs distribuído
No modelo Local, você depende de um banco de dados na sua máquina. No Distribuído (como o Git), cada desenvolvedor tem uma cópia completa do histórico do projeto, o que aumenta a segurança e permite trabalhar offline.


### Benefícios do Controle de Versão

<!-- TODO: Liste os principais benefícios -->
<!-- Exemplos: histórico completo, colaboração, backup, experimentação segura, etc. -->
- Histórico Completo: Rastreabilidade de cada linha de código.

- Colaboração em Massa: Milhares de desenvolvedores podem contribuir no mesmo projeto.

- Experimentação Segura: Crie ramificações para testar ideias sem quebrar o código principal.

- Backup Nativo: Como cada clone é um backup completo, o risco de perda total é quase nulo.

## O que é Git?

<!-- TODO: Explique o que é Git -->
O Git é um sistema de controle de versão distribuído, gratuito e de código aberto. Foi criado em 2005 por Linus Torvalds (o criador do Linux) para gerenciar o desenvolvimento do kernel do Linux, focando em velocidade, integridade de dados e suporte a fluxos de trabalho não lineares.

### Características Principais do Git

<!-- TODO: Liste as características que tornam o Git especial -->
- Distribuído: O repositório completo fica na sua máquina.

- Velocidade: Quase todas as operações são locais e instantâneas.

- Integridade: Tudo é verificado por um checksum (SHA-1) antes de ser armazenado.

- Ramificação (Branching) Leve: Criar e alternar entre branches é incrivelmente rápido.

### Como o Git Funciona?

<!-- TODO: Explique o modelo básico de funcionamento do Git -->
Diferente de outros sistemas que guardam as "diferenças" entre arquivos, o Git pensa em Snapshots (fotos instantâneas do estado do projeto).

Os Três Estados do Git:

- Working Directory: Onde você altera seus arquivos.

- Staging Area (Index): Onde você marca os arquivos que entrarão no próximo "retrato".

- Repository (.git): Onde o Git salva permanentemente os snapshots.

## O que é GitHub?

<!-- TODO: Explique o que é GitHub -->
O GitHub é uma plataforma de hospedagem de código-fonte e arquivos que utiliza o Git como motor. É a maior comunidade de desenvolvedores do mundo, funcionando como uma camada social e de gestão sobre o Git. Importante: Você pode usar o Git sem o GitHub, mas o GitHub não existe sem o Git.

### Recursos do GitHub

<!-- TODO: Liste os principais recursos do GitHub -->
- Pull Requests: Onde ocorre a revisão de código antes da integração.

- Issues: Gestão de tarefas, bugs e sugestões.

- Actions: Automação de testes e deploy (CI/CD).

- Pages: Hospedagem gratuita de sites estáticos diretamente do repositório.
  
## Diferença entre Git e GitHub

<!-- TODO: Explique claramente a diferença -->
<!-- Esta é uma confusão comum! Seja muito claro aqui -->

| Caracteristicas | GitHub | GitHub |
|-----------------|--------|--------|
| Tipo | Software de linha de comando local | Serviço de hospedagem baseado na nuvem |
| Instalação | Deve ser instalado no seu SO | Acessado via navegador ou app |
| Funcionalidade | Gerencia histórico e versões | Facilita a colaboração e gestão de projetos |
| Offline | Funciona perfeitamente sem internet | Requer internet para a maioria das funções |


### Analogia Útil

<!-- TODO: Crie uma analogia para ajudar a entender a diferença -->
<!-- Exemplo: Git é como um sistema de arquivos com histórico, GitHub é como o Google Drive para Git -->
O Git é como o seu editor de texto (Microsoft Word) onde você cria o conteúdo localmente. O GitHub é como o Google Drive ou Dropbox, onde você coloca esse conteúdo para compartilhar, receber comentários e colaborar com outros.

## Conceitos Fundamentais

### Repositório (Repository)

<!-- TODO: O que é um repositório? -->
<!-- Tipos: local vs remoto -->
É o "container" do seu projeto. Contém todos os arquivos, pastas e, principalmente, todo o histórico de alterações dentro da pasta oculta .git.

- Local: No seu computador.
- Remoto: No servidor (GitHub).

### Commit

<!-- TODO: O que é um commit? -->
<!-- Por que commits são importantes? -->
<!-- Estrutura de um commit: snapshot, mensagem, autor, timestamp -->
É a unidade básica de histórico. Um commit representa uma alteração confirmada. Ele contém:

- O Snapshot dos arquivos.
- Uma Mensagem explicando a mudança.
- Metadados (Autor, Data/Hora).
- Um hash único (ID).

### Branch

<!-- TODO: Introdução básica ao conceito de branch -->
<!-- (Explicação detalhada virá no capítulo 03) -->
Uma ramificação do projeto. Permite que você desenvolva uma funcionalidade nova em uma linha do tempo paralela sem afetar a linha principal (main).

### Histórico

<!-- TODO: O que é o histórico do Git? -->
<!-- Como visualizar? Para que serve? -->
O registro cronológico de todos os commits. É usado para auditar a evolução do software e para "voltar no tempo" se algo der errado.

### Clone vs Fork

<!-- TODO: Explique a diferença entre clone e fork -->
- Clone: Você cria uma cópia idêntica de um repositório remoto para sua máquina local (geralmente de um projeto seu ou que você tem permissão).
- Fork: Você cria uma cópia de um repositório de outra pessoa para a sua conta do GitHub. Útil para contribuir com projetos open source sem ter acesso direto ao original.

## Instalação do Git

### Windows

<!-- TODO: Como instalar Git no Windows -->
<!-- Link para download: https://git-scm.com/download/win -->
- 1. Baixe o instalador em git-scm.com/download/win.
- 2. Execute e siga o "Next, Next, Finish" (recomendo manter as opções padrão).

### macOS

<!-- TODO: Como instalar Git no macOS -->
<!-- Homebrew, Xcode, download direto -->
Abra o terminal e digite git --version. Se não estiver instalado, o macOS oferecerá a instalação automática das ferramentas de linha de comando do Xcode. Alternativamente, use o Homebrew: brew install git.

### Linux

<!-- TODO: Como instalar Git no Linux -->
<!-- Comandos para Ubuntu/Debian, Fedora, Arch -->
No Ubuntu/Debian: sudo apt update && sudo apt install git. No Fedora: sudo dnf install git.

### Verificando a Instalação

<!-- TODO: Como verificar se o Git foi instalado corretamente -->

```bash
git --version
```

## Configuração Inicial

<!-- TODO: Configure Git pela primeira vez -->

```bash
# TODO: Adicione comandos para configurar nome e email
git config --global user.name "Seu Nome Completo"
git config --global user.email "seuemail@exemplo.com"
```

### Por que Configurar Nome e Email?

<!-- TODO: Explique a importância dessas configurações -->
No mercado de IA e Software, a autoria é fundamental. Sem isso, ninguém sabe quem treinou o modelo ou quem corrigiu o bug. O GitHub usa o email para associar seus commits locais ao seu perfil online.

## Criando uma Conta no GitHub

<!-- TODO: Passo a passo para criar conta no GitHub -->

1. <!-- Passo 1 --> Acesse github.com
2. <!-- Passo 2 --> Clique em Sign Up e siga as instruções (você precisará de um email válido)
3. <!-- Passo 3 --> Verifique seu email para desbloquear todos os recursos

## Exemplos Práticos

### Exemplo 1: Cenário sem Controle de Versão

<!-- TODO: Descreva um cenário caótico sem controle de versão -->
Você está criando um modelo de Visão Computacional.
- Segunda: script.py
- Terça: script_v2.py
- Quarta: script_final.py
- Quinta: script_final_corrigido.py
- Sexta: Você apaga uma linha sem querer no script_final_corrigido.py e não lembra qual era. O projeto para.

### Exemplo 2: Mesmo Cenário com Git

<!-- TODO: Mostre como Git resolve o problema do Exemplo 1 -->
Você usa apenas script.py. Cada vez que termina uma melhoria, faz um git commit. Se apagar algo na sexta, basta dar um git checkout e o arquivo volta ao estado perfeito de quinta-feira em segundos.

## Erros Comuns

<!-- TODO: Liste erros comuns de iniciantes -->

### Erro 1: Confundir Git com GitHub

<!-- TODO: Como evitar essa confusão -->
Achar que ao instalar o Git, seu código já está na nuvem. Correção: Lembre-se que o Git é local; para subir ao GitHub, você precisa de um comando extra (git push).

### Erro 2: Não configurar nome e email

<!-- TODO: O que acontece e como corrigir -->
Isso gera commits "anônimos" que não contam pontos no seu perfil do GitHub. Correção: Rode os comandos de git config antes do primeiro commit.

## Exercícios

<!-- TODO: Crie 3-5 exercícios práticos -->

1. <!-- Exercício 1: Instalar Git e verificar versão --> Instale o Git em sua máquina e verifique se a versão é superior a 2.30.
2. <!-- Exercício 2: Configurar Git com seu nome e email --> Configure seu nome e email de forma global no terminal.
3. <!-- Exercício 3: Criar conta no GitHub --> Crie sua conta no GitHub e adicione uma foto de perfil profissional (seu "cartão de visitas").
4. <!-- Exercício 3: Criar pasta de projetos --> Crie sua primeira pasta de projeto e execute git init dentro dela.

## Recursos Adicionais

<!-- TODO: Adicione links úteis para aprofundamento -->

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Cheat Sheet do GitHub](https://training.github.com/downloads/pt_BR/github-git-cheat-sheet.pdf)

## Glossário

<!-- TODO: Defina termos importantes usados neste capítulo -->

- **Commit**: <!-- Definição --> Snapshot gravado no histórico.
- **Repository**: <!-- Definição --> Pasta controlada pelo Git.
- **Clone**: <!-- Definição --> Copiar do remoto para o local.
- **Fork**: <!-- Definição --> Copiar de um usuário para outro dentro do GitHub.

## Resumo

<!-- TODO: Faça um resumo dos pontos principais do capítulo -->
<!-- Lista de 5-8 pontos-chave que os alunos devem lembrar -->
- Git é a ferramenta; GitHub é o serviço.
- O controle de versão é essencial para a segurança e colaboração.
- O Git trabalha com "fotos" (snapshots) do projeto, não apenas diferenças de texto.
- Existem três áreas principais: working directory, staging e repository.
- Configurar nome e email é o primeiro passo para o profissionalismo.
- Um commit bem feito é a base de um projeto organizado.

---

## 👥 Contribuidores

<!-- Este conteúdo é colaborativo. Contribuidores deste arquivo: -->
<!-- Adicione seu nome quando contribuir:-->
- [@Tom-Junior](https://github.com/Tom-Junior) - Seção Todas

