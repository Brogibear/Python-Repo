### Objective

In this lab, I create an algorithm that uses Python code to check whether an “allow list” contains any IP addresses identified on a “remove list.” This file is “allow_list.txt” and allows access to resources only certain users should see based on IP address. While another list “remove_list.txt” tells us which IP addresses should be removed from the file containing the allow list.

### Skills Learned

- Create a python script utilizing basic python concepts.
- Develop the script to have the ability to modify a file based on other files such as a list of IP addresses.
- Use python file manipulation techniques.
- Implement python methods to manipulate files based on other factors.
- Use critical thinking and problem-solving skills to create the script and understand how methods can be used for file manipulation.

### Tools Used

- Python3, methods and file manipulation.
- IP Addressing.

### Steps
<!-- This is a comment. It won't be rendered on the webpage. drag & drop screenshots here or use imgur and reference them using imgsrc
Every screenshot should have some text explaining what the screenshot is about.
Example below.
*Ref 1: Network Diagram* -->
- The steps for this project are outlined below on the project files sections detailing all aspects on the script.
- The script is posted here but details on its funciont will be found on the [Python Script Solution](https://docs.google.com/document/d/1Vg0n8CG7fo4XjlLtFo3TBdFo_rmdoKl73xO-_W6G3Ok/edit?resourcekey=0-N6RGHlo2MpUrm1qi-0fnfQ) link.

import_file = "allow_list.txt"

with open(import_file, "r") as file:
ip_addresses = file.read()
print(ip_addresses)

ip_addresses = ip_addresses.split()
For element in remove_list:
	If element in ip_addresses:
		ip_addresses.remove(element)
Ip_addresses = “\n”.join(ip_addresses)

With open(import_file, “w”) as file:
	file.write(ip_addresses)



### Project Files

[Python Script Solution](https://docs.google.com/document/d/1Vg0n8CG7fo4XjlLtFo3TBdFo_rmdoKl73xO-_W6G3Ok/edit?resourcekey=0-N6RGHlo2MpUrm1qi-0fnfQ)
