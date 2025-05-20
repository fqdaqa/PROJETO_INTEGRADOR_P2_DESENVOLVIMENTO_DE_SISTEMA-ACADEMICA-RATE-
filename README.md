\documentclass[
    12pt,            % Tamanho da fonte
    a4paper,         % Tamanho do papel
    oneside,         % Impressão em um lado
    brazil           % Idioma
]{abntex2}

% PACOTES BÁSICOS (Já inclusos ou recomendados pelo abntex2)
\usepackage[T1]{fontenc}     % Seleção de codificação de fonte
\usepackage[utf8]{inputenc}  % Codificação de entrada
\usepackage{lmodern}         % Usa a fonte Latin Modern
\usepackage{indentfirst}     % Indenta o primeiro parágrafo de cada seção
\usepackage{graphicx}        % Para incluir figuras
\usepackage{amsmath}         % Para equações matemáticas
\usepackage{amsfonts}        % Para fontes matemáticas
\usepackage{amssymb}         % Para símbolos matemáticos
\usepackage{enumitem}        % Para customizar listas
\usepackage{hyperref}        % Para links clicáveis (último pacote a ser carregado, geralmente)
\usepackage{hyphenat}        % Para melhor hifenização em português
\usepackage{geometry}        % Para configurar as margens
\geometry{a4paper, top=3cm, bottom=2cm, left=3cm, right=2cm} % Margens ABNT

% --- Configurações do abntex2 ---
\titulo{PROJETO INTEGRADOR 1: DESENVOLVIMENTO DE SISTEMAS ORIENTADO A DISPOSITIVOS MÓVEIS E BASEADOS NA WEB}
\autor{Alexandra Siqueira Tarnoski \\
       Camila Balestri dos Santos \\
       Felipe Queiroz de Azevedo \\
       João Vitor Barbosa Medeiro \\
       Lucas Bueno da Rosa \\
       Daniel Gonçalves Souza \\
       Pedro Henrique Pegado de Souza}
\instituicao{SERVIÇO NACIONAL DE APRENDIZAGEM COMERCIAL SENAC}
\tipotrabalho{Projeto Integrador}
\preambulo{Projeto Integrador apresentado ao Curso de Tecnologia em Análise e Desenvolvimento de Sistemas do Serviço Nacional de Aprendizagem Comercial (SENAC), como requisito parcial para a disciplina de Projeto Integrador 1.}
\local{Brasil}
\data{2025}
\orientador{} % Se houver, adicione aqui
% --- Fim das Configurações do abntex2 ---

% Configuração de listas para ABNT (espaçamento)
\setlist{noitemsep} % Remove espaço extra entre itens de listas

\begin{document}

% --- CAPA ---
% A \imprimircapa do abntex2 segue um formato padrão:
% Instituição (topo)
% Autor (abaixo da instituição)
% Título (centro)
% Local (rodapé)
% Data (rodapé)
% A capa original do OCR tinha uma ordem e elementos ligeiramente diferentes
% (Curso, EAD). Para replicar 100% o OCR da capa, seria necessário
% \renewcommand{\imprimircapa}{...} ou criar uma capa totalmente manual.
% Por ora, usaremos a capa padrão do abntex2 com os dados fornecidos.
\imprimircapa
% --- FIM DA CAPA ---

% --- FOLHA DE ROSTO (para "Visão do Produto") ---
% Esta é uma página de rosto customizada para a seção "Visão do Produto",
% baseada na segunda página do OCR fornecido.
\newpage
\thispagestyle{empty} % Adicionado para remover cabeçalho/rodapé (número da página)
\begin{center}
    \ABNTEXfontereduzida{\imprimirinstituicao} % Ex: SERVIÇO NACIONAL DE APRENDIZAGEM COMERCIAL SENAC
    \vspace*{\fill} % Espaço para centralizar verticalmente o título abaixo
    \ABNTEXfontecaixaltaenegrito{\Large VISÃO DO PRODUTO - RATE+} % Título principal desta página
    \vspace*{\fill} % Espaço para empurrar o conteúdo abaixo para o rodapé da área centralizada
    \ABNTEXfontereduzida{EAD - ENSINO À DISTÂNCIA} \\ % Informação adicional
    \ABNTEXfontereduzida{\imprimirdata} % Ex: 2025
\end{center}
\cleardoublepage % Garante que a próxima página textual comece como uma página direita (ABNT)
% --- FIM DA FOLHA DE ROSTO ---

