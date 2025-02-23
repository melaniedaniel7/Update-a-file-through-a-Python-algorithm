# Algorithm for file updates in Python
Disclaimer:

### Project description
In this scenario I was a security analyst at a health care company. The company has a file that
only authorized employees can access. The authorized employees are identified by their IP addresses
and it is my job to keep this file up to date. I use a Python algorithm to keep this file up-to-date
and automate the process of parsing the file.

The algorithm I have developed parses the text file of IP addresses and updates the file by removing 
IP addresses that no longer have access to the restricted content.

Parsing a file allows security analysts to read and update the contents. 
Parsing is the process of converting data into a more readable format.
An important part of cybersecurity and my job as a security professional 
is controlling access to restricted content.

Below are the steps I followed to create this algorithm.

### Open the file that contains the allow list
The file that I want to open is called '"allow_list.txt"'. 
I start by assigning a string containing this file name to the 'import_file' variable. 
Then, I use a 'with' statement to open it.
The keyword 'with' handles errors and manages external resources. 
The 'open()' function opens a file in Python.
I use the variable 'file' to store the file while I work with it inside the 'with' statement.

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this.
Details on using a with statement and the open() function in your algorithm

### Read the file contents
Next, use the .read() method to convert the contents of the allow list file into a string so that you can read them. Store this string in a variable called ip_addresses.

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this in the Read the file contents section of the Algorithm for file updates in Python template.

### Convert the string into a list
In order to remove individual IP addresses from the allow list, the IP addresses need to be in a list format. Therefore, use the .split() method to convert the ip_addresses string into a list.

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this in the Convert the string into a list section of the Algorithm for file updates in Python template.

### Iterate through the remove list
A second list called remove_list contains all of the IP addresses that should be removed from the ip_addresses list. Set up the header of a for loop that will iterate through the remove_list. Use element as the loop variable.

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this in the Iterate through the remove list section of the Algorithm for file updates in Python template.

### Remove IP addresses that are on the remove list
In the body of your iterative statement, add code that will remove all the IP addresses from the allow list that are also on the remove list. First, create a conditional that evaluates if the loop variable element is part of the ip_addresses list. Then, within that conditional, apply the .remove() method to the ip_addresses list and remove the IP addresses identified in the loop variable element. 

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this in the Remove IP addresses that are on the remove list section of the Algorithm for file updates in Python template.

In addition, include a sentence that explains that applying the .remove() method in this way is possible because there are no duplicates in the ip_addresses list.

### Update the file with the revised list of IP addresses
Now that you have removed these IP addresses from the ip_address variable, you can complete the algorithm by updating the file with this revised list. To do this, you must first convert the ip_addresses list back into a string using the .join() method. Apply .join() to the string "\n" in order to separate the elements in the file by placing them on a new line.

Then, use another with statement and the .write() method to write over the file assigned to the import_file variable.

<img src="" width="600" />

Describe the Python syntax, functions, and keywords you need to accomplish this in the Update the file with the revised list of IP addresses section of the Algorithm for file updates in Python template.

### Summary

In the Summary section, provide a short summary of the algorithm by highlighting its main components. Write four to six sentences.


- Details on using a with statement and the open() function in your algorithm
- Details on using the .read() and .write() methods in your algorithm
- Details on using the .split() method in your algorithm
- Details on using a for loop in your algorithm
- Details on using the .remove() method in your algorithm


