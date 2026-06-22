# Energy-Efficient QoS-Aware Data Transfer in SW-LPWAN using Q-Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)

This project implements a novel approach to improve data transfer efficiency in
Low-Power Wide-Area Networks (LPWANs) by integrating **Small-World
Characteristics (SWC)** and **Q-Learning**. It addresses challenges in
traditional multihop data transmission, such as latency, energy imbalance, and
low throughput.

To learn more about the research behind this implementation, visit the [IEEE
publication](https://ieeexplore.ieee.org/abstract/document/10214496).

## What it Does

The simulation models a network of smart IoT devices (IoDs) and uses
Reinforcement Learning (Q-Learning) to optimize the addition of long-range
links. By achieving "small-world" properties, the network reduces the Average
Path Length (APL) while maintaining a high Average Clustering Coefficient (ACC),
leading to:

- Reduced data latency.
- Balanced energy consumption across nodes.
- Improved network lifetime and throughput.

## Key Features

- **Small-World Network Modeling**: Implementation of the Watts-Strogatz model to
  simulate small-world properties.
- **Q-Learning Optimization**: An agent that learns the most efficient
  long-range links to add based on rewards tied to QoS metrics.
- **QoS Analysis**: Detailed tracking of Average Path Length (APL) and Average
  Clustering Coefficient (ACC).
- **Energy Simulation**: Comparison of energy-remaining metrics across different
  routing strategies (Proposed Model vs. Multihop, Single-hop, LEACH, and
  Modified LEACH).
- **Visualization**: Extensive plotting of network topology, interference
  patterns, and performance metrics.

## Tech Stack

- **Language**: Python 3.x
- **Environment**: Jupyter Notebook
- **Graph Theory**: [NetworkX](https://networkx.org/)
- **Data Science**: [NumPy](https://numpy.org/), [Pandas](https://pandas.pydata.org/)
- **Visualization**: [Matplotlib](https://matplotlib.org/)
- **Scientific Computing**: [SciPy](https://scipy.org/)

## Prerequisites

Ensure you have Python installed. It is recommended to use a virtual environment.

```bash
pip install numpy pandas matplotlib networkx scipy notebook
```

## Installation

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Launch Jupyter**:

   ```bash
   jupyter notebook
   ```

## Usage

The core logic is divided into three primary notebooks within the
`Research_using_SW-LPWAN_and Q-Learning/` directory:

1. **`Research_Work_RL.ipynb`**:
   - Contains the main Reinforcement Learning implementation.
   - Defines the reward function based on network slope variations (APL and
     ACC).
   - Trains the agent to identify optimal long-range links (radio range
     threshold > 3000 units).

2. **`QOS.ipynb`**:
   - Performs comparative analysis of the proposed model against standard
     protocols.
   - Generates performance graphs for energy consumption and interference.
   - Visualizes the "Small World" effect on LPWAN.

3. **`Test_Notebook.ipynb`**:
   - Used for validating graph generation and basic pathfinding algorithms.
   - Contains sanity checks for node coordinates and initial network edges.

## Project Structure

```text
.
├── README.md                                      # Project documentation
└── Research_using_SW-LPWAN_and Q-Learning/        # Source directory
    ├── Research_Work_RL.ipynb                     # Q-Learning logic
    ├── QOS.ipynb                                  # QoS and Energy analysis
    └── Test_Notebook.ipynb                        # Testing and validation
```

## Simulation Details

- **Nodes**: 300 IoT devices.
- **Initial Topology**: Connected graph with nodes placed in a 2D coordinate
  system.
- **Long-Range Threshold**: Links are considered for RL training if the physical
  distance exceeds 3000 units.
- **Learning Parameters**:
  - Epsilon (Exploration): 0.5
  - Learning Rate: 0.8
  - Discount Factor (Gamma): 0.8

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any
improvements or bug fixes.

## License

This project is licensed under the MIT License - see the LICENSE file for
details (or standard MIT terms if not present).

---
*Disclaimer: This project is based on the research paper "Energy-Efficient and
QoS-Aware Data Transfer in SW-LPWAN Using Q-Learning".*
**To know more about our paper, visit: https://ieeexplore.ieee.org/abstract/document/10214496**
