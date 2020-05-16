# -CG2020-Script_Execute
[CG2020] TechGig-Code-Gladiators UiPath-RPA-Hackathon. Script_Execute. Activity to execute any Script file and return output in UiPath Studio

Project Name:  [CG2020] Script_Execute
UiPath Product used (Focus area):  Activity Creator
Team:
Name     : Legends
Member: Surya Narayanan S

Demo Video Link:
https://www.youtube.com/watch?v=7YGoTG8i1WA
https://www.youtube.com/watch?v=zVP-tKLvWfs

Project Description:
	The Project focuses on executing Script Code from other languages like (C, C++, Python, Nodejs etc.). 
  
List of Activities created:
1.	Zip File or Folder
2.	Unzip a compressed File
3.	(Code) Script Executor

Use Cases:

	For example purpose, I took Python. It can be any script language(C, C++, Nodejs etc.), if the interpreter is preinstalled. It can execute and get the output. It uses CMD to execute it.
	Since it can run any script file, it can be used for other purposes too. It would be easy for non C Sharp programmers like me and it will be easy to add features to the Robot as it doesn’t require any building, updating of Packages.  

1.	Scenario 1: (Example) A Python Teaching faculty assigns students a coding problem to solve. The faculty asks students to mail the zipped python script file as attachment with subject in some format. 
Without Robot: The faculty has to download each mail, unzip each file, execute each python file, verify each output and enter marks in excel file manually (Tedious job).
With UiPath Robot: The Robot downloads the attachment, unzip file, execute python file, verify the output and update the excel file automatically.

2.	Scenario 2: (Example) A Lab attender need to execute batch files to shut down all the computers at the time when the Lab closes. 
Without Robot: The Lab attender has to shut down each and every computer manually. 
With Robot: The Lab attender can write a batch script file to shut down the computers automatically at scheduled time with Script Executor Activity. 

3.	Scenario 3: (Example) let us consider a data scientist needs to clean every dataset whenever a dataset is moved to a folder.  A Script file can be made to clean the dataset and it can be scheduled in UiPath with (Code) Script Executor Activity.

Activity Documentation:

Unzip File Activity:

	Input: 
	Zip File             - requires full path of the zip file (zip file must exist) (e.g. My Documents\Folder1\compressed.zip)
	Destination     - requires full destination path (e.g. My Documents\Folder1)

	Output:
	Completion    - return True if unzip is completed. Otherwise, it returns False

Zip a Folder or File Activity:

	Input:
	Path                 - requires Folder or File Path which needs to be Zipped (e.g. My Documents\Folder1)
	Destination    - requires destination path along with zip name (e.g. My Documents\result.zip)

	Output:
	Completion    - return True if unzip is completed. Otherwise, it returns False

Script Executor Activity:

	Input:
	Program Name    - Name of the Program to run (e.g. python, node, perl, gcc, g++,  etc.,)
	Script File     - requires Script File path (e.g. My Documents/learn.py)
	Input File      - requires Input File path. Input should be given in a text file (e.g. My Documents/input.txt) 

	Output:
	Output       -   returns Output of the Script File after execution
	Error        - returns completion status. Returns true, if executed successfully. Otherwise, it returns false
