# MpCsvAccounting <img src="images/f-klubben.png" width="200" align="right">

This is a parser for MobilePay MyShop CSVs. It writes CSVs that Dinero accounting software recognizes, as well as PDFs used for documentation.
In use by F-klubben at the Department of Computer Science at Aalborg University, Denmark.

## Prerequisites

The script is written in [Python 3](https://www.python.org/downloads/) and requires it to be installed on the system.
In addition, [Pip](https://github.com/pypa/pip) is needed for dependency installation.

## Installation

The script currently has three high-level dependencies, [holidays](https://github.com/dr-prodigy/python-holidays), [PyFPDF](https://github.com/reingart/pyfpdf), and [dateutil](https://github.com/dateutil/dateutil). To install with pip, run
```bash
python3 -m pip install --user -r requirements.txt
```

## Usage

Keep in mind that the input file should be the exported CSV file for transfers, not sales. The sales file will not work.

An example MP CSV is in the examples directory.
To generate CSV and PDFs for the example, pass input file and appendix start number:
```bash
./mp_csv_accounting.py examples/example.csv 123
```
The output, 123-128.csv and PDF directory 123-128/, is located in the project root.

The config file in config/config.ini is where transfers to the MP number to be processed is defined. Change this if transfers are for something other than Stregsystemet (e.g. sales for the Fyttetur auction).

## License

This script is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
