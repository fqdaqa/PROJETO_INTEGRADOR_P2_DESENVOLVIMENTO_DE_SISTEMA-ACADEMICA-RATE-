# Rate+ Sistema de Gestão Acadêmica

Bem-vindo ao Rate+ Sistema de Gestão Acadêmica! Esta aplicação web moderna foi desenvolvida para auxiliar instituições de ensino na gestão de alunos, cursos, docentes e na obtenção de insights sobre o desempenho estudantil através de inteligência artificial.

## Funcionalidades Principais

O sistema oferece diversas funcionalidades para otimizar a gestão acadêmica:

### 0. Autenticação

Para garantir a segurança e personalização da experiência, o Rate+ possui um sistema de autenticação.

#### Tela de Login
*   **Como Acessar:** Ao iniciar a aplicação, você será direcionado para a tela de login (`/login`).
*   **Como Usar:** Insira seu email e senha nos campos indicados e clique no botão "Entrar".
*   A tela é centralizada e responsiva, adaptando-se a diferentes tamanhos de dispositivos. O fundo é preto, com o logo e nome do sistema em destaque.

#### Cadastro de Novo Usuário (Primeiro Acesso)
*   **Como Acessar:** Na tela de login, clique no botão "Primeiro acesso? Cadastre-se".
*   **Como Usar:** Você será direcionado para a tela de cadastro (`/signup`). Preencha o formulário com seu Nome Completo, Email, Senha e Confirmação de Senha. Após preencher, clique em "Cadastrar". (Atualmente, esta funcionalidade é simulada e não persiste dados).
*   Para retornar à tela de login, clique em "Voltar para Login" no rodapé.

#### Recuperação de Senha
*   **Como Acessar:** Na tela de login, clique no botão "Esqueceu sua senha?".
*   **Como Usar:** Na tela de recuperação (`/forgot-password`), insira o email associado à sua conta e clique em "Enviar Link por Email". Uma mensagem simulada indicará o envio de instruções. A opção de recuperação por SMS está planejada para o futuro.
*   Para retornar à tela de login, clique em "Voltar para Login" no rodapé.

#### Logout
*   **Como Acessar:** Após fazer login, clique no ícone de perfil de usuário (localizado no canto superior direito do cabeçalho da aplicação).
*   **Como Usar:** No menu suspenso, selecione a opção "Sair". Você será redirecionado para a tela de login.

### 1. Painel Principal (Dashboard)

*   **Como Acessar:** Automaticamente após um login bem-sucedido, ou clicando no item "Painel" (ícone `LayoutDashboard`) no menu lateral esquerdo.
*   **O que faz:** O painel é sua central de comando. Ele exibe cards que oferecem acesso rápido às principais seções do sistema:
    *   "Gerenciar Usuários"
    *   "Catálogo de Cursos" (funcionalidade futura)
    *   "Desempenho dos Alunos"
    *   Um resumo de atividades recentes (placeholder atual).

### 2. Gerenciamento de Usuários

*   **Como Acessar:**
    *   A partir do Painel, clique no card "Gerenciar Usuários".
    *   Alternativamente, clique no item "Usuários" (ícone `Users`) no menu lateral esquerdo.
