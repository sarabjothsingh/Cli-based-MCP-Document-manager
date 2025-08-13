# CLI-based MCP Document Manager

A powerful command-line interface for managing and interacting with documents through AI, built on the Model Control Protocol (MCP) architecture and powered by Anthropic's Claude AI.

![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🌟 Features

- **Interactive Document Management**: Seamlessly interact with documents using natural language
- **AI-Powered Analysis**: Leverage Claude AI for document analysis and manipulation
- **Smart Document Operations**: 
  - Read document contents
  - Edit documents
  - Format documents to Markdown
  - Generate summaries
- **Command Auto-completion**: Tab completion for all commands and document IDs
- **Extensible Architecture**: Built on MCP for easy addition of new capabilities

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- An Anthropic API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sarabjothsingh/Cli-based-MCP-Document-manager.git
   cd Cli-based-MCP-Document-manager
   ```

2. **Set up environment**
   ```bash
   # Copy example environment file
   cp .env.example .env
   
   # Edit .env and add your Anthropic API key
   # ANTHROPIC_API_KEY=your-key-here
   ```

3. **Install dependencies (Choose one method)**

   Using uv (Recommended):
   ```bash
   pip install uv
   uv venv
   .venv\Scripts\activate  # On Windows
   # source .venv/bin/activate  # On Unix/macOS
   uv pip install -e .
   ```

   Using pip:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   # source .venv/bin/activate  # On Unix/macOS
   pip install -e .
   ```

## 💡 Usage

### Starting the Application

```bash
uv run main.py  # If using uv
# or
python main.py  # If using standard Python
```

### Basic Commands

1. **Document Retrieval**
   ```bash
   > Tell me about @deposition.md
   > What does @report.pdf contain?
   ```

2. **Document Operations**
   ```bash
   > /format deposition.md  # Convert to Markdown
   > /edit document.txt "old text" "new text"
   ```

3. **AI Analysis**
   ```bash
   > Summarize the key points in @report.pdf
   > Compare the contents of @spec.txt and @plan.md
   ```

### Document Management

Current supported document types:
- Markdown (.md)
- PDF (.pdf)
- Text (.txt)
- Word (.docx)

## 🛠️ Development

### Project Structure
```
├── core/              # Core functionality
│   ├── chat.py       # Chat interface
│   ├── claude.py     # Claude AI integration
│   └── tools.py      # Document tools
├── mcp_server.py     # MCP server implementation
├── mcp_client.py     # MCP client
└── main.py           # Entry point
```

### Adding New Documents

Edit `mcp_server.py` to add new documents to the `docs` dictionary:
```python
docs = {
    "new_doc.md": "Document content here",
    # ...
}
```

## Based on Official MCP Tutorials
This project follows the [Model Context Protocol tutorials](https://github.com/modelcontextprotocol/quickstart-resources) 
and [Anthropic's MCP Course](https://anthropic.skilljar.com/introduction-to-model-context-protocol).

**My Learning Contributions:**
- Document management implementation
- Custom tool and resource definitions  
- Project documentation and organization


## Acknowledgments
This project was built following [Anthropic's MCP Course](https://www.anthropic.com). 
Uses the MCP Python SDK under MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Implementing MCP Features

To fully implement the MCP features:

1. Complete the TODOs in `mcp_server.py`
2. Implement the missing functionality in `mcp_client.py`

### Linting and Typing Check

There are no lint or type checks implemented.
#
