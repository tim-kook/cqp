# Qiskit Installation with Jupyter Notebook

**Complete setup from a blank Windows PC**

## Aim

Starting with no Python installed, install Python for your Windows account, set up Qiskit and its local simulator, then run the practical in classic Jupyter Notebook. VS Code is not required.

## Before you start

- A 64-bit Windows 10 or 11 PC, a web browser, and an internet connection.
- Use a standard user account. The per-user Python installation usually does not need administrator rights, but college restrictions can still block software or downloads.

## A. Install Python from the official source

### 1. Download Python

Open the official [Python releases for Windows](https://www.python.org/downloads/windows/) page. Choose a Python 3.13.x release and download its **Windows installer (64-bit)**. Use the normal installer, not the embeddable ZIP package.

### 2. Run the installer

Open the downloaded installer. On its first screen, check **Add python.exe to PATH**, then click **Install Now**. This installs Python for your account. Wait for the success message and click **Close**.

If the installer is blocked by Windows or college policy, ask the lab administrator to install the approved Python version. Do not choose an all-users installation on a managed PC.

### 3. Open PowerShell and verify Python and pip

Close any terminal windows opened before installation. Open Windows PowerShell from the Start menu as your normal user, then run:

```powershell
python --version
python -m pip --version
python -c "import struct; print(struct.calcsize('P') * 8, 'bit')"
```

Expected: Python 3.13.x, a pip version, and `64 bit`. If Python is not found, open a new PowerShell window and try again. Troubleshooting is at the end of this guide.

## B. Prepare the project environment

### 4. Open PowerShell in your practical folder

Create your folder in File Explorer first. Open that folder, click its address bar, type `powershell`, and press Enter. Run the remaining commands in that PowerShell window.

### 5. Create an isolated Python environment

This keeps the practical's packages separate from Windows and other Python projects:

```powershell
python -m venv .venv
```

### 6. Set the policy for your account

Run the requested command in this regular PowerShell window. It changes the policy for **CurrentUser** only. If a confirmation prompt appears, type **Y** and press Enter.

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Check the policy scopes:

```powershell
Get-ExecutionPolicy -List
```

If college Group Policy does not override it, `CurrentUser` should show `RemoteSigned`. A college `MachinePolicy` or `UserPolicy` can override this setting.

### 7. Activate the project environment

Run this in the practical folder. The PowerShell prompt should start with `(.venv)`:

```powershell
.\.venv\Scripts\Activate.ps1
```

#### If activation is blocked

Do not try to override a college policy. Skip activation and use `.\.venv\Scripts\python.exe` instead of `python` in Steps 8-10, and `.\.venv\Scripts\jupyter.exe` instead of `jupyter` in Step 11.

Use these commands instead of Steps 8-11:

```powershell
.\.venv\Scripts\python.exe -m pip install --upgrade pip
.\.venv\Scripts\python.exe -m pip install "qiskit[visualization]" matplotlib
.\.venv\Scripts\python.exe -m pip install qiskit-aer notebook ipykernel qiskit-ibm-runtime
.\.venv\Scripts\python.exe -m ipykernel install --user --name qiskit
.\.venv\Scripts\jupyter.exe notebook
```

## C. Install Qiskit and open Notebook

### 8. Upgrade pip

With `(.venv)` active, upgrade the package installer:

```powershell
python -m pip install --upgrade pip
```

### 9. Install the Qiskit, Aer, visualization, and Jupyter packages

Install Qiskit's visualization extra and Matplotlib for plots, Qiskit Aer for local simulation, Notebook and IPykernel, and the IBM Quantum Runtime client:

```powershell
python -m pip install "qiskit[visualization]" matplotlib
python -m pip install qiskit-aer notebook ipykernel qiskit-ibm-runtime
```

The visualization extra supplies Qiskit's plotting requirements; Matplotlib is also listed explicitly for practical work. The Runtime client is included for hardware exercises, but using real hardware requires a suitable IBM Quantum account and connection.

Wait for pip to finish and return to the prompt. Keep the terminal open if it is still downloading or installing.

### 10. Register the notebook kernel

Give this environment a recognizable name in Jupyter's kernel menu:

```powershell
python -m ipykernel install --user --name qiskit
```

### 11. Start Jupyter Notebook

Start the classic Notebook server from the practical folder. Keep this PowerShell window open while using Notebook:

```powershell
jupyter notebook
```

A browser tab should open. If not, copy the local URL printed in PowerShell into your browser. In Jupyter, choose **New > Python (qiskit)**. Save the notebook as `Qiskit_Practical_Test.ipynb`.

## D. Verify the installation

In the first notebook cell, paste and run this code. It creates a one-qubit circuit, applies a Hadamard gate, measures the qubit, and displays the circuit diagram:

```python
from qiskit import QuantumCircuit
from qiskit_aer import AerSimulator

qc = QuantumCircuit(1, 1)
qc.h(0)
qc.measure(0, 0)
qc.draw(output="mpl")
```

In a second cell, run the simulator and show the measurement counts:

```python
result = AerSimulator().run(qc, shots=1024).result()
result.get_counts()
```

The counts for `0` and `1` should be roughly balanced, though the exact numbers vary between runs.

To record the installed package versions, run another cell:

```python
import qiskit
import qiskit_aer
import matplotlib
import notebook
import ipykernel
import qiskit_ibm_runtime

print("Qiskit:", qiskit.__version__)
print("Aer:", qiskit_aer.__version__)
print("Matplotlib:", matplotlib.__version__)
print("Notebook:", notebook.__version__)
print("IPykernel:", ipykernel.__version__)
print("IBM Runtime:", qiskit_ibm_runtime.__version__)
```

**Successful result:** the notebook displays the circuit diagram, executes without import errors, and returns measurement counts from Aer.

## Troubleshooting

| Problem | What to do |
|---|---|
| Python installer is blocked | Use **Install Now** for a current-user install. If Windows or college policy still blocks it, ask the lab administrator to install the approved Python version; do not choose an all-users install. |
| `python` is not recognized | Close and reopen PowerShell. If it still fails, rerun the Python installer and ensure **Add python.exe to PATH** is selected. If `py` works, use `py -3.13 -m venv .venv` for Step 5. |
| Notebook says `No module named qiskit` | In Jupyter, use **Kernel > Change Kernel**, select **Python (qiskit)**, then restart the kernel. |
| Aer install fails | Confirm Python 3.13 is 64-bit and the PC can reach PyPI. Use the college-approved package mirror if downloads are blocked; do not try to compile Aer from source on the lab PC. |
| PowerShell blocks `Activate.ps1` | Run `Get-ExecutionPolicy -List`. If `MachinePolicy` or `UserPolicy` is set by the college, use the direct `.venv` paths in Step 7's fallback note. |
| `jupyter` is not found | Wait for Step 9 to finish. If activated, confirm `(.venv)` is in the prompt before Step 11. If using the policy fallback, use `.\.venv\Scripts\jupyter.exe`. |
| College network blocks package downloads | Use the college-approved network or Python package mirror, or ask the lab administrator for the approved install method. |

Save the notebook when finished. Stop the server with **Ctrl+C** in PowerShell.

## References

- [Python Windows setup](https://docs.python.org/3.13/using/windows.html) and [Python downloads](https://python.org/downloads/windows/)
- [Install Qiskit](https://quantum.cloud.ibm.com/docs/en/guides/install-qiskit) and [Qiskit visualization](https://quantum.cloud.ibm.com/docs/en/api/qiskit/visualization)
- [Install IBM Quantum Runtime](https://quantum.cloud.ibm.com/docs/en/guides/install-qiskit-runtime)
- [Install Jupyter Notebook](https://jupyter.org/install)
- [PowerShell execution policy](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.5)
