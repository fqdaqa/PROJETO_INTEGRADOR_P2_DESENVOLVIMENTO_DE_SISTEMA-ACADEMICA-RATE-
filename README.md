# Rate+ Sistema de Gestão Acadêmica

Bem-vindo ao Rate+ Sistema de Gestão Acadêmica! Esta aplicação web moderna foi desenvolvida para auxiliar instituições de ensino na gestão de alunos, cursos, docentes e na obtenção de insights sobre o desempenho estudantil através de inteligência artificial.

## Tecnologias Utilizadas

O Rate+ é construído com um conjunto de tecnologias robustas e eficientes, incluindo:

*   **Next.js:** Framework React para renderização no servidor e geração de sites estáticos (utilizando o App Router).
*   **React:** Biblioteca JavaScript para construção de interfaces de usuário componentizadas.
*   **ShadCN UI:** Coleção de componentes de UI elegantes e reutilizáveis.
*   **Tailwind CSS:** Framework CSS utility-first para estilização rápida.
*   **Genkit (com Google AI):** Para funcionalidades de Inteligência Artificial, como análise de desempenho.
*   **TypeScript:** Superset do JavaScript que adiciona tipagem estática.
*   **Lucide React:** Biblioteca de ícones SVG.
*   **Zod & React Hook Form:** Para gerenciamento e validação de formulários.

## Como Usar o Sistema: Um Guia Rápido

### 1. Autenticação: A Porta de Entrada

Para garantir a segurança dos dados, o primeiro passo é sempre a autenticação.

*   **Login:** Ao acessar o sistema, você verá a tela de login. Insira seu email e senha cadastrados para entrar.
*   **Primeiro Acesso?** Se for seu primeiro acesso, clique em "Primeiro acesso? Cadastre-se". Você preencherá um formulário simples (nome, email, senha) e, após o cadastro, será redirecionado para a tela de login.
*   **Esqueceu a Senha?** Se não se lembra da sua senha, clique em "Esqueceu sua senha?". Informe seu email para receber as instruções de recuperação (funcionalidade simulada).
*   **Sair (Logout):** Dentro do sistema, clique no ícone de perfil no canto superior direito e selecione "Sair" para encerrar sua sessão com segurança.

### 2. Painel Principal (Dashboard)

Após o login, você chegará ao Painel. Ele é o seu ponto de partida e oferece atalhos para as áreas mais importantes:

*   **Gerenciar Usuários:** Para visualizar e administrar todas as contas.
*   **Catálogo de Cursos:** Para gerenciar os cursos oferecidos.
*   **Desempenho dos Alunos:** Para usar a ferramenta de análise com Inteligência Artificial.

### 3. Gerenciamento de Usuários

Esta seção é o coração administrativo do sistema, permitindo o controle total sobre quem tem acesso.

*   **Como Acessar:** Pelo atalho no Painel ou clicando em "Usuários" no menu lateral.
*   **O que você pode fazer:**
    *   **Visualizar:** Veja uma tabela com todos os usuários (alunos, professores e administradores), incluindo nome, email e perfil.
    *   **Pesquisar e Ordenar:** Use a barra de busca para encontrar alguém rapidamente ou clique nos títulos das colunas para ordenar a lista.
    *   **Adicionar Usuário:** Clique no botão "Adicionar Usuário". Um formulário completo aparecerá para você cadastrar todos os dados de uma pessoa, desde informações gerais (CPF, endereço) até dados específicos do seu perfil (matrícula de aluno, cargo de administrador, etc.).
    *   **Editar:** Clique nos três pontinhos ao lado de um usuário e escolha "Editar" para atualizar qualquer informação do seu cadastro.
    *   **Excluir:** No mesmo menu, a opção "Excluir" remove o usuário do sistema.

### 4. Catálogo de Cursos

Aqui você pode organizar todos os cursos que a instituição oferece.

*   **Como Acessar:** Pelo atalho no Painel ou clicando em "Catálogo de Cursos" no menu lateral.
*   **O que você pode fazer:**
    *   **Visualizar:** Uma tabela mostra todos os cursos com seu código, nome e quantidade de créditos.
    *   **Adicionar Curso:** Clique no botão "Adicionar Curso" para abrir um formulário e cadastrar um novo curso.
    *   **Editar e Excluir:** Use o menu de ações em cada linha para modificar os detalhes de um curso ou removê-lo do catálogo.

### 5. Matrícula de Novos Alunos

Esta tela foi desenhada para agilizar o processo de registro de um novo aluno na instituição.

*   **Como Acessar:** Clique em "Matrículas" no menu lateral.
*   **Como Usar:** Preencha o formulário com os dados do novo aluno (nome, email, endereço, contato de emergência, etc.) e selecione o curso de interesse. Ao clicar em "Matricular Aluno", o sistema automaticamente:
    1.  Cria um perfil de usuário para o aluno.
    2.  Registra a matrícula dele no curso selecionado.

### 6. Consulta de Matrículas

Precisa saber em quais matérias um aluno está matriculado? Esta é a tela certa.

*   **Como Acessar:** Clique em "Consulta de Matrículas" no menu lateral.
*   **Como Usar:**
    1.  Selecione o nome de um aluno na lista.
    2.  O sistema mostrará instantaneamente uma tabela com todos os cursos em que aquele aluno está matriculado.

### 7. Perfis de Docentes e Discentes

Esta é uma central de consulta para visualizar a "ficha cadastral" completa de qualquer pessoa no sistema.

*   **Como Acessar:** Clique em "Perfis de Docentes e Discentes" no menu lateral.
*   **Como Usar:** Selecione qualquer usuário na lista (seja aluno, professor ou administrador). Imediatamente, todos os dados cadastrados para essa pessoa serão exibidos na tela, de forma organizada.

### 8. Análise de Desempenho com IA

Esta é a ferramenta mais inovadora do Rate+. Ela usa Inteligência Artificial para ajudar a entender e apoiar o desenvolvimento dos alunos.

*   **Como Acessar:** Pelo atalho no Painel ou clicando em "Análise de Desempenho" no menu lateral.
*   **Como Usar:**
    1.  Informe o nome do aluno que você deseja analisar.
    2.  No campo de texto, descreva o desempenho dele (notas, comportamento, participação, dificuldades, etc.).
    3.  Clique em "Gerar Análise".
*   **O que a IA faz:** Com base nas informações que você forneceu, a IA, atuando como um especialista em pedagogia, irá gerar um relatório completo contendo:
    *   Um **resumo profissional** do desempenho do aluno.
    *   A identificação de **áreas de preocupação**, explicando as possíveis causas pedagógicas.
    *   Uma **sugestão de intervenção pedagógica** clara e prática para ajudar o aluno a superar suas dificuldades.

## Como Executar o Projeto (Desenvolvimento)

1.  **Clone o repositório:**
    ```bash
    git clone <url-do-repositorio>
    cd rate-plus-sistema-gestao-academica
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Configure as variáveis de ambiente:**
    Crie um arquivo `.env` na raiz do projeto e adicione sua chave de API para o Google AI (Genkit).
    ```env
    GOOGLE_API_KEY=SUA_CHAVE_API_DO_GOOGLE_AQUI
    ```

4.  **Inicie o servidor de desenvolvimento:**
    ```bash
    npm run dev
    ```
    A aplicação estará disponível em `http://localhost:9002`.

[Link para acessar o projeto do sistema Rate +](https://9000-firebase-studio-1747677786641.cluster-uf6urqn4lned4spwk4xorq6bpo.cloudworkstations.dev/?monospaceUid=340319)
