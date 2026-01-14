
## Patch 0005: AI-Native Graph Logging
**Applied:** 2025-01-14T10:40:00Z
**By:** Ka_tuar_el

### Changes
- Implemented secondary logging system in Neo4j
- Created system monitoring service (checks every 60 seconds)
- Added daily cleanup service (removes events older than 10 days)
- Monitors: CPU, memory, disk, processes, systemd services
- Enables AI-powered diagnostics and causality analysis

### Files Created
- `/opt/mythos/graph_logging/` (complete installation)
- `~/.config/systemd/user/arcturus-monitor.service`
- `~/.config/systemd/user/arcturus-cleanup.service`
- `~/.config/systemd/user/arcturus-cleanup.timer`
- `~/.config/arcturus/systemd.env`

### Services Monitored
- neo4j
- postgresql
- mythos_api
- mythos_bot
- Auto-discovers: mythos-*, arcturus-*

### Configuration
- Event retention: 10 days
- Monitoring interval: 60 seconds
- Thresholds: CPU 80%, Memory 80%, Disk 90%

## Patch 0006: LLM Diagnostics Interface
**Applied:** $(date -Iseconds)
**By:** Ka_tuar_el

### Changes
- Integrated Ollama for local LLM diagnostics
- Created natural language query interface
- Added conversation logging to Neo4j
- Implemented diagnostic tool integration
- CLI commands: mythos-ask, mythos-chat

### Files Created
- `/opt/mythos/llm_diagnostics/` (complete installation)
- `/usr/local/bin/mythos-ask` (CLI query tool)
- `/usr/local/bin/mythos-chat` (interactive mode)

### Features
- Natural language system queries
- Graph-powered diagnostics
- Read-only access (no system changes)
- Full conversation logging

### Model
- llama3.2:3b (3B parameters, efficient)
