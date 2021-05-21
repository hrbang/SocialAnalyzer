API and Web App for analyzing & finding a person profile across +300 social media websites. It includes different string analysis and detection modules, you can choose which combination of modules to use during the investigation. The detection modules utilize a rating mechanism based on different detection techniques, which produces a rate value that starts from 0 to 100 (No-Maybe-Yes)


## Security Testing

```bash
-------------------------------------              ---------------------------------
|        Security Testing           |              |        Social-Analyzer        |
-------------------------------------              ---------------------------------
|   Passive Information Gathering   |     <-->     |   Find Social Media Profiles  |
|                                   |              |                               |
|    Active Information Gathering   |     <-->     |    Post Analysis Activities   |
-------------------------------------              ---------------------------------
```

## Find Profile WEB APP (Fast)
<img src="https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/intro_fast.gif" style="max-width:768px"/>

## Find Profile WEB APP (Slow)
<img src="https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/intro_slow.gif" style="max-width:768px"/>

Profile images **will not** be blurred. If you want them to be blurred, turn that option on

## (New) Find Profile CLI (Fast)
<img src="https://raw.githubusercontent.com/qeeqbox/social-analyzer/main/readme/cli.gif" style="max-width:768px"/>

## Features
- String Analysis
- Search Engine Lookup
- Multi Layers detections
- Most Common Names & Words
- Convert Numbers to Letters
- Find Profile Normal (Fast)
- Find Profile Advanced (Slow)
- Find Profile Special (Slow)
- Profile Screenshot (Slow)
- Python CLI (Limited to FindUserProfilesFast option) 
- NodeJS CLI (Limited to FindUserProfilesFast option)
- Optional timeout and implicit wait for each detection (Some websites have a delay logic implemented in the backend)
- Adding descriptions' logic to websites (will be adding the categories later on)
- Custom user-agent option
- Dump Logs to folder

## Special Detections
- Facebook

## Install and run as web app (NodeJS + NPM + Firefox)
```bash
sudo add-apt-repository ppa:mozillateam/ppa
sudo apt-get update
sudo apt-get install -y firefox-esr tesseract-ocr git
git clone https://github.com/qeeqbox/social-analyzer.git
cd social-analyzer
rm -rf package-lock.json node_modules
npm install lodash
npm install
npm start
```

## Install and run as CLI (NodeJS + NPM + Firefox)
```bash
sudo add-apt-repository ppa:mozillateam/ppa
sudo apt-get update
sudo apt-get install -y firefox-esr tesseract-ocr git
git clone https://github.com/qeeqbox/social-analyzer.git
cd social-analyzer
rm -rf package-lock.json node_modules
npm install lodash
npm install
# If you want to list all websites use node app.js -c -l
# Remember the following runs as FindUserProfilesFast
node app.js -c -m "fast" -u "username" -w "youtube pinterest tumblr"
```

## Install and run as CLI (Python3 + NPM + Firefox)
```bash
sudo add-apt-repository ppa:mozillateam/ppa
sudo apt-get update
sudo apt-get install -y firefox-esr tesseract-ocr git
git clone https://github.com/qeeqbox/social-analyzer.git
cd social-analyzer
pip3 install lxml BeautifulSoup4 tld
# If you want to list all websites use python3 app.py -c -l
# Remember the following runs as FindUserProfilesFast
python3 app.py -c -m "fast" -u "username" -w "youtube pinterest tumblr"
```

## Install and run as web app with a grid (docker-compose)
```bash
git clone https://github.com/qeeqbox/social-analyzer.git
cd social-analyzer
docker-compose -f docker-compose.yml up --build
```

## Install and run as web app (docker)
```bash
git clone https://github.com/qeeqbox/social-analyzer.git
cd social-analyzer
docker build -t social-analyzer . && docker run -p 9005:9005 -it social-analyzer
```

## Running Issues
```
Make sure to update to the latest nodejs and npm
```

## Closing the app by port number
```
sudo kill -9 $(sudo lsof -t -i:9005)
```

## Goals
- Adding the generic websites detections (These need some reviewing, but I will try to add them in 2021)

## Resources
- DuckDuckGo API, Google API, NodeJS, bootstrap, selectize, jQuery, Wikipedia and font-awesome
- Let me know if I missed a reference or resource!

## Disclaimer\Notes
- This tool meant to be used locally (It does not have any type of Access Control)
- If you want your website to be excluded from this project, please reach out

## Contact
[![Generic badge](https://img.shields.io/badge/slack-@qeeqbox-yellow.svg?logo=slack&style=flat-square)](https://qeeqbox.slack.com/messages/social-analyzer)