% --- RESUMO ---
\begin{resumo}
Este projeto integrador apresenta a visão do produto para o Rate+, um Sistema de Gestão Acadêmica (SGA) moderno, projetado como uma aplicação web para instituições de ensino. O sistema visa auxiliar na gestão eficiente de alunos, cursos e docentes, e se destaca pela incorporação de inteligência artificial para fornecer \textit{insights} valiosos sobre o desempenho estudantil. A solução proposta consiste em uma plataforma centralizada e intuitiva, desenvolvida com tecnologias como Next.js, React e Genkit para IA, buscando otimizar processos acadêmicos e administrativos, melhorar a tomada de decisões e aprimorar a experiência de todos os usuários. O Rate+ enfatiza uma interface de usuário moderna e responsiva, segurança de dados e conformidade com a Lei Geral de Proteção de Dados (LGPD).
\bigskip % Pequeno espaço antes das palavras-chave
\noindent
\textbf{Palavras-chave}: Sistema de Gestão Acadêmica. Inteligência Artificial. SaaS. Gestão Educacional. Next.js. LGPD.
\end{resumo}
% --- FIM DO RESUMO ---

% --- SUMÁRIO ---
\pdfbookmark[0]{\contentsname}{toc}
\tableofcontents
\cleardoublepage
% --- FIM DO SUMÁRIO ---

% --- CORPO DO TRABALHO ---
\textual

\chapter{Introdução}
Universidades e instituições de ensino enfrentam desafios significativos na gestão de dados de alunos, professores, cursos e informações acadêmicas. A descentralização dessas informações ou o uso de sistemas legados podem causar perda de dados, retrabalho, erros e dificultar a tomada de decisões estratégicas baseadas em evidências. Adicionalmente, a capacidade de extrair \textit{insights} profundos sobre o desempenho estudantil para intervenções pedagógicas proativas é muitas vezes limitada.

Este projeto propõe o desenvolvimento do Rate+, um sistema de gestão acadêmica (SGA) moderno e centralizado. O Rate+ será uma aplicação web construída com tecnologias atuais, como Next.js e React, e integrará funcionalidades de inteligência artificial (IA) através do Genkit para analisar o desempenho estudantil. O objetivo é fornecer uma solução robusta que não apenas otimize a gestão acadêmica, mas também capacite as instituições com ferramentas analíticas avançadas.

\chapter{Problema}
A gestão de dados em instituições de ensino, quando não apoiada por sistemas adequados, frequentemente resulta nos seguintes problemas principais:
\begin{itemize}
    \item \textbf{Perda de Informações:} Dados dispersos em múltiplos sistemas, planilhas ou registros em papel dificultam a manutenção de informações precisas, atualizadas e seguras.
    \item \textbf{Retrabalho:} A necessidade de inserir as mesmas informações em diferentes sistemas ou corrigir erros manuais aumenta o volume de trabalho e a ineficiência.
    \item \textbf{Erros:} A duplicação de dados e a entrada manual são propensas a erros que podem afetar decisões importantes e a integridade dos registros acadêmicos.
    \item \textbf{Tomada de Decisões Limitada:} A falta de um sistema centralizado e de ferramentas analíticas impede uma visibilidade clara dos dados, dificultando análises abrangentes, identificação de tendências e decisões estratégicas informadas, especialmente no que tange ao acompanhamento do desempenho estudantil.
    \item \textbf{Dificuldade na Identificação Precoce de Problemas:} Sem análises preditivas ou \textit{insights} gerados por IA, torna-se mais difícil identificar alunos em risco ou áreas que necessitam de intervenção pedagógica.
\end{itemize}

