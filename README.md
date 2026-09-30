# MicroBlog - Repositories & Dependency Injection

## Description

MicroBlog is a simple ASP.NET Core Razor Pages application for creating and viewing blog posts.

This version uses the repository pattern and ASP.NET Core dependency injection.

Two repository implementations are included:

- `InMemoryBlogRepository` - stores posts in memory
- `JsonBlogRepository` - stores posts in `data/posts.json`

## Features

- Create new blog posts with a title and body
- View all posts on the Index page
- View individual posts on a Details page
- Uses `IBlogRepository`
- Uses ASP.NET Core dependency injection
- Supports both in-memory and JSON storage
- Uses a shared layout and navigation bar
- Uses the `_PostCard` partial view to display post summaries

## Switching Repositories

The repository implementation is registered in `Program.cs`.

To use the JSON repository:

```csharp
builder.Services.AddSingleton<IBlogRepository, JsonBlogRepository>();