Writing Your Own System Call


As described in the class, the OS provides operations to users via system calls.
System calls are functions, natively available to users via C library functions,
provide access to almost all OS level functionality – viz. open(), write(),
fork() etc.
You have to create your own system call in C, called sh task info(), which
takes argument as PID. It would need to search out the task struct() corresponding to the PID and print out all the fields corresponding to it and also
save it in a file. The file name also needs to be supplied as an argument to the
system call.
You also would require to handle errors in user inputs, such as incorrect arguments, through appropriate errno and function return values (e.g. 0 signaling
correct input, while 1 signaling incorrect input).
You are supposed to use Linux/kernel distribution that you used for Assignment 0 part 1. For the assignment, you need to modify the kernel source to add
the appropriate system call.


What To Submit
• You need to submit the diff, of the originally downloaded kernel source
tree and the one with your changes. This patched code MUST match the
one you have in our kernel source (running on a VM). We would verify
this at the time of the demos.


• Write-up describing the following:
– Description of your code and how you implemented the function –
the logical and implementation details.
– The inputs the user should give.
– Expected output (and how to interpret it).
– Error values and how to interpret them.
• A sample C program to test out your implementation of the system call.


Grading Rubric
• Successful compilation your diff against the base kernel source – 10 points.
• Correct functioning of your system call, testable through the supplied C
program – 20 points.
• Correct handling of input errors (atleast two different types of errors
should be handled) – 10 points.
• Description of the systems, how to test the system through your supplied
C program and what to expect etc. – 5 points
