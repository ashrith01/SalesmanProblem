# Salesperson Allocation Using Dynamic Programming

## Overview

This Python project allocates a fixed number of salespeople across multiple sales zones to maximize total expected profit. A PyQt5 desktop interface collects the number of zones, the available salespeople, and the profit associated with each allocation; a dynamic-programming routine then reports the maximum profit and every allocation that achieves it.

Despite the repository's historical name, this is a resource-allocation problem—not the travelling salesman problem.

## How It Works

For each zone, the input table records the profit produced by assigning 0 through `x` salespeople. The algorithm combines zones one stage at a time and reuses the best results from earlier stages. This avoids recalculating the same subproblems and produces the best allocation whose assigned-person total equals the available workforce.

## Repository Structure

```text
SalesmanProblem/
├── notebooks/
│   └── salesperson-allocation.ipynb
├── docs/
│   ├── project-report.docx
│   └── presentation.pptx
├── requirements.txt
├── CONTRIBUTING.md
└── README.md
```

## Quick Start

### Prerequisites

- Python 3.8 or newer
- A desktop environment capable of displaying a Qt window

### Install and run

```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
python3 -m notebook notebooks/salesperson-allocation.ipynb
```

On Windows PowerShell, activate the environment with `.venv\Scripts\Activate.ps1`.

In Jupyter, run the code cells in order. The final cell launches the PyQt5 application and remains active until the window is closed.

### Entering data

1. Select **Start**.
2. Enter the number of zones and the maximum number of salespeople.
3. For each zone, enter a comma-separated profit row containing one value for every allocation from zero through the maximum.
4. Select **Calculate** to display the maximum profit and optimal allocation combinations.

For example, if the maximum is 3 salespeople, every zone needs four values representing allocations `0, 1, 2, 3`.

## Project Team

The report and presentation credit:

- K. Vishnu Sainadh
- K. Satwik
- V. Ashrith

The archived material does not assign individual implementation roles, so no person-specific role claims are made here.

## Documentation

- [Project report](docs/project-report.docx)
- [Presentation](docs/presentation.pptx)

## Contributing

Contributions that improve input validation, algorithm tests, the GUI, or documentation are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

No open-source license has been declared for this repository. The source is publicly visible for educational and reference purposes; obtain permission from the repository owner before reuse or redistribution.
