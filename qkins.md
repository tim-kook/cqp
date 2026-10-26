# Qiskit Setup for Jupyter Notebook on Windows

This guide installs Qiskit and runs **Jupyter Notebook in your web browser**. It does not require VS Code.

## What you will install

- 64-bit CPython 3.14
- Qiskit and its visualization support
- Qiskit Aer for local simulation
- Qiskit IBM Runtime for IBM Quantum service examples
- Jupyter Notebook, Jupyter, and the IPython kernel

The version numbers in the setup PDF are a dated snapshot, so these instructions install compatible versions available when you run the commands rather than pinning those old versions.

## 1. Install Python

Install **64-bit Python 3.14** from [python.org](https://www.python.org/downloads/windows/). After setup, open a new PowerShell window and check that Python is available and 64-bit:

```powershell
py -3.14 --version
py -3.14 -c "import struct; print(struct.calcsize('P') * 8)"
```

The second command should print `64`. Qiskit 2.x supports 64-bit Windows and CPython. See the [Qiskit installation guide](https://quantum.cloud.ibm.com/docs/en/guides/install-qiskit).

## 2. Create and open a project folder

Create a folder for the practicals, for example:

```text
D:\UniWork\Python\QuantumComputing
```

If you do not have a `D:` drive, use a folder in Documents instead. Open PowerShell in the folder you chose.

## 3. Create and activate a Python environment

Run these commands in PowerShell, from the project folder:

```powershell
py -3.14 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

When activation succeeds, the prompt should begin with `(.venv)`.

### If PowerShell blocks activation

Open **Command Prompt** in the same project folder and run:

```cmd
.venv\Scripts\activate.bat
```

Continue with the remaining commands in the same terminal where the environment is active.

## 4. Install Qiskit and Jupyter packages

First update pip:

```powershell
python -m pip install --upgrade pip
```

Then install the packages used by the lab setup:

```powershell
python -m pip install qiskit qiskit-aer qiskit-ibm-runtime matplotlib "qiskit[visualization]" notebook jupyter ipykernel
```

The `notebook` package provides the Jupyter Notebook browser interface. The visualization extra provides Qiskit visualization dependencies. Aer is used for local simulation. IBM Runtime is needed for examples that connect to IBM's quantum service; connecting to that service also requires an IBM Quantum account and separate account setup. Refer to the [Qiskit visualization guide](https://quantum.cloud.ibm.com/docs/en/api/qiskit/visualization) and [IBM Quantum Runtime installation guide](https://quantum.cloud.ibm.com/docs/en/guides/install-qiskit-runtime).

## 5. Register the environment as a notebook kernel

This makes the environment available in Jupyter's kernel menu:

```powershell
python -m ipykernel install --user --name qiskit-lab --display-name "Python (Qiskit Lab)"
```

## 6. Check the installation

Run these commands in the activated terminal:

```powershell
python -m pip check
jupyter notebook --version
```

`pip check` should report no broken requirements.

## 7. Start Jupyter Notebook

From the project folder, run:

```powershell
jupyter notebook
```

A browser page should open. Keep the terminal window open while using Jupyter Notebook. Create a new Python notebook and choose **Python (Qiskit Lab)** as the kernel. Jupyter Notebook is a browser-based application; it runs locally on your computer. See [Project Jupyter's installation guide](https://github.com/jupyter/jupyter.github.io/blob/main/install.md).

## 8. Verify Qiskit from a notebook cell

Run this in a notebook cell:

```python
import sys
import qiskit
import qiskit_aer
import qiskit_ibm_runtime
import matplotlib
import ipykernel

print("Python:", sys.executable)
print("Qiskit:", qiskit.__version__)
print("Aer:", qiskit_aer.__version__)
print("Runtime:", qiskit_ibm_runtime.__version__)
print("Matplotlib:", matplotlib.__version__)
print("IPykernel:", ipykernel.__version__)
```

The `Python:` path should point to the `.venv` folder in your project.

## 9. Check circuit drawing

Run this in another notebook cell:

```python
from qiskit import QuantumCircuit

qc = QuantumCircuit(1)
qc.h(0)
qc.draw(output="mpl")
```

The notebook should display the circuit diagram.

## 10. Check local simulation with Aer

If your practicals use Aer, run this cell:

```python
from qiskit import QuantumCircuit
from qiskit_aer import AerSimulator

qc = QuantumCircuit(1, 1)
qc.h(0)
qc.measure(0, 0)

simulator = AerSimulator()
result = simulator.run(qc, shots=100).result()
print(result.get_counts())
```

The output should show counts for measurement outcomes `0` and `1`. The counts can vary between runs.

## Common issues

- **`py` is not recognized:** Install Python from [python.org](https://www.python.org/downloads/windows/), open a new terminal, and try the version check again.
- **PowerShell says scripts are disabled:** Use the Command Prompt activation instructions in Step 3.
- **`ModuleNotFoundError` in the notebook:** The notebook may be using a different kernel. In the kernel menu, select **Python (Qiskit Lab)**, then restart the kernel and rerun the cell.
- **Qiskit circuit drawing fails:** Confirm `qiskit[visualization]` and `matplotlib` were installed in the active `.venv`; restart the notebook kernel afterward.
- **Aer installation fails:** Confirm Python is 64-bit and pip is up to date. If it still fails, copy the complete error message so the failing dependency can be identified.

To stop the local notebook server, return to its terminal and press `Ctrl+C`; confirm if prompted.
