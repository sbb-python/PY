

1] **** Python installation Process*****
# First install Python greater than 3.9 and above
# To check where is python install you can install gitbash 
# Open Git Bash and just type as --> where python 
# To check Python version you can use commond as --> which python
# Now add environment varible for Python 
# For python -->C:\Users\sandi\AppData\Local\Programs\Python\Python311


2] Assuming VS code is already installed in System

3] ******Setup pip.ini --go to command line and execute below commands

python -m pip config set global.no-cache-dir false
python -m pip config set global.index-url https://pypi.org/simple
python -m pip config set global.itrusted-host pypi.org
python -m pip config set global.ssl-verify fasle 
python -m pip config set global.PLAYWRIGHT_SKIP_BROWSER_DOWNLOAD true

[global]
no-cache-dir = false
index-url = https://pypi.org/simple
itrusted-host = pypi.org
ssl-verify = fasle
playwright-skip-browser-download = true

 *********************************************************************************************************

4] Now create project directory on C drive and open VS code -->File--->open created folder  

5] Now execute below commands

python.exe -m pip install --upgrade pip
pip install pipenv
setup another environment varible for python scripts 
# For python scripts --> C:\Users\sandi\AppData\Roaming\Python\Python311\Scripts
pipenv install requests

After above command, PIPENV should create virtual environment specific to current project 
C:\Users\sandi\.virtualenvs\PY-YYxWkQU9

it should also create Pipfile and Pipfile.lock files in working directory

6 ] powershell setting --type powershell in windows search box and RUN POWERSHELL as ADMINISTRATOR
execute below commands
Get-ExecutionPolicy
Set-ExecutionPolicy Unrestricted

Exit from VS code and reopen VS code

You should see virtual env get activated automatically.
see below 2 lines from vs code terminal
PS C:\PY> & C:/Users/sandi/.virtualenvs/PY-YYxWkQU9/Scripts/Activate.ps1


7] 

