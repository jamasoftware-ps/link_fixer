# link_fixer by Jama Software
Fixes broken links in rich text description fields. These broken links are created from duplicating a project with link in it, and then removing the original project. 



#### Supported features:
* identifies bad links (links pointing to projects that do not exist) and attempts to fix the broken link

# Requirements
* [python 3.7+](https://www.python.org/downloads/)
* [pip](https://pip.pypa.io/en/stable/cli/pip_install/)

## Installing project and dependencies 
 * Clone the repo `git clone https://github.com/jamasoftware-ps/link_fixer.git`
 * Install the dependencies  `pip install requirements.txt`
 
## Usage
#### Config:
 * Open the config.ini file in a text editor and set the relevant settings for your environment.
 
 * Connections Settings:  These are the settings required to connect to Jama Connect via the REST API
   * `instnace url`: this is the URL of your Jama Instance ex: https://example.jamacloud.com
   * `using oauth`: Set to True or False.  If set to True, the client_id and client_secret variables will be used to log into 
   * `username`: The username or client id of the user
   * `password`: The password or client secret of the user
   Jama connect via OAuth
   * `disable ssl`: Set to True or False. Setting this to true will ignore SSL verifications 


 * Script Parameters:  These Settings inform the script how the data should be imported to Jama.
   * `link mode`: this is the default mode used to update the link to correct to the corrected item
   * `text mode`: This mode is used flag if the to set the link display text should be updated
     * `display attribute`: This optional field will only be used if the text mode is enabled. This field can be used to specify which item type field will be used for the link text (e.g. `name`, `documentKey`, `globalId`, etc). This will default to `documentKey`
   * `project id`: This is a required field, specify the API ID of the project for this script to run against.


#### Execution:
 * Open the terminal to the directory the script is in and execute the following:   
 ``` 
python3 link_fixer.py
 ```