\chapter{Solução Proposta}
Para resolver os problemas identificados, propõe-se o desenvolvimento do Rate+, um sistema de gestão acadêmica web moderno, centralizado e integrado, com as seguintes características principais:
\begin{itemize}
    \item \textbf{Plataforma Web Moderna:} Desenvolvido com Next.js e React, oferecendo uma interface de usuário rica, responsiva e componentizada, utilizando ShadCN UI e Tailwind CSS para um design elegante e estilização rápida.
    \item \textbf{Gestão Integrada:} Módulos para gerenciamento de alunos, cursos, docentes, matrículas, notas, frequência e outras informações acadêmicas essenciais.
    \item \textbf{Inteligência Artificial para \textit{Insights}:} Utilização do Genkit (com Google AI) para analisar dados de desempenho estudantil, gerar relatórios, identificar padrões e fornecer \textit{insights} que auxiliem na tomada de decisão pedagógica e administrativa.
    \item \textbf{Interface Intuitiva:} Ferramentas fáceis de usar para inserir, atualizar e acessar informações, visando uma excelente experiência do usuário para todos os perfis (alunos, professores, gestores).
    \item \textbf{Visualização de Dados:} Uso de bibliotecas como Recharts para apresentar dados e análises de forma clara e compreensível através de gráficos e dashboards.
    \item \textbf{Validação e Tipagem:} Emprego de TypeScript para tipagem estática e Zod para validação de esquemas de dados, garantindo maior robustez e manutenibilidade do código.
    \item \textbf{Segurança e Conformidade:} Foco na proteção dos dados sensíveis e conformidade com legislações relevantes, como a Lei Geral de Proteção de Dados (LGPD).
\end{itemize}

\chapter{Benefícios Esperados}
A implementação do Rate+ trará os seguintes benefícios:
\begin{itemize}
    \item \textbf{Eficiência Operacional:} Redução de retrabalho e erros manuais, liberando tempo para tarefas mais estratégicas através da automatização e centralização.
    \item \textbf{Qualidade dos Dados:} Dados mais precisos, consistentes e atualizados, melhorando a confiança nas informações e nas análises geradas.
    \item \textbf{Tomada de Decisões Informada e Proativa:} Acesso fácil a dados consolidados e, crucialmente, a \textit{insights} gerados por IA, permitindo decisões estratégicas e pedagógicas mais eficazes e a identificação precoce de tendências ou alunos que necessitam de apoio.
    \item \textbf{Melhoria na Experiência do Usuário:} Interfaces modernas e intuitivas para alunos, professores e gestores, facilitando o acesso à informação e a realização de tarefas.
    \item \textbf{Inovação na Gestão Educacional:} Introdução de ferramentas de IA para uma compreensão mais profunda do ambiente acadêmico e do progresso dos estudantes.
\end{itemize}

\chapter{Soluções Existentes}
O mercado de sistemas de gestão acadêmica apresenta diversas opções, que incluem:
\begin{itemize}
    \item \textbf{Sistemas de Gestão Acadêmica (SGAs) legados:} Muitas vezes são sistemas robustos, porém com interfaces desatualizadas, pouca flexibilidade, e que podem não oferecer funcionalidades analíticas avançadas ou integrações modernas.
    \item \textbf{Planilhas e Documentos Descentralizados:} Soluções manuais que levam a inconsistências, duplicidade de dados, falta de segurança e grande dificuldade na geração de relatórios consolidados.
    \item \textbf{Softwares de CRM/ERP Genéricos Adaptados:} Softwares que não são especializados para o ambiente universitário e que, mesmo com adaptações, podem não atender a todas as especificidades da gestão educacional.
\end{itemize}
O Rate+ se diferenciará por ser uma aplicação web construída com um \textit{stack} tecnológico moderno (Next.js, React, TypeScript), com foco na experiência do usuário (ShadCN UI, Tailwind CSS) e, principalmente, pela integração nativa de inteligência artificial (Genkit com Google AI) para análise de desempenho e geração de \textit{insights}, oferecendo uma solução mais ágil, inteligente e adaptada às necessidades contemporâneas das instituições de ensino.

\chapter{Objetivo Principal}
O objetivo principal do projeto é desenvolver o Rate+, uma plataforma web (SaaS) centralizada e intuitiva para a gestão completa de dados universitários e escolares. O sistema visa otimizar processos, reduzir erros, melhorar a comunicação e facilitar o acesso à informação para alunos, professores e gestores, com um diferencial chave na utilização de inteligência artificial para fornecer \textit{insights} sobre o desempenho estudantil e apoiar a tomada de decisões estratégicas e pedagógicas.

\chapter{Arquitetura e Tecnologias}
Para o desenvolvimento do Rate+, será utilizada uma arquitetura moderna e escalável, empregando as seguintes tecnologias principais, conforme a nova proposta do sistema:

