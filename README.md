NOTE: This was downloaded from sourceforge.net ([PYSAP][])
      It seems to be outdated but maybe can learn something from the code.
	  
> Author of Code: [Klavdij Voncina][]

[PYSAP]: https://sourceforge.net/projects/pysaprfc/
[Klavdij Voncina]: https://github.com/klavdijv


# Python SAP RFC module

Pysaprfc is a Python wrapper around SAP librfc and provides easy access to SAP data-structures,
tables and RFC enabled function modules.

Requirements

Mandatory:
Python (version 2.2 or newer, tested with Python 2.2.2),
SAP librfc,
ctypes (available from http://sourceforge.net/projects/ctypes).

Optional:
mxDateTime from eGenix mxBase package,
fixedpoint.

Installation

Just copy pysap.py somewhere on PYTHONPATH (prefferabily to the site-packages directory).

# ps: edit in vscode

In order to avoid the issue : "No module named:xxx".
You need add following configuration:

1. In launch.json(you may need create it manually) add following configuration,
   **"env": { "PYTHONPATH": "${workspaceRoot}" }**
```json
{
	"version": "0.2.0",
	"configurations": [
		{
			"name": "Python Debugger: Current File",
			"type": "debugpy",
			"request": "launch",
			"program": "${file}",
			"console": "integratedTerminal",
			"env": { "PYTHONPATH": "${workspaceRoot}" }
		}
	]
}
```

2. In settings.json(you may need create it manually) add following configuration,
```json
{
	"terminal.integrated.env.windows": {
		"PYTHONPATH": "${workspaceFolder};${env:PYTHONPATH}"
	}
}
```
