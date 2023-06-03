# fibtool

usage: fibtool [-h] [-id ID] [-n NAME] [-f [FILE]] [-s [SPLIT]] [-d DIR] [-ip IP] [-u USER] [-p PASSWORD] [-t TEMPLATE] [-tqae] [-dry]
               {qa,scene,gv} {get,upload,patch,delete,info}

command line tool for fibaro HC3

positional arguments:
  {qa,scene,gv}         hc3 resource
  {get,upload,patch,delete,info}
                        command to execute

options:
  -h, --help            show this help message and exit
  -id ID, --id ID       resource id on HC3
  -n NAME, --name NAME  resource name on hc3
  -f [FILE], --file [FILE]
  -s [SPLIT], --split [SPLIT]
                        split directory name, supports Supports %ID,%N and strftime args. Default "%N"
  -d DIR, --dir DIR     directory for output, template supporting strftime args
  -ip IP, --ip IP       ip address to hc3
  -u USER, --user USER  user at hc3
  -p PASSWORD, --password PASSWORD
                        password at hc3
  -t TEMPLATE, --template TEMPLATE
                        name template for output file. Supports %ID,%N and strftime args. Default "%ID_%N"
  -tqae, --tqae         add TQAE headers to main file of QA if missing
  -dry, --dry           don't write any file or make changes on hc3
