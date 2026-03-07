<div align="center">
  <img src="./assets/Yukari.png" alt="Yukari Logo" width="96"/>
  <h1>Yukari</h1>
</div>

<div align="center">
    <h2>📖 About Yukari</h2>

**Yukari** is an open-source desktop reader built with **WinUI 3** and **.NET 10** for Windows.  
It focuses on speed, privacy (100% local SQLite library, no telemetry/ads/accounts) and extensible via a **plugin-based architecture**.

Anyone can create or use plugins to add sources (MangaDex, ComicK, etc.) without forking the main app.
</div>

<div align="center">
    <h2>✨ Ecosystem Structure</h2>
</div>

- **[Yukari](https://github.com/Yukari-App/Yukari)** → The main application (core reader, UI, library management).  
  Install from here: [Releases](https://github.com/Yukari-App/Yukari/releases) or via Scoop (Asterism bucket).

- **[Yukari.Core](https://www.nuget.org/packages/Yukari.Core)** → Shared API contracts, interfaces (e.g. `IComicSource`) and data models.  
  Published as NuGet package: `dotnet add package Yukari.Core` (latest: 1.4.0).  
  Source repo: [Yukari-App/Core](https://github.com/Yukari-App/Core) (only for reference or PRs to the API itself).

- **[Plugins](https://github.com/orgs/Yukari-App/repositories?q=Plugin+sort%3Aname-asc)** → Community-maintained sources (format: `Plugin.*`).  
  To create one:  
  - Create a new .NET class library project.  
  - Add NuGet: `dotnet add package Yukari.Core`  
  - Implement `IComicSource` (or other required interfaces).  
  - Build → get the `.dll`.  
  - Publish as a new repo in the org (or your own), with Releases containing the DLL.  
  Current examples:  
    - [Plugin.MangaDex](https://github.com/Yukari-App/Plugin.MangaDex)  
    - [Plugin.ComicK](https://github.com/Yukari-App/Plugin.ComicK) (archived)  
    Browse all: [Yukari-App repositories → Plugin.*](https://github.com/orgs/Yukari-App/repositories?q=Plugin+sort%3Aname-asc)

<div align="center">
    <h2>🤝 Contributing & Community</h2>
</div>

- **Creating a new source/plugin**? No need to fork anything!  
  Just reference `Yukari.Core` via NuGet → implement the interfaces → build your DLL → share via a new repo or PR to add it to the org.  
  Guidelines soon in the wiki (coming).

- Report bugs, suggest features or discuss in the **[Yukari issues](https://github.com/Yukari-App/Yukari/issues)**.  

- Want to improve the Core API itself? PRs welcome on [Yukari-App/Core](https://github.com/Yukari-App/Core).

All repos and packages under **GPL-3.0** — feel free to contribute!

Project is **experimental** — more plugins, docs and features coming soon.