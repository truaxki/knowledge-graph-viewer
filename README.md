# Knowledge Graph Viewer

An interactive visualization tool for Model Context Protocol (MCP) knowledge graphs. View and explore your knowledge graph data in both card and network graph formats.

## Features

- Dual view modes:
  - Card view for detailed entity information
  - Network graph view for relationship visualization
- Real-time filtering and search
- Interactive graph manipulation
- Color-coded entity types
- Relationship visualization
- Responsive design

## Setup

1. Clone the repository:
```bash
git clone https://github.com/truaxki/knowledge-graph-viewer.git
cd knowledge-graph-viewer
```

2. Ensure your knowledge graph data is in the correct format (see data format section)

3. Run the sync script to process your data:
```bash
node sync-mcp-data.js
```

4. Start a local server:
```bash
python -m http.server 8000
```

5. Open http://localhost:8000 in your browser

## Data Format

The viewer expects data in JSON Lines format with the following structure:

```jsonl
{"type":"entity","name":"ExampleEntity","entityType":"Category","observations":["Observation 1","Observation 2"]}
{"type":"relation","from":"EntityA","to":"EntityB","relationType":"contains"}
```

## Architecture

- `index.html`: Main entry point and basic styling
- `app.js`: React application with dual view modes
- `sync-mcp-data.js`: Data processing and synchronization script

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

## License

[MIT](LICENSE)
