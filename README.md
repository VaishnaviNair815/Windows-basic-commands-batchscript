# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="780" height="136" alt="image" src="https://github.com/user-attachments/assets/3519a5b7-534b-468c-849a-b1a00d076b5a" />

Remove the directory "my-folder"


## COMMAND AND OUTPUT

<img width="780" height="136" alt="image" src="https://github.com/user-attachments/assets/7acd5243-fda9-4c68-a974-ab44f011069f" />

Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="962" height="367" alt="image" src="https://github.com/user-attachments/assets/1bc23aa4-a818-444d-832b-864eb7861fcd" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="890" height="120" alt="image" src="https://github.com/user-attachments/assets/bf8dcc93-a6f3-47fc-8059-9d8588e245ab" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="890" height="120" alt="646925178-fa57b227-742c-40aa-8f94-15308d892589" src="https://github.com/user-attachments/assets/3b27acb9-4401-4634-aa80-ad72226deef8" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="579" height="181" alt="646925333-0a915878-9679-470b-b6d2-e9e37b363787" src="https://github.com/user-attachments/assets/ee84034d-eaa0-4320-8084-f1d6b98751eb" />
<img width="891" height="236" alt="646925302-3550b302-99ac-4a13-9d77-59646acee262" src="https://github.com/user-attachments/assets/f4337555-0217-4e99-aee0-2e7d74e01c08" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

<img width="856" height="912" alt="646925356-152a0676-7f27-4e58-9657-591ce601d365" src="https://github.com/user-attachments/assets/5e2af54e-3b36-42c4-ad5f-f08304dd9ba9" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="856" height="912" alt="image" src="https://github.com/user-attachments/assets/ccad6568-539c-4037-850b-c34b53fa1390" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="726" height="222" alt="image" src="https://github.com/user-attachments/assets/147cee57-6c18-4fa1-8314-a60db7228e81" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```



## OUTPUT

<img width="623" height="95" alt="image" src="https://github.com/user-attachments/assets/5c0b2fc0-9dc1-47d7-a831-51390f8269b2" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT

<img width="861" height="241" alt="image" src="https://github.com/user-attachments/assets/fcfefccb-1336-4ede-a4fa-93e037dfdac4" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```


## OUTPUT

<img width="748" height="184" alt="image" src="https://github.com/user-attachments/assets/6d90b9c9-d760-4062-93d7-44b58be682ef" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT
<img width="905" height="228" alt="image" src="https://github.com/user-attachments/assets/bc5e093f-ecea-4b2e-83b5-a0dd28451509" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

## OUTPUT
<img width="707" height="423" alt="image" src="https://github.com/user-attachments/assets/73c1d031-2fad-4db5-9a4c-900c365cb85d" />



# RESULT:
The commands/batch files are executed successfully.

