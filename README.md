# HW3_21900400
youtube link: https://youtu.be/yuDX7QLsOMM
-printing lines using an address when found by typing a word containing the address.
-Uses named pipes and forks to create code.    
<h1>pfind.c</h1>
  <h3> Queue </h3>
     <h5> Node : Node struct, createNode,getData, setLink, getLink</h5>
     <h5> Queue : IsEmpty, createQueue, enqueue, dequeue, peek, printQ,freeQueue</h5>
  <h3> handler </h3>
    <h5>Intended to terminate in accordance with the signal.</h5>
  <h3> worker </h3>
    <h5> The address should be received through the pipe</h5>
    <h5>Insert the directory through openir and read through the other file names in the file if nothing is missing</h5>
    <h5>Copy the address to the dirpath and paste the slash and the found file name through strcat to create the absolute address</h5>
    <h5>Distinguish file</h5>
    <h5>- dir: Directly into the pipe and put it in the manager function.</h5>
    <h5>- regular file: Open the file and read it. </h5>
    <h5>Add one more line to find each line, and if there is a word that you received as input, you can use datapath, the whole line, and the number of the line number</h5>
    <h5>- Link: if link, ignore it and worker's worker is done. </h5>
   <h3>read_bytes and write_byte</h3>
    <h5>functions below are functions for using pipe.</h5>
   <h3>Main Function</h3>
    <h5>Input variable from case to case, so specify variables, declare and assign them well to the appropriate location</h5>
    <h5>Analyze the case of options to go to the desired function and perform the action if there is an option.</h5>
    <h5>Make a queue and put the first address in the queue, and after the fork, pull out the address in the task one by one from the child process </h5>
    <h5>Hand it over to the worker with the word. And if you are done, you can type through signal, or when the user sends a type signal, you can type all the workers and finish the program. </h5>
    
<h1>More Detail</h1>
<h4>In this program, though not all of them are implemented, the dir received as shown in the picture is put in the queue. In the process of dequeuing the directory in the queue, the directory address is passed to the worker function through the pipe. And when the worker is finished, give the subdirectory address inside to the manager again and queue it in the queue and save it. And if there is an empty space in the worker, you can repeat the process by putting it in one by one. And through the signal function, it was understood that it was a program to measure time and to make the worker type and the program type safely when time passes.</h4>
<img width="602" src="https://user-images.githubusercontent.com/63308012/115028992-76fc6180-9f00-11eb-99cc-c4d233893cde.jpg">

<h1>Running a program</h1>
<img width="602" alt="스크린샷 2021-04-16 오후 6 50 41" src="https://user-images.githubusercontent.com/63308012/115028747-30a70280-9f00-11eb-9ee0-a8229541aa8c.png">
