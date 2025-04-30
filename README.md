# LangGraph Agent Demo

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
<!-- Add other relevant badges here: build status, coverage, etc. -->
<!-- [![Build Status](https://travis-ci.org/your_username/langgraph-agent.svg?branch=main)](https://travis-ci.org/your_username/langgraph-agent) -->

A sample project demonstrating the use of [LangGraph](https://github.com/langchain-ai/langgraph) to build simple stateful, agent-like applications. This example showcases a basic graph that decides randomly between two activities (playing cricket or football).

## Overview

LangGraph is a library for building stateful, multi-actor applications with LLMs. It extends the LangChain expression language and is inspired by Pregel and Apache Beam. This project provides a minimal example to get started with defining states, nodes, and conditional edges in LangGraph.

## Features

*   **State Definition:** Uses `TypedDict` to define the graph's state.
*   **Node Implementation:** Simple Python functions representing graph nodes that modify the state.
*   **Conditional Edges:** Demonstrates routing logic based on the current state using conditional edges.
*   **Graph Compilation & Execution:** Shows how to compile and run the LangGraph graph.
*   **Visualization:** Includes code to visualize the graph structure using Mermaid.

## Getting Started

### Prerequisites

*   Python 3.9+
*   pip

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your_username/langgraph-agent.git # Replace with your repo URL
    cd langgraph-agent
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv .venv
    source .venv/bin/activate # On Windows use `.venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

The core logic is contained within the `simplegraph.ipynb` Jupyter notebook.

1.  **Start Jupyter:**
    ```bash
    jupyter notebook
    ```
    Or, if you prefer JupyterLab:
    ```bash
    jupyter lab
    ```

2.  **Open and run `simplegraph.ipynb`:**
    Navigate to the notebook in the Jupyter interface and run the cells sequentially.

    *   The notebook defines the `State`, node functions (`start_play`, `cricket`, `football`), and the conditional logic (`random_activity`).
    *   It then builds, compiles, and visualizes the graph.
    *   Finally, it invokes the graph with an initial state:
        ```python
        compiled_graph.invoke({"graph_info": "My name is Mo, "})
        ```
    *   You will see output indicating which nodes were called (e.g., `Start play node has been called`, `Football node has been called`) and the final state, which includes the accumulated `graph_info` string. Due to the `random_activity` function, the path taken (cricket or football) will vary between runs.

## Project Structure

```
langgraph-agent/
├── .venv/                   # Virtual environment (if created)
├── simplegraph.ipynb        # Jupyter notebook with the LangGraph example
├── requirements.txt         # Project dependencies
└── README.md                # This file
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` file for more information (or add license text here if no file).

## Contact

Your Name / Project Link - [optional contact info]

[Project Link](https://github.com/mojalil/langgraph-agent)