# `codemapper`

[![Pylint](https://github.com/shaneholloman/codemapper/actions/workflows/pylint.yml/badge.svg)](https://github.com/shaneholloman/codemapper/actions/workflows/pylint.yml)
[![TODO](https://img.shields.io/badge/✔%20ToDos-44-blue)](notes/todo.md)
![logo](codemapper-outlined.webp)

- [`codemapper`](#codemapper)
  - [Overview](#overview)
  - [Features](#features)
  - [Roadmap](#roadmap)
  - [Requirements](#requirements)
  - [Installation](#installation)
    - [From PyPI](#from-pypi)
    - [From Source](#from-source)
  - [Usage](#usage)
    - [Options](#options)
  - [Output](#output)
  - [Use Cases](#use-cases)
  - [TODO](#todo)
  - [Contributing](#contributing)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)
  - [Version History](#version-history)

## Overview

The Code Mapper is a powerful Python script that creates a comprehensive Markdown document representing the structure and contents of a given directory or GitHub repository. This tool is designed to provide a quick and thorough overview of codebases, making it invaluable for developers, AI systems, and analysts who need to quickly understand the layout and content of a project.

See audio explainers for this project:

- [podcasts](audio) Auto generated by Gemini (NotebookLLM)

## Features

- Generates a hierarchical table of contents based on file structure
- Creates an accurate file tree representation of the directory structure
- Produces code blocks for each file's contents with appropriate syntax highlighting
- Respects `.gitignore` rules when processing files and directories
- Excludes `.git` directories by default
- Supports various file types with appropriate code fence highlighting
- Handles file encoding detection for accurate content reading
- Provides an option to include files normally ignored by `.gitignore`
- Can clone and analyze GitHub repositories
- Saves output in a '_mapped' directory
- Automatically acknowledges large and binary files without printing their contents
- Displays file type and size information for large and binary files

## [Roadmap](./notes/todo.md)

## Requirements

- Python 3.6+
- `pathspec` library (for handling `.gitignore` rules)
- `chardet` library (for file encoding detection)

## Installation

### From PyPI

You can install CodeMapper directly from PyPI using pip:

```sh
pip install codemapper
```

### From Source

1. Clone this repository:

    ```sh
    git clone https://github.com/yourusername/codemapper.git
    ```

2. Install the required dependencies:

    ```sh
    pip install pathspec chardet
    ```

## Usage

Run the script from the command line, providing the path to the directory or GitHub repository URL you want to analyze:

```sh
codemapper <path_to_directory_or_github_url> [--include-ignored]
```

### Options

- `<path_to_directory_or_github_url>`: The path to the directory or GitHub repository URL you want to analyze (required)
- `--include-ignored`: Include files that are normally ignored by `.gitignore` (optional)

## Output

The script generates a Markdown file named `<directory_name>codemap.md` in the '_mapped' directory. This file contains:

1. A table of contents for easy navigation
2. A file tree representation of the directory structure
3. The contents of each file, formatted with appropriate syntax highlighting
4. Information about large and binary files (type and size) without their contents

Example use and output:

```python
codemapper https://github.com/shaneholloman/ansible-role-apache
```

[Example output see here](_example/ansible-role-apache_codemap.md)

## Use Cases

- Quickly understand the structure of new or unfamiliar projects
- Generate documentation for your codebase
- Facilitate code reviews by providing a comprehensive overview
- Aid in onboarding new team members to a project
- Assist AI systems in analyzing and understanding codebases
- Analyze GitHub repositories without needing to clone them manually

## TODO

[codemapper todo list is here](./notes/todo.md)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the `pathspec` and `chardet` libraries for making this tool possible.

## Version History

[For full version history, see [changelog.md](changelog.md)]

---

Don't forget to star this repository if you find it useful!
