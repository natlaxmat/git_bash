# 📄 git_bash
## **Working with bash** ## 

Sometimes we work on projects that don't involve a graphical interface, like backend services or API testing. In such cases, Git allows us to manage code, track changes, and collaborate with the team entirely through the command line.

_There are some bash commands that I used to complete assignmants during my QA studies:_

- ## Task 1

##### Working with files and directories
```bash
01. *created the bash1.txt file                  # First create the'bash1.txt' file where you will add the executed commands
02. cd ~                                         # Open home directory via terminal  
03. pwd                                          # Determine the name of the folder you are in
04. mkdir test1                                  # Create a directory inside this folder called 'test1'
05. cd test1                                     # Go to the 'test1' folder
06. touch 1 2 3                                  # Create the '1','2' and '3' files inside the 'test1' directory
07. ls                                           # Check the contents of the 'test1' directory 
08. cd ~                                         # Go to home directory
09. mkdir test2                                  # Create the 'test2' folder inside your home directory
10. rmdir test2                                  # Delete the 'test2' folder
11. rm test1/2                                   # Delete the '2' file from the 'test1' folder
12. mkdir test3                                  # Create the 'test3' folder in the home directory and add two files to it
    touch ~/test3/1 ~/test3/2
13. rm ~/test3                                   # Delete the 'test3' folder
14. mkdir test4                                  # Create the 'test4' folder in your home directory
15. mv test1/1 test/3 test4/                     # Move the '1' and '3' files from the 'test1' folder to the 'test4' folder 
16. echo "line" >> test1/1                       # Add three lines with words 'line' to the '1' file
    echo "line" >> test1/1
    echo "line" >> test1/1	
	-or-
    echo -e "line\nline\nline" >> test1/1
17. cat test1/1                                  # View the contents of the '1' file
18. echo "line" >> test1/3                       # Add three lines with the words 'line' to the 'file 3' folder
    echo "line" >> test1/3
    echo "line" >> test1/3
	-or-
    echo -e "line\nline\nline" >> test1/3
19. cat test1/1 test1/3                          # View the contents of two files ('1' and '3') at once
20. nano test1/1                                 # Using one of the editors, replace all lines in the '1' file  
	hello
	my
	world
```

- ## Task 2

##### Editing files, checking and killing proccesses, pinging websites
```bash
01. *created the bash2.txt file                            # First create the 'bash2.txt' file where you will add the executed commands
02. cd ~                                                   # Go to your home directory via terminal
03. mkdir test3                                            # Create the 'test3' folder
04. echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/4           # Add three files: '4', '5' and '6' to the 'test 3' folder, each of which should contain 4 lines: row1,                                                               row2, row3, row4
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/5
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/6
05. grep "row2" ~/test3/5                                  # Find the line 'row2' in the file '5'
06. grep "row" ~/test3/*                                   # Find the 'row' line in the 'test3' folder
07. grep -c "row" ~/test3/6                                # Count how many lines with the content 'row' in the '6' file
08. find ~/test3 -name "5"                                 # Find the '5' file inside the 'test3' folder
09. find . -name "5" -delete                               # Using the 'find' command delete the '5' file
10. echo "test" > ~/test3/4                                # Using the 'echo' command, add the word 'test' to the '4' file (without saving the contents)
11. sed 's/test/fail/g' ~/test3/4                          # Replace the word 'test' in the '4' file with the word 'fail'
12. echo "test" >> ~/test3/4                               # Add the word 'test' to the '4' file so that the content is preserved
13. ps aux                                                 # View all processes for users not only in the console that occur in the system
    -or-
    tasklist (for Windows)
14. kill 666                                               # Kill the process '666' in console (you don't have to kill it, just write a command)  
    -or-
    taskkill /PID 666 /F (for Windows)          
15. ping rusau.net                                         # Find out the availability of the resource 'rusau.net' using ping
16. ping -c 5 rusau.net                                    # Send 5 packages to the site: rusau.net
17. curl https://petstore.swagger.io/v2/pet                # Using GET and curl command, get information about registered pets with any status at                       /findByStatus?status=available,pending,sold              https://petstore.swagger.io/     
18. curl -X POST "https://petstore.swagger.io/v2/user"     # Using POST and the curl command, create a new user at https://petstore.swagger.io/
    -H "accept: application/json" 
    -H "Content-Type: application/json"
    -d "{\"id\":98765,
    \"username\":\"nat_test_user\",
    \"firstName\":\"Nat\",
    \"lastName\":\"Tester\",
    \"email\":\"nat@example.com\",
    \"password\":\"mySecurePass123\",
    \"phone\":\"123456789\",
    \"userStatus\":1}"
```

## **Working with git** ##

Git is used by testers to track changes in a project, collaborate with developers, and manage versions of test documentation or automated tests.
It helps efficiently control change history and synchronize team efforts.

_Here are some Git commands I used while building my portfolio on GitHub:_

```bash
git init natlaxmat                                              # Create your repository with the same name as your username 
git clone https://github.com/natlaxmat/natlaxmat.git            # Clone your repository on your computer to a separate folder
git clone https://github.com/testrusau/testrusau.git            # Clone github.com/testrusau/testrusau on your computer to a separate folder cd testrusau                                                                             
git push https://github.com/natlaxmat/testrusau.git main:main   # Push data from testrusau repository to your own one
git commit -m "commited change description"                     # Open the README.md file and replace each block with a separate commit 
git push origin main 
```

