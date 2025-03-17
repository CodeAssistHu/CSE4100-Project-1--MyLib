# CSE4100-Project-1--MyLib
**Download Link:** https://programmingsolver.com/questions-and-answers/cse4100-project-1-mylib/



Sogang University
Project #1: MyLib
: System Programming






CSE4100 Project 1: MyLib
 

    • Introduction

In the MyLib project, students will explore various data structures within the kernel library. They will ana-lyze these data structures and enhance their C programming skills by implementing structures such as lists, hash tables, and bitmaps. As a result, students will develop an interactive program capable of evaluating the functionalities of lists, hash tables, and bitmaps.

    • Materials

There are three items you must download to complete the MyLib Project.

    • Basics to know to implement MyLib: To understand the basics of data structures required for MyLib, you can refer to ‘sp prj1 mylib.pdf’, which is available for download on Cyber Campus.

    • Skeleton code: You can begin the project by downloading ‘sp prj1 code.tar.gz’, which is provided on Cyber Campus, to a directory where you plan to work on the project.

    • Tester code: To verify your implementation, you need to download ‘sp prj1 tester.tar.gz’. You must implement MyLib to ensure it operates with every command in the file format of ‘*.in’.You can also execute the tester script with your interactive program ($ sh prj tester.sh ../20xxxxxx/testlib). This will generate ‘.output’ files that display the output contents of each test (‘.output’ 파일은 기존에 있는 ‘.out’ 파일과 비교됩니다. ‘.out’파일을삭제하지 않도록 유의하시기바랍니다). Result files will show the outcome of each test, and ‘Score.txt’ will reveal your total score.

    • Below are examples of commands used in the ‘*.in’ file. Your interactive program should work properly with each command as illustrated in the example.

– create list <LIST>: Creates LIST.

– create hashtable <HASH TABLE>: Creates HASH TABLE.

– create bitmap <BITMAP> <BIT CNT>: Creates BITMAP with the size of BIT CNT.

– delete <LIST | HASH TABLE | BITMAP>: Deletes the given data structure.

– dumpdata <LIST | HASH TABLE | BITMAP>: Prints the given datas in data structure to STDOUT.

– quit: Terminates the interactive program.

    • Simulation Example: Following is and example of running interactive program.

CSE4100: System Programming
Project #1: MyLib

list_shuffle list1



dumpdata list1


4 1 3
//-------> Output of 'dumpdata'


quit
//-------> Terminate the program

$~>








    • Project Description

In this project, you are required to implement the following functions for three data structures used in MyLib.

• List (in list.c):











Figure 1: Description of list swap function












Figure 2: Description of list shuffle function


• Hash Table (in hash.c):









Figure 3: Description of hash int 2 function


• Bitmap (in bitmap.c):









Figure 4: Description of bitmap expand function


After implementing the above functions, you have to write an interactive program that can test the functionalities of lists, hash tables, and bitmaps in the main function. (main function에서 sp prj1 tester 폴더 내의 ‘*.in’ 형식의 파일을 줄 단위로 읽고, 해당 줄의 명령어를 MyLib을 통해 수행한다고 생각하시면 됩니다. 따라서, sp prj1 tester 폴더 내의 ‘*.in’ 형식의 파일들의 모든 명령어가 올바르게동작해야합니다.)


You can utilize various functions of the three data structures and fix them if needed, to ensure the interactive program works correctly.


2
CSE4100: System Programming	Project #1: MyLib

Thus, an example of the contents in your working directory might look similar to Figure 5 (Note that you also need to create a Makefile).























Figure 5: List of contents in project folder

Also, during implementing requirements, you have to follow the assumptions below.

    1. All inputs are from standard input (STDIN).

    2. All inputs and outputs are lower cases.

    3. All the types used in the program are integer.

    4. Use hash int() as hash function for hash table, which is already given library (hash.c의 hash int()를사용할 것. 그래도 hast int 2는 구현하셔야 합니다).

    5. Use true or false when the return type is Boolean.

    6. The number of list, hash table and bitmap is less than or equal to 10.

    7. You can use any function in given source codes and you can implement your own code if it is needed.


Tip 1: You may find that your program becomes pended while testing list swap. Many students struggle with swapping the 0th and 1st elements.


Tip 2: When printing ‘size t’ type values with printf(), use the length sub-specifier, such as z, to preserve the data’s length. Ex. size t a=10; printf(“%zu”, a);






















3
CSE4100: System Programming	Project #1: MyLib

    • Submission Guideline

Hand-In Specifications:The submission should include only source code files, a Makefile, and documentation. No executable programs should be included. The TA responsible for grading your project will automatically rebuild your shell program from the provided source code. Please adhere strictly to the submission instructions below to avoid penalties on your overall project score.

    1. You must submit a single archive file named prj1‘ your student id .tar.gz’.

    2. Upon extracting the file, the root directory name should be your student ID.

    3. The executable file created by the Makefile must be namedtestlib (no other names are allowed).

    4. The document should be named ‘document your student id.docx (no formats other than .docx are al-lowed).


Attachment File:

    • Makefile: Failure to use a Makefile will result in no points being awarded.

    • Provided libraries: Files in the ‘sp prj1 code’ directory.

    • Your Source Code: For example, main.c, etc.

    • Document : Briefly explain all the library functions and the functions you wrote, including their function-ality, parameters, and return value.


Scoring:

    • 80% for test cases (implementation) and 20% for documentation.

    • Compilation failures will result in zero points.

    • Code Copy will incur penalties (1st time: 0 point and downgrade; 2nd time: F grade). Following is and example of a submission.


$~> ls
prj1_20241234.tar.gz

$~> tar -zxvf prj1_20241234.tar.gz

$~> ls
20241234	prj1_20241234.tar.gz

$~> cd 20241234

$~> ls -al
document_20241234.docx

bitmap.c

bitmap.h

debug.c

debug.h

hash.c

hash.h

hex_dump.c

hex_dump.h

limits.h

list.c

list.h

main.c

Makefile

round.h


All students are requested to upload their archived source files on eclass (Cyber Campus).



Note: Please ensure that you compile your source code on the CSPRO server, as the TA will build and compile your submitted project on that server. If the submitted code does not compile, it cannot be scored!



4
CSE4100: System Programming	Project #1: MyLib

    • Miscellaneous

5.1	Best practices the system programmers must comply to

WHAT YOU MUST DO:

    1. You must thoroughly read the entire data structure documentation to fully understand, learn, and complete this project.

    2. Ensure you read the project specifications before beginning your MyLib project programming.

    3. Commenting on your source code is a professional practice for programmers and is required for this project as well.

WHAT YOU MUST NOT DO:

    1. Do not submit any binary or object code files in your source code directory.

    2. Avoid including any hardcoded paths in your Makefile.

    3. Your Makefile must list all dependencies (libraries, etc.) required to build your program.

    4. Do not copy or share your source code with others. Doing so is strictly prohibited and will result in penalties.



WeChat: WeChat: **Programming Help ** Email: programmingtutor1@proton.me











