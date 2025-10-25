# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **GameStore API** built with **.NET 9** using the minimal API approach. The project follows ASP.NET Core conventions with a single-project structure.

## Architecture

- **Framework**: .NET 9.0 (SDK 9.0.306)
- **Project Type**: ASP.NET Core Web API (minimal API pattern)
- **Entry Point**: `GameStore.Api/Program.cs` - contains application configuration and endpoint definitions
- **Configuration**: Standard ASP.NET Core configuration via `appsettings.json` and `appsettings.Development.json`

The project uses the minimal API pattern where endpoints are defined directly in `Program.cs` using `app.MapGet()`, `app.MapPost()`, etc., rather than traditional controller classes.

## Development Commands

### Build
```bash
dotnet build
```

### Run the application
```bash
dotnet run
```
Application URLs:
- HTTP: http://localhost:5223
- HTTPS: https://localhost:7166

### Run with specific profile
```bash
dotnet run --launch-profile http
dotnet run --launch-profile https
```

### Restore dependencies
```bash
dotnet restore
```

### Clean build artifacts
```bash
dotnet clean
```

## Project Structure

- `GameStore.Api/` - Main API project
  - `Program.cs` - Application entry point and endpoint definitions
  - `appsettings.json` - Production configuration
  - `appsettings.Development.json` - Development environment configuration
  - `Properties/launchSettings.json` - Launch profiles for development
  - `GameStore.Api.csproj` - Project file

## Key Configuration

- **Nullable reference types**: Enabled
- **Implicit usings**: Enabled
- **Target framework**: net9.0
- **Default HTTP port**: 5223
- **Default HTTPS port**: 7166
