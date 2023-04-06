 ███████╗███████╗██╗
██╔════╝██╔════╝██║
███████╗█████╗  ██║
╚════██║██╔══╝  ██║
███████║███████╗███████╗
 
## Overview
 
* DNS
* Web stack debugging
 
## Environment
 
<!-- ubuntu -->
[![Ubuntu](https://img.shields.io/static/v1?label=&message=Ubuntu&color=E95420&logo=Ubuntu&logoColor=E95420&labelColor=2F333A)](https://ubuntu.com/) <!-- bash -->
[![Bash](https://img.shields.io/static/v1?label=&message=GNU%20Bash&color=4EAA25&logo=GNU%20Bash&logoColor=4EAA25&labelColor=2F333A)](https://www.gnu.org/software/bash/) <!-- vim -->
[![Vim](https://img.shields.io/static/v1?label=&message=Vim&color=019733&logo=Vim&logoColor=019733&labelColor=2F333A)](https://www.vim.org/) <!-- vs code -->
[![VS Code](https://img.shields.io/static/v1?label=&message=Visual%20Studio%20Code&color=5C2D91&logo=Visual%20Studio%20Code&logoColor=5C2D91&labelColor=2F333A)](https://code.visualstudio.com/)
 
* OS: ``Ubuntu`` 20.04
* Shell: ``bash``
* ``ssh``
* Style guidelines: ``shellcheck`` 0.3.7
* Editors: ``vim``, ``VS Code``
* ``awk``
* ``dig``
* ``snap`` snapd
* ``certbot``
 
## Run the code
 
To get the A records for the subdomains of xelar.tech, run:
 
```bash
ralex@ralex-nb:~$ dig xelar.tech | grep -A1 'ANSWER SECTION:'
;; ANSWER SECTION:
xelar.tech.		4151	IN	A	54.165.191.52
ralex@ralex-nb:~$ dig www.xelar.tech | grep -A1 'ANSWER SECTION:'
;; ANSWER SECTION:
www.xelar.tech.		4502	IN	A	54.165.191.52
ralex@ralex-nb:~$ dig lb-01.xelar.tech | grep -A1 'ANSWER SECTION:'
;; ANSWER SECTION:
lb-01.xelar.tech.	4502	IN	A	54.165.191.52
ralex@ralex-nb:~$ dig web-01.xelar.tech | grep -A1 'ANSWER SECTION:'
;; ANSWER SECTION:
web-01.xelar.tech.	4502	IN	A	35.231.236.4
ralex@ralex-nb:~$ dig web-02.xelar.tech | grep -A1 'ANSWER SECTION:'
;; ANSWER SECTION:
web-02.xelar.tech.	4502	IN	A	34.74.187.179
ralex@ralex-nb:~$