\begin{itemize}
    \item \textbf{Next.js:} Framework React para renderização no servidor (\textit{SSR}), geração de sites estáticos (\textit{SSG}), e construção de aplicações web full-stack robustas.
    \item \textbf{React:} Biblioteca JavaScript para a construção de interfaces de usuário componentizadas, interativas e reutilizáveis.
    \item \textbf{ShadCN UI:} Coleção de componentes de UI elegantes, acessíveis e reutilizáveis, construídos sobre o Radix UI e Tailwind CSS, para agilizar o desenvolvimento da interface.
    \item \textbf{Tailwind CSS:} Framework CSS \textit{utility-first} para estilização rápida e customizável, permitindo a criação de designs modernos sem sair do HTML/JSX.
    \item \textbf{Genkit (com Google AI):} Framework para desenvolvimento de aplicações baseadas em IA, que será utilizado para integrar funcionalidades de inteligência artificial, como análise de desempenho estudantil, utilizando modelos do Google AI.
    \item \textbf{TypeScript:} Superset do JavaScript que adiciona tipagem estática ao código, melhorando a manutenibilidade, a detecção de erros em tempo de desenvolvimento e a clareza do código.
    \item \textbf{Lucide React:} Biblioteca de ícones SVG leves, customizáveis e consistentes para a interface do usuário.
    \item \textbf{Recharts:} Biblioteca de componentização de gráficos para React, utilizada para visualização de dados e criação de dashboards analíticos.
    \item \textbf{Zod:} Biblioteca para validação de esquemas de dados com foco em TypeScript, garantindo a integridade e o formato correto dos dados manipulados pela aplicação.
\end{itemize}
Esta pilha tecnológica foi escolhida para garantir uma aplicação performática, com excelente experiência de usuário, desenvolvimento ágil e capacidade de integrar recursos avançados de inteligência artificial.

\chapter{Personas}
Para garantir que o Rate+ atenda às necessidades dos usuários, foram definidas as seguintes personas:

\begin{itemize}
    \item \textbf{Persona 1 - Ana Silva, Estudante de Graduação:}
    \begin{itemize}
        \item \textit{Dados Demográficos:} 20 anos, estudante do 3º semestre de Engenharia da Computação.
        \item \textit{Objetivos:} Acessar notas e frequência rapidamente, verificar o calendário acadêmico, realizar solicitações online, manter-se informada sobre avisos da universidade, entender seu progresso e áreas de melhoria.
        \item \textit{Frustrações:} "Perco muito tempo procurando informações que deveriam estar em um só lugar. A falta de um aplicativo móvel ou de uma interface web responsiva também dificulta o acesso quando estou fora da universidade.”
        \item \textit{Comportamentos:} Utiliza principalmente o smartphone e o notebook para acessar informações acadêmicas. Prefere interfaces intuitivas e processos rápidos. Valoriza feedback sobre seu desempenho.
    \end{itemize}
    \vspace{0.5em} % Pequeno espaço entre personas
    \item \textbf{Persona 2 - Carlos Oliveira, Professor Titular:}
    \begin{itemize}
        \item \textit{Dados Demográficos:} 45 anos, professor do departamento de Física há 15 anos.
        \item \textit{Objetivos:} Lançar notas e frequência de forma eficiente, comunicar-se com os alunos, acessar o plano de ensino, gerenciar materiais didáticos, acompanhar o desempenho da turma e identificar alunos que precisam de mais atenção.
        \item \textit{Frustrações:} "Os sistemas da universidade são fragmentados e desatualizados. Preciso redigitar informações em diferentes plataformas, o que é frustrante e propenso a erros. A interface é pouco intuitiva e não oferece boas ferramentas de análise."
        \item \textit{Comportamentos:} Utiliza principalmente o computador para tarefas acadêmicas. Valoriza a precisão, a organização das informações e ferramentas que otimizem seu tempo.
    \end{itemize}
    \vspace{0.5em}
    \item \textbf{Persona 3 - Maria Souza, Gestora Acadêmica:}
    \begin{itemize}
        \item \textit{Dados Demográficos:} 35 anos, gestora acadêmica responsável pela coor-denação de cursos de graduação.
        \item \textit{Objetivos:} Gerar relatórios acadêmicos consolidados, acompanhar o desempenho dos alunos e dos cursos, administrar o calendário acadêmico, garantir a conformidade com as regulamentações, identificar tendências de evasão ou retenção.
        \item \textit{Frustrações:} "A falta de um sistema centralizado e com capacidade analítica dificulta a obtenção de dados consolidados para a tomada de decisões. Perco muito tempo compilando informações de diferentes fontes e gerando relatórios manualmente."
        \item \textit{Comportamentos:} Utiliza principalmente o computador para tarefas administrativas e de gestão. Precisa de ferramentas de análise de dados robustas e relatórios personalizáveis e de fácil interpretação.
    \end{itemize}
