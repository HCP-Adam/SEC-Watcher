## SEC_Watcher

SEC_Watcher is a Python script that monitors real-time SEC 8-K filings for specific keywords related to data breaches and cybersecurity incidents.

## Installation

Before running SEC_Watcher, you need to install the necessary dependencies:

pip install sec-api-python

## Getting Started:

To use SEC_Watcher, you need to obtain an API key from SEC API(https://sec-api.io/). Follow the instructions on their website to sign up and receive your API key.

## Configuration:

Set your SEC API key as an environment variable for security purposes:

On Windows:

set SEC_API_KEY=YourActualAPIKey

On macOS/Linux:

export SEC_API_KEY=YourActualAPIKey

## Usage
Once you have set up your environment variable, you can run the script:

python sec_watcher.py

Make sure to replace sec_watcher.py with the actual name of your script.

SEC_Watcher focuses on the following sections from 8-K filings:

- 1.01: Entry into a Material Definitive Agreement
- 2.02: Results of Operations and Financial Condition
- 2.06: Material Impairments
- 3.02: Unregistered Sales of Equity Securities
- 4.02: Non-Reliance on Previously Issued Financial Statements or a Related Audit Report or Completed Interim Review
- 5.02: Departure of Directors or Certain Officers; Election of Directors; Appointment of Certain Officers: Compensatory Arrangements of Certain Officers
- 7.01: Regulation FD Disclosure
- 8.01: Other Events
- 9.01: Financial Statements and Exhibits

These sections are monitored for keywords and phrases related to data breaches, cybersecurity incidents, and other information security concerns.

SEC EDGAR Filings Real-time Stream API
For real-time monitoring, SEC_Watcher uses the SEC EDGAR Filings Real-time Stream API. This allows the script to process filings as they are submitted to the SEC.

## Credits
This project utilizes the sec-api-python (https://github.com/janlukasschroeder/sec-api-python) library developed by Jan Lukas Schroeder. Special thanks to the contributors of this library for providing the tools to access SEC data.

License
This project is licensed under the MIT License - see the LICENSE file for details.
