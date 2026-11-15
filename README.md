📝 Minhas Tarefas — To-Do List em PHP
Aplicação web de lista de tarefas (To-Do List) desenvolvida em PHP com banco de dados MySQL, criada como trabalho acadêmico da disciplina de Estrutura de Dados na Fatec Taquaritinga.

Com ela você pode adicionar tarefas, marcar como concluídas e excluir, acompanhando o progresso em tempo real.

✨ Funcionalidades
➕ Adicionar tarefas (com validação: título obrigatório e até 255 caracteres)
✅ Marcar / desmarcar tarefas como concluídas
🗑️ Excluir tarefas (com confirmação antes de apagar)
📊 Contadores de tarefas totais, pendentes e concluídas
📈 Barra de progresso com a porcentagem de tarefas concluídas
🕒 Data e hora de criação de cada tarefa
🌙 Interface moderna em tema escuro, responsiva (funciona no celular)
🛠️ Tecnologias utilizadas
Tecnologia	Uso
PHP 8	Lógica do servidor
PDO	Conexão segura com o banco (prepared statements)
MySQL / MariaDB	Armazenamento das tarefas
HTML5	Estrutura da página
Tailwind CSS (CDN)	Estilização
Font Awesome (CDN)	Ícones
Google Fonts (Sora e Inter)	Tipografia
📁 Estrutura do projeto
ED-TODOLIST-PHP/
├── index.php     # Página principal: lista as tarefas, contadores e formulário
├── actions.php   # Processa as ações (adicionar, alternar, excluir)
├── db.php        # Configuração e conexão com o banco de dados (PDO)
└── schema.sql    # Script de criação do banco e da tabela
🗄️ Banco de dados
O script schema.sql cria o banco todo_db com a tabela tarefas:

Coluna	Tipo	Descrição
id	INT (auto incremento)	Identificador da tarefa
titulo	VARCHAR(255)	Texto da tarefa
concluida	TINYINT(1)	0 = pendente, 1 = concluída
criada_em	TIMESTAMP	Data e hora de criação
🚀 Como executar
Pré-requisitos
XAMPP (ou WAMP / Laragon), que já vem com PHP, Apache e MySQL
Passo a passo
Baixe o projeto

git clone https://github.com/JuanGabrielPereiraAugusto/ED-TODOLIST-PHP.git
Ou clique em Code → Download ZIP e extraia.

Coloque a pasta no servidor Copie a pasta ED-TODOLIST-PHP para dentro de C:\xampp\htdocs\.

Inicie os serviços Abra o XAMPP Control Panel e clique em Start no Apache e no MySQL.

Crie o banco de dados

Acesse http://localhost/phpmyadmin
Vá na aba SQL
Cole o conteúdo do arquivo schema.sql e clique em Executar
Confira a conexão (se necessário) No arquivo db.php, ajuste usuário e senha caso seu MySQL não use o padrão do XAMPP:

define('DB_USER', 'root');
define('DB_PASS', '');
Abra no navegador

http://localhost/ED-TODOLIST-PHP/
🔒 Boas práticas aplicadas
Prepared statements com PDO para evitar SQL Injection
htmlspecialchars na exibição para evitar XSS
Validação dos dados recebidos (trim, tamanho máximo, filter_input para IDs)
Padrão POST → Redirect → GET, que evita reenviar o formulário ao atualizar a página
Conexão com o banco reutilizada (instância static)
🎓 Informações acadêmicas
Instituição	Fatec Taquaritinga
Disciplina	Estrutura de Dados
Professor	Danilo Antonio Sichieri
👤 Autor
Juan Gabriel Pereira Augusto GitHub: @JuanGabrielPereiraAugusto

Projeto desenvolvido para fins acadêmicos.
