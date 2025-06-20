# Spike Prime Python Project Setup

## Prerequisites

- Python 3.8 or newer (recommended: 3.10+)
- [pip](https://pip.pypa.io/en/stable/installation/) (Python package manager)
- A computer with Bluetooth Low Energy (BLE) support (for wireless connection)
- LEGO SPIKE Prime hub with [Pybricks firmware](https://pybricks.com/learn/getting-started/install-pybricks/) installed

## Installation

Open a terminal in the project directory and run:

```sh
pip install bleak
```

> **Note:**  
> `bleak` is the BLE backend used by `pybricksconnect`.

## Additional Notes

- You do **not** need to install the `pybricks` package on your computer unless you are developing for the hub directly.  
  The hub runs Pybricks code natively.

## Uploading and Running Your Python Code on SPIKE Prime

1. **Connect your SPIKE Prime hub to your computer** via USB.
2. **Open the [Pybricks Code editor](https://code.pybricks.com/)** in your web browser.
3. **Open your Python file** (for example, `prime-code.py`) in the Pybricks Code editor.
4. **Click the "Run" (⬇️) button** in the Pybricks Code editor to upload your script to the hub.
5. **Once uploaded, press the center button on the SPIKE Prime hub** to start running your script.  
   The hub is now ready to receive commands from your computer.

## Order of Operations

1. **Run your Python script on your computer** (for example, `basicdemo.py` or your own script using `primeCommands.Prime`).
2. **Press the center button on the SPIKE Prime hub** to start your uploaded program (`prime-code.py`).
3. **Send commands from your computer to the hub** using the provided API or GUI.

> **Tip:**  
> The SPIKE Prime hub will only respond to commands while your Python program (like `prime-code.py`) is running.  
> If you restart the hub or upload a new program, you’ll need to press the center button again to start it before sending commands.

## Example: Using the New Prime API

Your `basicdemo.py` might look like this:

```python
import primeCommands

# Connects to spike prime and does some behinds the scenes stuff
prime = primeCommands.Prime("NSE_Pybricks")

# Goes forward 100 cm
prime.moveForward(100)

# Spins around for fun
prime.partyTime()
```

## Troubleshooting

- Make sure your hub is running the Pybricks firmware and your script is started before connecting.
- If you see BLE errors, ensure Bluetooth is enabled and your hub is in range.
- If you get `ModuleNotFoundError`, double-check your `pip install` commands above.

---