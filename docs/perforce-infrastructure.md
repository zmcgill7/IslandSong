# Perforce Infrastructure

Island Song used Perforce instead of Git for the production Unreal Engine project. That decision mattered because the project was Blueprint-heavy and contained large binary assets, both of which are difficult to manage well with ordinary Git workflows.

## Why Perforce

Unreal projects often involve assets that cannot be cleanly merged as text. Blueprint files, maps, materials, and art assets benefit from file locking, binary-friendly history, rollback, and workflows designed around large game-development depots.

I evaluated alternatives before preserving the Perforce path:

- Vendor-managed setup: approximately $2,500.
- Self-administered cloud path: approximately $1,500.
- Weaker version-control alternatives with worse Unreal integration or large-file behavior.

Perforce offered the best balance of Unreal integration, large-file performance, and team workflow fit.

The early meeting notes show that this was not a retroactive justification. At project launch, I compared Perforce, GitHub, GitLab, and cloud/self-hosted options across storage limits, outbound bandwidth, subscription cost, Unreal integration, large binary handling, binary locking, and administration risk. The initial low-cost fallback was GitHub LFS; the stronger professional path was Perforce if I could make self-hosting reliable for the team. As the project grew into a large Blueprint-heavy Unreal depot, preserving Perforce became the right engineering decision.

## What I Owned

- Designed and maintained the self-hosted Perforce environment.
- Supported secure remote access using tunnel-based networking.
- Kept infrastructure available despite network restrictions and dated hardware.
- Added startup/recovery automation and middleware so the system could come back online reliably.
- Onboarded and trained teammates who had no prior P4V experience.
- Responded to infrastructure issues so development was not blocked.

## Recruiter-Relevant Takeaway

This was not just "set up source control." It was a practical infrastructure tradeoff under budget, hardware, networking, security, and team-experience constraints. The goal was to preserve a professional Unreal workflow without overbuying a managed solution, while keeping the rest of the team productive.
