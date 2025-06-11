# cs382-lab-3-solved
**TO GET THIS SOLUTION VISIT:** [CS382 Lab 3 Solved](https://mantutor.com/product/cs382-solved-5/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113831&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS382 Lab 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
&nbsp;

In this lab, we’re going to write and execute assembly programs for the first time.

1 Task 1: Install QEMU Emulator

Recall that assembly programs are closely related to the hardware platform they are performed on, so an assembly program written in ARM syntax cannot be executed on any other machines. Most of the time, however, we also want to execute ARM assembly on some other machines. In this case, we can install an emulator that can simulate the hardware execution of ARM machines on any type of machine. This is called cross-compilation. The emulator we are using is called QEMU.

To install QEMU on your virtual machine, type the following in your terminal:

Once you have finished the installation, you need to write the simplest ARM assembly program (the one listed in B.1.1 in textbook), and assemble and execute it. Upon success, there should be nothing printed out — no warnings or any type of output. To learn how to assemble, link, and execute an assembly program, read B.2.1 in textbook.

To get credits for attendance, show your CA that you have installed QEMU, and can assemble/link/execute the simplest ARM program. No submission needed.

2 Task 2: Write a Simple Program

One very common thing we do in programming is to print something to the screen. Although printing numerical numbers takes a bit more work, it is relatively much easier to print a string. In this task, you will learn how to declare a string, and how to invoke system call to print the string out. The code listed in B.1.1 in textbook is your starter code. Please learn how to declare data and load address by reading B.1.3 in textbook before starting this task.

Unlike high-level languages, in assembly, if we want to print a string, we have to declare it first in the .data segment:

To print this string out, we need to set several registers to correct values before invoking the system call, because the system needs to retrieve the information about this string from these registers:

Regis ter Content

X0 Destination (for printing, its value is 1)

X1 The address of the string to be printed

X2 The length of the string to be printed

X8 System call number (for printing, its value is 64)

1

Once these registers are ready, we can invoke the system call by using instruction: SVC 0 , and the string will be printed out!

Lastly, to terminate the program successfully, we need the following instructions:

Requirements Note your code is a complete assembly program (not just a sequence of instructions). It must be able to

assemble, link, and execute without error and warnings. When executed, the program must finish without problems;

If your code cannot assemble, you get no credit – this is the same to C programs that cannot be compiled;

You must declare the length of the string as a quadword in the .data segment;

You must put comments on every instruction you wrote; no need to comment on labels and directives;

3 Grading

Task 2 will be graded based on a total of 10 points. The following lists deductibles, and the lowest score is 0 – no negative scores: the code does not assemble, or the program terminates abnormally/unsuccessfully; the code is generated by compiler;

-2: the length of the string is not declared as a quad data in the .data segment; -2: one or more instructions is missing comments; -1: no pledge and/or name.

Attendance: show your CA completed task 1 and check off at the end of the lab to get attendance credit.

2
