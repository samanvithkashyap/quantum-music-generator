# Quantum Music Generator

A Python project that leverages quantum computing principles to generate random musical melodies. This tool uses Qiskit for quantum circuit simulation and pydub for audio synthesis.

## Core Concept

This generator creates a simple 3-qubit quantum circuit. Hadamard gates are applied to place the qubits in a state of superposition. Upon measurement, this superposition collapses into one of eight possible classical states (from '000' to '111') with equal probability.

This quantum-generated random bitstring is then mapped to a corresponding musical note within the C major scale, resulting in a short, unpredictable melody.

## Features

* **True Randomness:** Utilizes quantum superposition and measurement for melody generation.
* **Audio Synthesis:** Converts quantum states into musical notes (C major scale) using `pydub`.
* **Visualization:** Includes `matplotlib` visualizations of the quantum circuit and measurement histograms.
* **Portable Output:** Generates standard `.wav` files.

## Requirements

* Python 3.8+
* Qiskit
* Matplotlib
* Pydub
* IPython
* FFmpeg

## Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/samanvithkashyap/quantum-music-generator](https://github.com/samanvithkashyap/quantum-music-generator)
    cd quantum-music-generator
    ```

2.  **Install Python dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Install FFmpeg:**
    FFmpeg is a required backend for `pydub`.

    * **On Debian/Ubuntu:**
        ```bash
        sudo apt-get install ffmpeg
        ```
    * **On macOS (using Homebrew):**
        ```bash
        brew install ffmpeg
        ```
    * **On Windows:**
        Download the FFmpeg binaries from the official website and add them to your system's PATH.

## Usage

Run the main script to generate your quantum melody. The script will execute the quantum circuit, map the results to notes, and save the output as `quantum_music.wav` in the project directory.

```bash
python main.py
