# mbs-project-0-development-and-debugging-environment-exercises-solved
**TO GET THIS SOLUTION VISIT:** [MBS Project 0-Development and debugging environment Exercises Solved](https://www.ankitcodinghub.com/product/mbs-project-0-development-and-debugging-environment-exercises-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94263&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;MBS Project 0-Development and debugging environment Exercises Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
P0: 80×86 Development and debugging environment Exercises

Basic structure of programs in Assembly language 80×86

Open the “factor.asm” file in a text editor. The first remark is the definition of the different segments of the program (data, stack, extra and code). The order in which the definition of the different segments appear within the program source is indifferent. Not all segments are always present in all programs. For example, the extra segment may not be defined in some programs.

At the beginning of the code segment, you must use the ASSUME directive to associate the segments name with the segment to be used when accessing to the memory addresses in each segment. However, this is only a syntactic helper, and this directive does not load any value on the segment registers (DS, SS, ES), which should be assigned programmatically. The code to load these values should be at first in any program.

<pre>    MOV AX, DATOS
    MOV DS, AX
    MOV AX, PILA
    MOV SS, AX
    MOV AX, EXTRA
    MOV ES, AX
</pre>
Instructions can only be present in the code segment. However, the data can be defined in any segment. The default state is that the data are defined in the data/extra segments, but in this example we may observe a variable defined in the code segment. This is the reason why the program starts at address cs:0002 and not at cs:0000 (that is the default start).

To finish the program execution, it is used the 21H Interruption in conjunction with AX=4C00h. This combination takes the control back to the operating system.

In the last line of the file the ‘END’ directive shall be included and followed by the name of the procedure where the program execution should be started (entry) (in our example, it is the START procedure). When starting TD, the arrow marker will point right at the beginning of this procedure, and the IP register will be loaded with the corresponding memory address.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Variable visualization

</div>
</div>
<div class="layoutArea">
<div class="column">
Quite often while debugging the code with the “td”, it may be necessary to see the content of the variables used in our program that are stored in memory. For this it is necessary to modify slightly the makefile we created previously by replacing the last line

<pre>tasm /zi factor.asm
</pre>
by

<pre>tasm / zi factor.asm ,, factor.lst
</pre>
If we execute “make” after these changes (deleting the factor.obj and factor.exe files previously), we can observe by typing “dir” that an additional file has been created, called factor.lst. In this new file we can find first the correspondence between the Assembly instructions of our program and the instructions in machine code.

However, to see the content of the program variables we have to look towards the end of the file factor.lst since it contains the symbol table used in the program.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
The logical direction of any variables is decomposed in two pieces of information: a segment and an offset.

For example:

<pre>DATO_1: DATOS segment, offset 0
DATO_2: DATOS segment, offset 1
FACT_DATO_1: CODE segment, offset 0
RESULT: EXTRA segment, offset 0
</pre>
let’s run our program again on the “td”. This time, instead of running step by step with F7 key, we will place a breakpoint at the instruction

MOV AX, 4C00H

To do this, select the instruction with the cursor and the press F2. Move the cursor upwards to check that the breakpoint has been activated, (indicated with a red line)

</div>
</div>
<div class="layoutArea">
<div class="column">
Then execute the program pressing F9 key. The program will then be executed and stopped at the breakpoint. In this moment, the RESULT variable should contain its final value.

This value can be found in the data window, using “Goto ES: 0”.

Remember that EXTRA segment is associated to to the ES register through the directive ASSUME.

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Next images show the window data with the value 0C, that is, the value 12 in decimal (= 2! X 3!).

</div>
</div>
<div class="layoutArea">
<div class="column">
In the same way, we could inspect the rest of the variables of the program (DATO_1, DATA_2 and DATA_FACT_1), using “Goto DS: 0”, “Goto DS: 1” and “Goto CS: 0” respectively.

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Exercise 1: Factorial calculation

The program “factor.asm” has been designed to calculate the product of the factorial of a number by the factorial of another number. Make the appropriate modifications in the source code to calculate the following products with the help of TD. Record the results on a sheet in hexadecimal and decimal format, including a screenshot and a brief explanation of the changes and results obtained.

1. 4!x5!= 2. 8!=

3. 9!=

4. 8!x7!=

What is the value of FACT_DATO_1 on each case?

Exercise 2: “Factor” Program Modification

Modify the program “factor.asm” to calculate factorial of products instead of products of

factorials. When you are done, calculate the expressions shown below with the help of TD.

Record the results on a sheet in hexadecimal and decimal format, including a screenshot and a brief explanation of the changes and results obtained.

1. (2×3)!= 2. (2×4)!= 3. (3×3)!= 4. (5×2)!=

Exercise 3: “Alumno” Program Modification

The program “alumno.asm”, has been designed to ask the user for the introduction of a name

using the keyboard and print a line of text on the screen, using the input name.

You can find the program in the subfolder “alumnos” inside the “pra0” directory.

In this exercise you must repeat the process made with the “factor” program (i.e. assemble, link and run using the TD). This program can be also executed from the command line, since it includes input/output data by keyboard/screen.

Make the appropriate source code modifications to ask separately for the name, surname and country of the user, and then print a single line of text including the 3 previously entered fields. For instance: “John Doe (FROM United States) IS COURSING SECOND COURSE OF COMPUTER SCIENCE”.

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
During the debugging process, we can see what the program “alumno” is writing on screen by using the key combination ‘Alt+F5’.

Once the exercise is done you must add comments to the source code explaining all the changes performed.

ASSIGMENT SUBMISSION: CONTENTS

Exercises 1 and 2: A report must be upload to Moodle. It must contain the results, in both decimal and hexadecimal format, including screenshots of DosBox and a brief explanation of the modifications performed, as well as the results obtained.

Exercise 3: In this case you must upload a compress zip file containing both the source code and a makefile. The source code must include the comments with the modifications carried out and the student’s name in its header.

</div>
</div>
</div>
