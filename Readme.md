<div align= >

# 🖥️ Operating System Scheduler


</div>
<p align="center">
   <img align="center" width=600px height=450px src="https://cdn.dribbble.com/users/1243527/screenshots/4928430/file-transfer.gif" alt="logo">
</p>

<p align="center"> 
    <br> 
</p>

## 📝 Table of Contents

- <a href ="#about"> 📙 Overview</a>
- <a href ="#Started"> 💻 Get Started</a>
- <a href ="#Path"> 🎯 Path of the program</a>
- <a href ="#Work"> 🧱  Data Structures Used </a>
- ⚙<a href ="#Algorithms">  Algorithms Explanation</a>
- <a href ="#Assumptions"> 📃 Assumptions</a>
- <a href ="#Structure"> 📁  File Structure</a>
- <a href ="#Contributors"> ✨ Contributors</a> 
- <a href ="#License"> 🔒 License</a> 
<hr style="background-color: #4b4c60"></hr>

 <a id = "about"></a>

## 📙 Overview
<br>
<ul> 
<li>
A CPU scheduler determines an order for the execution of its scheduled processes.</li>
<li>It decides which process will run according to a certain data structure that keeps track of the processes in the system and their status.</li>
<li>A process, upon creation, has one of the three states: Running, Ready, Blocked (doing I/O, using other resources than CPU or waiting on unavailable resource).</li>
<li>
A bad scheduler will make a very bad operating system, so your scheduler should be as much optimized as possible in terms of memory and time usage.
</li>

<li>
The project has 2 phases.</li>
<br>

 - <a href="https://github.com/AdhamAliAbdelAal/OS-Project/blob/master/Docs/Project%20Phase%201.pdf">Project Phase 1</a>
 - <a href="https://github.com/AdhamAliAbdelAal/OS-Project/blob/master/Docs/Project%20Phase%202.pdf">Project Phase 2</a>
 
<br>
<li> Build using <a href="https://en.wikipedia.org/wiki/C_(programming_language)">C lnaguage</a>.</li>
</ul>
<hr style="background-color: #4b4c60"></hr>
<a id = "Started"></a>

## 🚀 Get Started 

<ol>
<li>Clone the repository.

<br>

```
git clone https://github.com/AdhamAliAbdelAal/OS-Project
```

</li>
<li> You will need to download platform <a href="https://www.linux.org/">Linux</a>. </li>
<br>
<li>  Install a C Compiler on Linux if you haven't.

<br>

```
sudo dnf install gcc
```
</li>
</ol>
<hr style="background-color: #4b4c60"></hr>


## 🗺️ Path of the program <a id ="Path"></a>

<ol>
<li>Go to folder <a href="https://github.com/AdhamAliAbdelAal/OS-Project/tree/master/Phase%201/code">Phase 1 </a>
or  <a href="https://github.com/AdhamAliAbdelAal/OS-Project/tree/master/Phase%202/code">Phase 2 </a> , as you want.

</li>
<li>Put input in file "processes.txt" or run file "test_generator.c" and it will put random input </li>
<br>
<ul><li>Phase 1</li>
<div  align= "center"  >
<br>

 <img width=300px height=80x src="https://user-images.githubusercontent.com/71986226/182129022-8e52e601-cb15-4ada-9ce5-64834521d84f.png">

 </div>
 <li>Phase 2</li>
<div  align= "center"  >
<br>

 <img  width=300px height=80x  src="https://user-images.githubusercontent.com/71986226/182179357-966b00d5-0609-4bb4-b986-5b34f9057744.png">

 </div>
 </ul>
<br>
<li>Open terminal</li>
<li> Build file process_generator.c.</li>

<br>

```
gcc process_generator.c -o ex
```

<li> Run ex.</li>

<br>

```
./ex
```
<br>
<li>Choose a scheduling algorithm.</li>

<br>
<table>
<tr>
<td>Input</td>
<td>Algorithm</td>
</tr>
<tr>
<td>1</td>
<td>Non-preemptive Highest Priority First (HPF)</td>
</tr>
<tr>
<td>2</td>
<td>Shortest Remaining time Next (SRTN)</td>
</tr>
<tr>
<td>3</td>
<td>Round Robin (RR)</td>
</tr>
</table>
<div  align= "center"  >
<br>
 <img  src="https://user-images.githubusercontent.com/71986226/182130330-a6f0caad-70fa-4a68-a14c-631d28132a82.png">

 </div>
<br>
<li>
There are 2 output file "scheduler.Log" and "scheduler.perf". "memory.log" is created in phase 2.
<ul>
<br>
<li>scheduler.Log
<div  align= "center"  >
<br>

 <img width=600px src="https://user-images.githubusercontent.com/71986226/182129431-22801211-7e73-4b94-a1c0-6eb473ebefa9.png">

 </div>
</li>
<br>
<li>scheduler.perf
<div  align= "center"  >
<br>

 <img src="https://user-images.githubusercontent.com/71986226/182129632-ec5c139e-4ced-4506-a482-58222727a1ea.png">

 </div>
