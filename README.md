# PubMed-DOI-Redirect
A Tampermonkey/Greasemonkey script that automatically detects and redirects you from PubMed article pages to the corresponding articles on the publisher’s website using the DOI link. 

## Why? 
Because PubMed metadata is usually inferior compared to publisher's websites when importing into the Zotero Connector, and I don't like having to click the DOI link every time I load a PubMed page.

## Screenshot
A message is dispalyed when the PubMed page is about to redirect (when it finishes loading) as a reminder that this script is enabled and working.

![image](https://github.com/huachuman/PubMed-DOI-Redirect/assets/125603964/a30d8ede-66cf-414f-a855-b6021e26929a)


## Installation
If you don't have it already, install the Tampermonkey or Greasemonkey extension for your browser from the official website.

Open the dashboard and click on the “Create a new script” button.

Copy the text from the .js script and paste the it into the editor.

Click on “File” -> “Save” or press Ctrl+S to save the script.

## Usage
Once installed, the script will automatically run whenever you navigate to a PubMed article page. If a DOI link is found on the page, you will be redirected to it without any manual intervention.

## Contributing
We welcome contributions from everyone. If you have any suggestions or find any bugs, please open an issue in this repository.
