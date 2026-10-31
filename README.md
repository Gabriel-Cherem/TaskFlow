TaskFlow - Kanban Management System 📋

Um sistema de gerenciamento de tarefas e projetos baseado no modelo Kanban, desenvolvido para organizar o fluxo de trabalho do dia a dia. Este projeto permite a criação de múltiplos quadros, colunas personalizáveis e cartões de tarefas com suporte a drag-and-drop.

🚀 Funcionalidades

Gestão de Quadros (Boards): Crie, edite e personalize múltiplos quadros (ex: Projetos Pessoais, Trabalho, Estudos).

Colunas Dinâmicas: Adicione e ordene colunas como "A Fazer", "Em Andamento" e "Concluído".

Gerenciamento de Tarefas: Crie cartões de tarefas, adicione descrições e organize-os com Labels (etiquetas coloridas).

Drag and Drop (Arrastar e Soltar): Mova as tarefas entre as colunas de forma fluida, sem recarregar a página.

Dashboard de Quadros: Uma página inicial centralizada listando todos os seus Kanbans salvos.

🛠️ Tecnologias Utilizadas

Back-end: C# com ASP.NET Core (Razor Pages)

ORM: Entity Framework Core

Banco de Dados: MySQL (via Pomelo.EntityFrameworkCore.MySql)

Front-end: HTML, CSS, JavaScript (Fetch API para requisições assíncronas)

Interatividade: SortableJS (para o drag-and-drop)

Estilização: Bootstrap / CSS Customizado

⚙️ Como Executar o Projeto Localmente

Pré-requisitos

.NET SDK instalado (versão 8.0 ou superior recomendada).

Servidor MySQL rodando localmente ou via Docker (ex: DBeaver para gerenciamento).

Passo a Passo

Clone o repositório:

git clone https://github.com/SEU_USUARIO/TaskFlow.git
cd TaskFlow


Configure a String de Conexão:
Abra o arquivo appsettings.json na raiz do projeto Web e ajuste a DefaultConnection com as credenciais do seu banco de dados MySQL:

"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Port=3306;Database=TaskFlowDb;Uid=seu_usuario;Pwd=sua_senha;"
}


Rode as Migrations do Entity Framework:
Abra o terminal na pasta do projeto e execute os comandos para criar o banco e as tabelas:

dotnet ef database update


Inicie a aplicação:

dotnet run


O sistema estará disponível no navegador, geralmente em https://localhost:5001 ou http://localhost:5000.

📂 Estrutura do Banco de Dados

A modelagem principal consiste em:

Boards: Representa o quadro geral.

KanbanColumns: Etapas do fluxo de trabalho pertencentes a um quadro.

TaskItems: As tarefas em si, associadas a uma coluna.

TaskLabels: Etiquetas categorizadoras associadas (N-N) às tarefas.

📝 Licença

Este projeto foi desenvolvido para fins de uso pessoal e estudo. Sinta-se livre para usar e modificar.
