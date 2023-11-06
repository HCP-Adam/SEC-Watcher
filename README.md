## SEC_Watcher

SEC_Watcher is a Python script that monitors real-time SEC 8-K filings for specific keywords related to data breaches and cybersecurity incidents.

## Installation

Before running SEC_Watcher, you need to install the necessary dependencies:

pip install sec-api-python

## Getting Started:

To use SEC_Watcher, you need to obtain an API key from SEC API(https://sec-api.io/). Follow the instructions on their website to sign up and receive your API key.

## Configuration:

Set your SEC API key as an environment variable for security purposes:
For Windows
    Using Command Prompt (cmd.exe):
        Press Win + R, type cmd, and press Enter to open Command Prompt.
        Type the following command and press Enter
        
    set SEC_API_KEY=YourActualAPIKey
    
Note that this will set the environment variable for the current session only. If you close the Command Prompt, you will need to set it again next time.

Using PowerShell:

Press Win + X and select “Windows PowerShell” from the menu.
    Type the following command and press Enter:

    $env:SEC_API_KEY="YourActualAPIKey"

Similar to Command Prompt, this sets the variable for the current session only.

To set the environment variable permanently in Windows:

Search for "Environment Variables" in the Start menu and select "Edit the system environment variables".
In the System Properties window, click on the "Environment Variables..." button.
Under "User variables" or "System variables", click "New..." to add a new variable.
Enter SEC_API_KEY as the variable name and your actual API key as the variable value.
Click OK to save and close all dialogs.

On macOS/Linux:
Using Terminal:

Open Terminal from your applications folder or by searching for it.
Type the following command and press Enter:

    export SEC_API_KEY=YourActualAPIKey

This will set the environment variable for the current session only. To make it permanent, you need to add it to your shell profile file.

To set the environment variable permanently on macOS/Linux:

In the Terminal, open your shell profile file with a text editor. For example, if you're using the default Bash shell, you can type:

    nano ~/.bash_profile

or for the Zsh shell (default on newer macOS versions):

    nano ~/.zshrc

Add the following line to the file:

    export SEC_API_KEY=YourActualAPIKey

Save the file and exit the editor (in nano, press Ctrl + X, then Y to confirm, and Enter to exit).
To apply the changes, you can either restart the Terminal or source the profile file with:

    source ~/.bash_profile

or for Zsh:

    source ~/.zshrc

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

## License
This project is licensed under the MIT License - see the LICENSE file for details.