\end{itemize}

\chapter{Jornadas Associadas}
\section{Jornada da aluna Ana - Acessando Notas e Frequência}
\begin{enumerate}
    \item \textit{Acesso ao Sistema:} Ana faz \textit{login} no sistema Rate+ usando suas credenciais através do navegador em seu smartphone ou notebook.
    \item \textit{Navegação até a Seção de Desempenho:} Ela navega facilmente até a seção de "Meu Desempenho" ou "Notas e Frequência" no menu principal.
    \item \textit{Visualização das Notas:} Ana visualiza suas notas de todas as disciplinas, com clareza sobre avaliações parciais e finais. Gráficos podem indicar sua evolução.
    \item \textit{Verificação de Frequência:} Ela verifica sua frequência nas aulas, com percentuais atualizados.
    \item \textit{Recebimento de Alertas/Notificações:} Ana pode receber um alerta (no sistema ou por e-mail/push, se configurado) informando sobre novas notas lançadas ou alertas de baixa frequência.
    \item \textit{Feedback (Opcional):} O sistema pode oferecer um canal para Ana enviar dúvidas sobre uma nota específica ao professor.
\end{enumerate}
\textit{Pensamentos do Usuário (Ana):} "Preciso ver minhas notas e faltas rapidamente e entender como estou indo no semestre."
\textit{Oportunidades de melhoria:} Alertas proativos sobre desempenho; interface totalmente responsiva; sumário de desempenho com IA.

\section{Jornada do Professor - Lançar Notas}
\begin{enumerate}
    \item \textit{Acesso ao Sistema:} O professor Carlos faz \textit{login} no sistema Rate+ usando suas credenciais.
    \item \textit{Navegação até a Seção de Lançamento:} Carlos navega até a seção de "Lançamento de Notas" ou "Minhas Turmas".
    \item \textit{Seleção da Disciplina/Turma:} Carlos seleciona a disciplina e a turma para a qual deseja lançar as notas.
    \item \textit{Lançamento das Notas:} Ele insere as notas dos alunos em uma interface clara, possivelmente com opções de importação de planilhas ou cálculo automático de médias.
    \item \textit{Verificação e Histórico:} Carlos pode verificar o histórico de notas já lançadas e conferir os dados antes de submeter.
    \item \textit{Confirmação e Envio/Publicação:} Ele confirma e envia/publica as notas, que se tornam visíveis para os alunos e para a gestão.
    \item \textit{Feedback (Opcional):} Carlos pode adicionar observações individuais para os alunos junto com as notas. O sistema pode apresentar \textit{insights} da IA sobre a distribuição das notas da turma.
\end{enumerate}
\textit{Pensamentos do Usuário (Carlos):} "Preciso lançar as notas de forma rápida, segura e sem erros, e ter uma visão geral do desempenho da turma."
\textit{Oportunidades de Melhoria:} Validação inteligente de notas; histórico de alterações; automatização do lançamento a partir de outras ferramentas; dashboard de desempenho da turma com IA.

\chapter{Conclusão}
O desenvolvimento da visão do produto do Rate+ demonstrou o potencial de um sistema de gestão acadêmica moderno, enriquecido com inteligência artificial, para transformar a forma como as instituições de ensino lidam com seus dados e processos. Ao centralizar informações, automatizar tarefas, oferecer uma interface intuitiva e, crucialmente, fornecer \textit{insights} baseados em IA sobre o desempenho estudantil, o Rate+ poderá aumentar significativamente a eficiência operacional, melhorar a qualidade dos dados e facilitar uma tomada de decisões mais estratégica e pedagógica.

A adoção de tecnologias como Next.js, React, ShadCN UI, Tailwind CSS para o front-end, e Genkit com Google AI para as funcionalidades de inteligência artificial, juntamente com TypeScript e Zod para robustez, garantirá que o sistema seja performático, seguro, com excelente experiência de usuário e adaptável às necessidades futuras das instituições. A implementação gradual, com foco contínuo nas personas e suas jornadas, será fundamental para assegurar a usabilidade, a aceitação e a satisfação dos usuários, culminando em uma ferramenta poderosa para a gestão educacional do século XXI.

% --- FIM DO CORPO DO TRABALHO ---

% --- PÓS-TEXTUAIS ---
% \bibliography{nome_do_arquivo_bib} % Se você tiver um arquivo .bib para referências

\end{document}
