# `code-mapper`

![logo](code-mapper.svg)

<!-- TOC -->

- [`code-mapper`](#code-mapper)
  - [Overview](#overview)
  - [Features](#features)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Usage](#usage)
    - [Options](#options)
  - [Output](#output)
  - [Use Cases](#use-cases)
  - [TODO](#todo)
  - [Contributing](#contributing)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)
  - [Version History](#version-history)

<!-- /TOC -->History](#version-history)

<!-- /TOC -->
<!-- /TOC -->

## Overview

The Code Mapper is a powerful Python script that creates a comprehensive Markdown document representing the structure and contents of a given directory. This tool is designed to provide a quick and thorough overview of codebases, making it invaluable for developers, AI systems, and analysts who need to quickly understand the layout and content of a project.

See audio explainers for this project:

- [podcasts](audio) Auto generated by Gemini (NotebookLLM)

## Features

- Generates a hierarchical table of contents based on file structure
- Creates an accurate file tree representation of the directory structure
- Produces code blocks for each file's contents with appropriate syntax highlighting
- Respects `.gitignore` rules when processing files and directories
- Excludes `.git` directories and archive files by default
- Supports various file types with appropriate code fence highlighting
- Handles file encoding detection for accurate content reading
- Provides an option to include files normally ignored by `.gitignore`

## Requirements

- Python 3.6+
- `pathspec` library (for handling `.gitignore` rules)
- `chardet` library (for file encoding detection)

## Installation

1. Clone this repository:

    ```sh
    git clone https://github.com/yourusername/directory-structure-markdown-generator.git
    ```

2. Install the required dependencies:

    ```sh
    pip install pathspec chardet
    ```

## Usage

Run the script from the command line, providing the path to the directory you want to analyze:

```python
python directory_markdown_generator.py <path_to_directory> [--include-ignored]
```

### Options

- `<path_to_directory>`: The path to the directory you want to analyze (required)
- `--include-ignored`: Include files that are normally ignored by `.gitignore` (optional)

## Output

The script generates a Markdown file named `<directory_name>_structure.md` in the current directory. This file contains:

1. A table of contents for easy navigation
2. A file tree representation of the directory structure
3. The contents of each file, formatted with appropriate syntax highlighting

Example output:

[example output](example-output/shaneholloman.iptables_structure.md)
    - Was ran on this repository: <https://github.com/shaneholloman/ansible-role-iptables>

## Use Cases

- Quickly understand the structure of new or unfamiliar projects
- Generate documentation for your codebase
- Facilitate code reviews by providing a comprehensive overview
- Aid in onboarding new team members to a project
- Assist AI systems in analyzing and understanding codebases

## TODO

- [ ] add support for creating directly from repo url
- [ ] we need a clever way to include images in the artifacts, maybe base64 encode them directly to the markdown file, but that could chew thru tokens at prompt time? Suggestions?

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the `pathspec` and `chardet` libraries for making this tool possible.

## Version History

- 2.5.0 (2024-09-10): Current version

---

Don't forget to star this repository if you find it useful!
