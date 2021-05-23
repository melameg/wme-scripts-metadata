# wme-scripts-metadata
Holds Waze Map Editor (WME) scripts metadata.  
Serve UI which enables scripts smart search: by popularity, author, environemts, latest etc.  
## Input:
* Anyone can add a new script.  
* Script is added via GitHub PR in src/metadata.json file, with the following json format:
### Option 1: greasyfork scripts
#### script
Name of the script (link) in greasyfork.
#### forum
Waze forum link describing the script.
#### waze
* user: waze username of script author
* environments (optional) [usa|row|il]
* languages (optional)
## Output:
An offline process reads src/metadata.json and generates a dist/metadata.json file which combines metadata from src/metadata.json and metadata from the script source repository (e.g. greasyfork.com).