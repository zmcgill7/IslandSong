# Distribution Pipeline

Island Song's public distribution path was handled separately from the production Perforce depot. The goal was to give players a clean way to download and install the game without exposing the entire Unreal project.

## What I Built

- Created and maintained the Windows installer flow for the game.
- Supported a public website that served the installer.
- Managed website hosting and deployment through Google Cloud CI/CD.
- Purchased and connected the project domain for the public site.

## Why It Mattered

The production game project was too large and asset-heavy to treat as a simple public GitHub repo. Separating the public download path made the project easier to present and distribute:

- Perforce remained the right tool for Unreal production collaboration.
- The website gave nontechnical visitors a simpler entry point.
- CI/CD kept the website workflow repeatable instead of manual.
- The installer gave players and reviewers a practical way to try the game.

## Portfolio Takeaway

This work connected infrastructure decisions to user-facing delivery. I was not only maintaining source-control access for the development team; I also helped package the finished project into something a player or reviewer could actually install.
