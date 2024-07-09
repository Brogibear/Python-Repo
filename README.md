### Objective

This project is a simple network port scanner implemented in Python. It uses the socket library to attempt connections to specified ports on target IP addresses, identifying which ports are open. The tool can handle both single and multiple targets and provides real-time feedback on the scan progress.

### Skills Learned

- Create a python script utilizing basic python concepts and use the socket library.
- Develop the script to have the ability do a basic network scan.
- Use a python library outside of the common ones.
- Implement python methods to manipulate files based on other factors.
- Use critical thinking and problem-solving skills to create the script and understand how methods can be used for file manipulation.

### Tools Used

- Python3, methods and python library.
- IP Addressing.

### Steps
<!-- This is a comment. It won't be rendered on the webpage. drag & drop screenshots here or use imgur and reference them using imgsrc
Every screenshot should have some text explaining what the screenshot is about.
Example below.
*Ref 1: Network Diagram* -->
- The steps for this project are outlined below on the project files sections detailing all aspects on the script.
- The script is posted here but details on its funciont will be found on the [Python Basic Port Scanner](https://docs.google.com/document/d/1Vb8oog2Yl1GrESjKmwhsWng6FL1gjWxxVazeyE5emRU/edit?usp=sharing) link.

import socket
import termcolor

def scan(target, ports):
	print('\n' + ' Starting Scan For ' + str(target))
	for port in range(1,ports):
		scan_port(target,port)

def scan_port(ipaddress, port):
	try:
		sock = socket.socket()
		sock.connect((ipaddress, port))
		print("[+] Port Opened " + str(port))
		sock.close()
	except:
		pass

targets = input("[*] Enter Targets To Scan(split them by ,): ")
ports = int(input("[*] Enter How Many Ports You Want To Scan: "))
if ',' in targets:
	print(termcolor.colored(("[*] Scanning Multiple Targets"), 'green'))
	for ip_addr in targets.split(','):
		scan(ip_addr.strip(' '), ports)
else:
	scan(targets,ports)



### Project Files

[Python Basic Port Scanner](https://docs.google.com/document/d/1Vb8oog2Yl1GrESjKmwhsWng6FL1gjWxxVazeyE5emRU/edit?usp=sharing)
