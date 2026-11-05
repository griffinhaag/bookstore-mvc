# Bookstore MVC

An inventory app for a small bookstore, built with ASP.NET MVC 5, Entity Framework (code-first), and ASP.NET Identity.

The main focus is role-based access: every page requires a login, and each role can only do its own job.

| Role | Can |
| --- | --- |
| Manager | Add new books to inventory |
| Sales Executive | Sell books, which decreases the stock count |

Each book records title, author, price, quantity, and which user added it.

## Structure

```
Controllers/     Account (Identity), Book (add/sell), Home
Models/          Book, Identity user and role models, view models
Migrations/      EF code-first migrations
Views/           Razor views
```

## Running it

Requires Visual Studio with the ASP.NET workload and SQL Server LocalDB (.NET Framework 4.7.2).

1. Open `BookStoreMVCApp.csproj`. NuGet restores the packages on build.
2. In the Package Manager Console, run `Update-Database` to create the database from the migrations.
3. Run the app, register users, and assign them the `Manager` or `SalesExecutive` role.
