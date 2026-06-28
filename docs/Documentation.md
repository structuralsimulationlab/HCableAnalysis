# Documentation
## Installation

### Requirements

- Python 3.13+
- NumPy
- SciPy
- pandas
- openpyxl
- ezdxf

### Install

pip install -r requirements.txt

## Quick Start

1. Prepare an Excel file.

2. Load the model.

3. Run shape finding.

4. Export DXF.

Example:

```python
from hcableanalysis import ShapeFinding
model = ShapeFinding("Example.xlsx")
model.solve()
model.export_dxf("Cable.dxf")
```

---

## input format


## shape finding

## coming soon
