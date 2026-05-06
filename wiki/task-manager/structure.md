# Wiki — Structure Task Manager

## Informations projet
- Repo    : https://github.com/toujaninoura/task-manager
- Local   : C:\projects\task-manager
- Stack   : C# .NET 8 + Angular 17 + Bootstrap 5 + SQL Server
- DB      : TaskManagerDb_Dev (SQL Server local)

## Architecture N-Tier .NET

### Projets
TaskManager.Domain\
TaskManager.Application\
TaskManager.Infrastructure\
TaskManager.API\
TaskManager.Tests\

### Entites existantes
- TaskItem : Id, Title, Description, Status, Priority, DueDate, UserId
- User     : IdentityUser + FirstName, LastName, RefreshTokens

### Interfaces existantes
- ITaskRepository, IUnitOfWork, ITaskService, IAuthService, ITokenService

### Enums
- TaskStatus  : Todo, InProgress, Done
- TaskPriority: Low, Medium, High

### Endpoints existants
- POST   /api/v1/auth/register
- POST   /api/v1/auth/login
- GET    /api/v1/tasks
- POST   /api/v1/tasks
- PUT    /api/v1/tasks/{id}
- DELETE /api/v1/tasks/{id}

## Architecture Angular
- Port API    : https://localhost:7063
- Port Angular: http://localhost:4200
- Bootstrap 5 installe

### Composants existants
- LoginComponent, RegisterComponent
- TaskListComponent, TaskFormComponent
- DashboardComponent

## Conventions
- ApiResponse<T> sur tous les endpoints
- [Authorize] sur tous les endpoints sauf auth
- feat/issue-{N}-{slug} pour les branches
- Commits : feat(scope): description