*   **Funcionalidades:**
    *   **Visualizar Usuários:** Uma tabela exibe todos os usuários cadastrados (alunos, professores, administradores) com detalhes como nome, email, papel (com badge colorida) e data de registro.
    *   **Pesquisar e Ordenar:** Utilize o campo de busca acima da tabela para filtrar usuários por nome, email ou papel. Clique nos cabeçalhos das colunas (Nome, Email, Papel, Registrado em) para ordenar os dados.
    *   **Adicionar Novo Usuário:**
        *   **Como Acessar:** Clique no botão "Adicionar Usuário" (com ícone `PlusCircle`) localizado no canto superior direito da tela de listagem de usuários.
        *   **Como Usar:** Você será levado a um formulário (`/users/add`) para preencher os detalhes do novo usuário (atualmente um placeholder).
    *   **Editar Usuário:**
        *   **Como Acessar:** Na tabela de usuários, clique no ícone de três pontos (`MoreHorizontal`) na coluna "Ações" correspondente ao usuário desejado. No menu suspenso, selecione "Editar".
        *   **Como Usar:** (Funcionalidade placeholder no momento) Idealmente, levaria a um formulário pré-preenchido para edição.
    *   **Excluir Usuário:**
        *   **Como Acessar:** Na tabela de usuários, clique no ícone de três pontos (`MoreHorizontal`) na coluna "Ações". No menu suspenso, selecione "Excluir".
        *   **Como Usar:** Uma caixa de diálogo de confirmação aparecerá. Confirme para remover o usuário (a remoção é simulada e opera no estado do cliente).

### 3. Matrícula de Novos Alunos

*   **Como Acessar:** No menu lateral esquerdo, clique no item "Matrículas" (ícone `UserPlus`). Isso o levará para a página `/enrollment`.
*   **Como Usar:** Preencha o formulário detalhado com as informações do novo aluno, incluindo:
    *   Nome completo do aluno
    *   Email do aluno
    *   Data de nascimento
    *   Endereço completo
    *   Nome e telefone do contato de emergência
    *   Seleção do programa/curso de interesse
    *   Após preencher, clique em "Matricular Aluno". (Envio simulado).

### 4. Inscrição em Cursos

*   **Como Acessar:** No menu lateral esquerdo, clique no item "Inscrição em Cursos" (ícone `ClipboardList`). Isso o levará para a página `/courses/register`.
*   **Como Usar:** Este formulário permite inscrever um aluno em um ou mais cursos para um semestre específico.
    *   Selecione o aluno desejado na lista.
    *   Escolha o semestre.
    *   Marque os cursos disponíveis (com nome, código e créditos) nos quais o aluno será inscrito.
    *   Clique em "Inscrever em Cursos". (Envio simulado).

### 5. Gerenciamento de Perfis de Docentes

*   **Como Acessar:** No menu lateral esquerdo, clique no item "Perfis de Docentes" (ícone `Briefcase`). Isso o levará para a página `/faculty/profile`.
*   **Como Usar:** Esta seção é para criar ou atualizar os perfis dos membros do corpo docente.
    *   Selecione um membro do corpo docente existente na lista.
    *   Informe o departamento e o título (ex: Professor, Professor Associado).
    *   Opcionalmente, adicione a localização do gabinete, horário de atendimento e uma breve biografia.
    *   Clique em "Salvar Perfil". (Envio simulado).

### 6. Análise de Desempenho com IA

*   **Como Acessar:**
    *   A partir do Painel, clique no card "Desempenho dos Alunos".
    *   Alternativamente, clique no item "Análise de Desempenho" (ícone `BrainCircuit`) no menu lateral esquerdo. Isso o levará para a página `/performance-insights`.
*   **Como Usar:** Esta ferramenta utiliza Inteligência Artificial (Genkit) para analisar o desempenho de um aluno.
    *   No formulário, informe o nome completo do aluno.
    *   No campo "Registros de Cursos e Observações", forneça um resumo do desempenho acadêmico (notas, comportamento, participação, dificuldades, etc.).
    *   Clique em "Gerar Análise".
    *   O sistema processará os dados e exibirá:
        *   Um **resumo conciso** do desempenho geral do aluno.
        *   Uma identificação de **áreas potenciais de preocupação**.
        *   Um gráfico de barras (se aplicável) para visualizar as áreas de preocupação.

[Link para acessar o projeto do sistema Rate +](https://9000-firebase-studio-1747677786641.cluster-uf6urqn4lned4spwk4xorq6bpo.cloudworkstations.dev/?monospaceUid=340319)
