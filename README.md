# kanban-zone

A Claude Skill (also compatible with OpenClaw and Codex) for managing [KanbanZone](https://kanbanzone.io) kanban boards via the KanbanZone Public API v1.3.

Single-file Python CLI using only the standard library. All output is JSON.

## Setup

```bash
export KANBANZONE_API_KEY="your-api-key"   # Settings > Organization Settings > Integrations
export KANBANZONE_BOARD_ID="your-board-id"
```

## Usage

```bash
python scripts/kanbanzone_api.py boards                        # List all boards
python scripts/kanbanzone_api.py cards                         # List cards
python scripts/kanbanzone_api.py create-card --title "Task"    # Create a card
python scripts/kanbanzone_api.py move-card --id 42 --column-id abc123  # Move a card
python scripts/kanbanzone_api.py search-cards --query "deploy" # Search across boards
python scripts/kanbanzone_api.py wip-check                     # Check WIP limits
```

Run `python scripts/kanbanzone_api.py --help` for all commands and options.

## License

MIT
