# Process Management

## Overview
- I have just completed learning about process management in Linux, such as monitoring RAM and CPU usage, to understand active processes and their "health."
- This is important in cloud environments because it allows you to assess server conditions, identify issues, and determine how to resolve them.

## Core Concepts
When monitoring processes, several key aspects must be observed:
- RAM: Understanding how much memory each process is using.  
- CPU: Determining how much processing power a process consumes.  
- PID: Interacting with a specific process via its Process ID.

## Commands Learned

ps aux
Function: Displays a snapshot of PID, CPU, and RAM usage.

Basic Syntax:  
ps aux

Flags Used:  
- a: Shows all processes for all users.  
- u: Displays detailed process information (user, PID, CPU, RAM).  
- x: Includes processes not attached to a terminal.

Real Example:  
ps aux

htop
Function:  
Displays all processes in real time.

Basic Syntax:  
htop

Flags Used:  
— (None)

Real Example:  
htop

kill
Function:  
Sends a signal to a process, as signals are the system’s way of communicating with processes.

Basic Syntax:  
kill [PID]

Flags Used:  
- -SIGKILL or -9: Forcefully terminates a process without allowing it to clean up.

Real Examples:  
kill 37312  
kill -9 38712

sleep [Time in seconds]
Function:  
Pauses execution for a specified number of seconds.

Basic Syntax:  
sleep 120 &

Flags Used:  
- &: Runs the command in the background.

Real Example:  
sleep 160 &

jobs
Function:  
Lists processes currently running in the background.

Basic Syntax:  
jobs

Flags Used:  
— (None)

Real Example:  
jobs

fg
Function:  
Brings a background process to the foreground.

Basic Syntax:  
fg [%job_id] (Note: typically uses job numbers, not PID)

Flags Used:  
— (None)

Real Example:  
fg %1 (common usage; original example with PID is atypical)

free
Function:  
Displays memory and swap usage information.

Basic Syntax:  
free

Flags Used:  
- -h: Formats output in human-readable units (e.g., MB, GB).

Real Example:  
free -h

df
Function:  
Shows disk space usage information.

Basic Syntax:  
df

Flags Used:  
- -h: Human-readable output.

Real Example:  
df -h

## Experiments Conducted
I performed various experiments to observe processes:
- Used ps aux to view a snapshot of each process, showing PID, CPU, and RAM usage.
- Since ps aux only provides a static snapshot (not real-time), I used htop to monitor processes dynamically.
- Ran a background process with sleep 60 &, successfully placing it in the background, then brought it to the foreground using fg.
- Used the jobs command to list background processes.
- Finally, used free to check RAM status and df to examine disk usage.

## Relevance to Cloud Engineers
Process monitoring is highly relevant to cloud engineers because they must continuously observe every process on servers and assess their status. This enables them to quickly identify and troubleshoot server issues.

## Unanswered Questions
- If an issue is detected during monitoring, how should it be resolved?  
- What are common causes of server problems—such as high CPU load or RAM nearing full capacity?
