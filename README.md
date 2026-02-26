# BlogApp-MVC

Layered **ASP.NET Core MVC Blog Application** built with **Entity Framework Core** and **Repository Pattern**.  
Includes **Cookie Authentication**, **Tag filtering**, **ViewComponents**, and **AJAX-based commenting**.

## Features
- Post CRUD (Create / Edit / List / Details)
- Tag filtering (`Index(string tag)`)
- AJAX Comment System (jQuery) without page refresh
- User Register / Login / Logout (Cookie Auth)
- Protected endpoints with `[Authorize]`
- ViewModels + DataAnnotations validation
- ViewComponents (`NewPosts`, `TagsMenu`)
- EF Core Migrations + SeedData

## Project Structure
- `Controllers/` → Posts & Users controllers
- `Data/Abstract/` → repository interfaces
- `Data/Concrete/EfCore/` → EF Core implementations + `BlogContext`
- `Entity/` → domain entities (Post, Tag, Comment, User)
- `Models/` → ViewModels (PostCreateViewModel, LoginViewModel, RegisterViewModel)
- `Views/` → Razor views
- `ViewComponents/` → reusable UI components
- `wwwroot/` → static assets

## Tech Stack
- ASP.NET Core MVC
- EF Core
- SQLite (dev)
- Bootstrap + jQuery

## Run Locally
```bash
git clone https://github.com/Kaganucar/BlogApp-MVC.git
cd BlogApp-MVC
dotnet restore
dotnet ef database update
dotnet run