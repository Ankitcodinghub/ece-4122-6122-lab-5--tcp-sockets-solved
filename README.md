# ece-4122-6122-lab-5--tcp-sockets-solved
**TO GET THIS SOLUTION VISIT:** [ECE 4122/6122 Lab 5- TCP Sockets Solved](https://www.ankitcodinghub.com/product/ece-4122-6122-lab-5-tcp-sockets-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;127133&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE 4122\/6122 Lab 5- TCP Sockets Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
(100 pts)

Category: sockets

Objective:

Implement a TCP server and TCP client application that can be used to receive and send messages from multiple clients.

Description:

Write a console program that takes as a command line argument the port number on which the TCP Server will listen for connection requests. A separate thread shall be created to handle the data received from each remote client and the remote clients can continue to send and receive data on the connections until either the server or the client closes the connection. The TCP server needs to maintain a list of all connected clients so that it can send out the appropriate messages. The TCP server needs to be able to receive data from clients without blocking the main application thread. The program needs to respond to user input while handling socket communications at the same time. You are free to use the SFML socket sample as a starting point.

Server-60 points

1) The program should continuously prompt the user for commands to execute like so:

Please enter command: msg – prints to the console the last message received (if any) Last Message: last message received

Please enter command: clients – prints to the console a list of all connected clients (ip address and port number) like the following:

Number of Clients: 2

IP Address: localhost | Port: 51717

IP Address: localhost | Port: 51718

Please enter command: exit – closes all sockets and terminates the program

2) The data being sent back and forth will use the following packet structure:

struct tcpMessage

{ unsigned char nVersion; unsigned char nType; unsigned short nMsgLen; char chMsg[1000];

};

The TCP server needs to have the following functionality for received messages:

• If nVersion is not equal to 102 then the message is ignored.

• If nType == 77 then the message should be sent to all other connected clients exactly as received (but not the client that sent the message).

• If nType == 201 then the message is reversed and sent back to only the client that sent the message.

Client-40 points

In order to test your server, write a console program that takes as a command line argument the IP Address and port number of the server as shown below:

./a.out localhost 51717

The program should prompt the user for inputs and display any messages received.

Here are example user inputs:

Please enter command: v # the user enters a “v”, a space, and then a version number. This version number is now used in all new messages.

Please enter command: t # message string the user enters a “t”, a space, and then a type number, followed by the message. Be sure you are able to handle the spaces in the message string.

Please enter command: q the user enters a “q” causes the socket to be closed and the program to terminate.

Any messages received from the server should be displayed as followed:

Received Msg Type: #; Msg: message received

Turn-In Instructions

Zip up your server file(s) into Lab5Server.zip and your client files into Lab5Client.zip upload these zip files on the assignment section of Canvas.

Grading Rubric:

AUTOMATIC GRADING POINT DEDUCTIONS PER PROBLEM:

Element Percentage Deduction Details

Does Not Compile 40% Code does not compile on PACE-ICE!

Does Not Match Output Up to 90% The code compiles but does not produce correct outputs.

Clear Self-Documenting Coding Styles Up to 25% This can include incorrect indentation, using unclear variable names, unclear/missing comments, or compiling with warnings. (See Appendix A)

LATE POLICY

Element Percentage Deduction Details

Appendix A: Coding Standards

Indentation:

When using if/for/while statements, make sure you indent 4 spaces for the content inside those. Also make sure that you use spaces to make the code more readable. For example:

for (int i; i &lt; 10; i++)

{ j = j + i;

}

If you have nested statements, you should use multiple indentions. Each { should be on its own line (like the for loop) If you have else or else if statements after your if statement, they should be on their own line.

for (int i; i &lt; 10; i++)

{

if (i &lt; 5) { counter++; k -= i; } else

{ k +=1; } j += i;

}

Camel Case:

This naming convention has the first letter of the variable be lower case, and the first letter in each new word be capitalized (e.g. firstSecondThird).

This applies for functions and member functions as well!

The main exception to this is class names, where the first letter should also be capitalized.

Variable and Function Names:

Your variable and function names should be clear about what that variable or function represents. Do not use one letter variables, but use abbreviations when it is appropriate (for example: “imag” instead of

“imaginary”). The more descriptive your variable and function names are, the more readable your code will be. This is the idea behind self-documenting code.

File Headers:

Every file should have the following header at the top

/*

Author: your name

Class: ECE4122 or ECE6122 (section)

Description:

What is the purpose of this file?

*/

Code Comments:

1. Every function must have a comment section describing the purpose of the function, the input and output parameters, the return value (if any).

2. Every class must have a comment section to describe the purpose of the class.

3. Comments need to be placed inside of functions/loops to assist in the understanding of the flow of the code.
