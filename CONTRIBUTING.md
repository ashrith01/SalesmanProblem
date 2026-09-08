# Contributing

## Workflow

1. Create a branch for one focused change.
2. Keep the resource-allocation terminology distinct from the travelling salesman problem.
3. Add or document test tables when changing the dynamic-programming routine.
4. Run all notebook cells and exercise the PyQt5 interface before opening a pull request.
5. Include the tested profit table, expected maximum, and expected allocations.

## Validation

Validate the notebook structure before committing:

```bash
python3 -m json.tool notebooks/salesperson-allocation.ipynb >/dev/null
```

Do not commit virtual environments, notebook checkpoints, or operating-system metadata.