</li>
<li>memory.log
<div  align= "center"  >
<br>

 <img width=600px src="https://user-images.githubusercontent.com/71986226/182178875-e9f4f08b-a5fe-4f49-bc03-31d85d49a14d.png">

 </div>
</li>
<ul>
</li>
</ol>
<hr style="background-color: #4b4c60"></hr>
 <a id="Work"> </a>

## 🏗️ Data Structures Used 
<br>
<ol>
<li>Queue</li>
<li>Priority Queue</li>
<li>Process Data
<ul>
<li>Arrival time</li>
<li>Priority</li>
<li>Run time</li>
<li>ID</li>
<li>Memsize</li>
</ul>
</li>
<li>Memory Node
<ul>
<li>Size</li>
<li>Start</li>
<li>Pointer to the next memory node</li>
</ul>
</li>
<li> PCB for each process
<ul>
<li>ID</li>
<li>PID</li>
<li>Arrival time</li>
<li>Burst time</li>
<li>Finish time</li>
<li>Running time</li>
<li>Stop time</li>
<li>Priority</li>
<li>Start time</li>
<li>Start Address in memory</li>
<li>Memory Size</li>
</ul>
</li>
</ol>
<hr style="background-color: #4b4c60"></hr>
 <a id ="Algorithms"></a>

## 🧠 Algorithms Explanation
<br>
<ol>
<li>HPF
<ul>
<li>The main loop checks if the processes are all finished or not. </li>
<li>In an inner loop, we get all the processes arrived at this particular second and enqueue them in the ready queue.</li>
<li>If there is no current process and the ready queue isn’t empty, we directly pop from the ready queue as it’s already sorted with the minimum priority, then start the process, fork it, and execl Process.c.</li>
<li>Last check: If the remaining time of the running process is zero, then it is finished and the running process is set to NULL. The finished processes counter is incremented as well and the loop continues.</li>
</ul>
</li>
<li>SRTN
<ul>
<li>Receiving the processes from the process generator.</li>
<li>Checking if the coming process's burst time is smaller than the remaining time of the running process.</li>
<li>If it's smaller than the running process will be added to the ready queue and saved in stop resuming queue and the smaller one will be the running process.</li>
<li>Then every time we a process starts then we check if this process was stopped before “existing in stop resuming queue" or not to know if it started or resumed to resume the stopped process.</li>
</ul>
</li>
<li>RR
<ul>
<li>Check if there are arriving processes, receive them in ready queue.</li>
<li>Check if there is a processes finished or the time slot ended, change the state of the process from running to finished or ready respectively.</li>
<li>Check if there are processes in ready queue and no process is running so pick up one of them and run it.</li>
</ul>
</li>
</ol>
<hr style="background-color: #4b4c60"></hr>
<a id ="Assumptions"></a>

## 📜 Assumptions
<br>
<ol>
<li>
In the memory waiting queue, it is implemented as a priority queue based on the algorithm so if it’s a SRTN, the priority is the remaining time while for RR, it is based on the memory size where the smaller one gets put into the ready queue first. As for the HPF, there is no need since the running process is the only one put into the ready queue.
</li>
<br>
<li>
We made an array of arrivals in the process generator as a shared memory with the scheduler in order to make sure that any process arriving at a specific time is read by the scheduler and not skipped.
</li>
<br>
<li>We synchronize between the stopped process and the arrived one if they come in the same second so that the stopped process is put into the queue before the arrived process.
</li>
</ol>
<hr style="background-color: #4b4c60"></hr>
<a id="Structure"> </a>

## 🗃️ File Structure 
<br>
<div align= center>
<img   src="https://user-images.githubusercontent.com/71986226/182103221-e5d5b882-f846-4794-814f-5f42403948a8.png">
</div>

<hr style="background-color: #4b4c60"></hr>

## 👑 Contributors <a id ="Contributors"></a>

<table align="center" >
  <tr>
     <td align="center"><a href="https://github.com/AbdelrahmanNoaman"><img src="https://avatars.githubusercontent.com/u/76150639?v=4" width="150;" alt=""/><br /><sub><b>Abdelrahman Noaman</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/abdelrahman0123"><img src="https://avatars.githubusercontent.com/u/67989900?v=4" width="150;" alt=""/><br /><sub><b>Abdelrahman Hamdy</b></sub></a><br /></td>
     <td align="center"><a href="https://github.com/AdhamAliAbdelAal" ><img src="https://avatars.githubusercontent.com/u/83884426?v=4" width="150;" alt=""/><br /><sub><b>Adham Ali</b></sub></a><br />
    </td>
     <td align="center"><a href="https://github.com/EslamAsHhraf"><img src="https://avatars.githubusercontent.com/u/71986226?v=4" width="150;" alt=""/><br /><sub><b>Eslam Ashraf</b></sub></a><br /></td>
  </tr>
</table>

## 🔒 License <a id ="License"></a>

>This software is licensed under MIT License, See [License](https://github.com/AdhamAliAbdelAal/MP-Processor-Game/blob/master/LICENSE) for more information ©AdhamAliAbdelAal.
