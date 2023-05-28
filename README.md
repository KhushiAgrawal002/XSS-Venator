# XSS-Venator


SETUP & INSTALLATION
XSSearch requires Selenium, ChromeDriver and Python to work smoothly on your system.

Installing Selenium

sudo apt update

pip3 install selenium (Must)

Installing Chrome Browser for Linux (Skip this if you already have Chrome browser on your Linux)

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo apt install ./google-chrome-stable_current_amd64.deb

You may use the command to start Chrome from your terminal.


google-chrome --no-sandbox


Downloading ChromeDriver

Go to https://chromedriver.chromium.org/downloads and get the linux 64 zipped version of ChromeDriver 80.0.3987.106.

Unzip the zip file. There will be a file for ChromeDriver. Open terminal on the same location and use the following command.

sudo chmod +x chromedriver

sudo mv -f chromedriver /usr/bin/chromedriver


USAGE
XSSearch is a command line tool that uses a single command line instruction for simple and speedy execution.
Note : This tool will only work on url which has a input paramter in the url. Example : www[.]target[.]com/?xyz=

python3 xssearch.py -u url.com/?s={xss} -p payloads.txt

Arguments :
-u : It is required for URL input
-p : It is required for Payload file input
{xss} : It is a placeholder that the user should append after an equal to sign (=) in the url argument.


Live Usage

python3 xssvenator.py -u https://xss.challenge.training.hacq.me/challenges/baby01.php?payload={xss} -p payloads.txt

