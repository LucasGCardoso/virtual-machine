# Virtual Machine and OS
A virtual machine, that runs a simple Operational System. Everything here is implemented in Java, for OS subject's final test, in PUCRS university. 

## Usage
- To run this project, after cloning it, you should simply run the ```Application.java``` file.
- To choose which program to run, just run the command ```s <PROGRAM_NUMBER>```. For instance: 's 1' runs the program ```p1.txt```
- To give values for the programs that require input, just type ``` c <INT_VALUE> ```. For instance: 'c 5' sends the number 5 to the console.
- The programs should be named as ```p<NUMBER>.txt``` to properly work
- In the end of each process, a memory dump is given, before clearing the process from the memory.

## Description
The OS, that runs in the virtual machine, simulates the basic aspects of a real OS, just as process management, memory management, memory pagination, PCBs, etc. The OS only accepts INT inputs. The processes that can run in it are individual programs, writen in its assembly language. You can also try writing new programs and run them. The group implemented this project using Java Threads as well, so that everything could be concurrent, just as in a real OS. Please note that all of this was made for learning pouposes only.

## OS Main Parts
In this section, you will cover al the basic classes of the OS and how they work and are related.

### GP
The GP, meaning Process Manager (Gerenciador de Processos), is reponsible for creating and finalizing processes. When created, the process is stored in a segment of the memory, which is allocated by the Memory Manager (GM), and then, it is sent to the Ready Queue. When finalized, the process is cleared from the memory. 

### GM
This is the Memory Manager (Gerente de Memória), responsible for allocating and deallocating the memory, mapping each program to its correct memory frame.

### Thread Escalonador
This class is treated as a Java Thread, and its responsible for coordinating which process goes to the CPU (to run) and which ones keep waiting or keep blocked.

### Thread CPU
The CPU is also a Thread, and it executes each assembly command the processes have, running them, one by one, until the running process gets interrupted by timer, STOP command, or some errors, such as Illegal Memory Access.

### Rotinas
The Routines contain a bunch of functions, that are executed for each specific Interruption the CPU generates. For instance, when a process stops, reaching the STOP command, a routine is called, clearing the process from the memory, and putting the next one in the CPU.

### Thread Application (Shell)
This is the Shell of the OS, responsible for reading the entries of the user, that chooses the next program to run.

### Thread Console
The console is responsible for printing eventual outputs the process can return. It also waits a process to call for an input, asking it for the user. Please, note that our OS only accepts INT inputs.


## Programs
 - p1.txt: Executa os 10 primeiros números da sequência de fibonacci.
 - p2.txt: Um programa que le um valor de uma determinada posição (carregada no inicio),
            se o número for menor que zero coloca -1 no início da posição de memória para saída;
            se for maior que zero este é o número de valores
            da sequencia de fibonacci a serem escritos em sequencia a partir de uma posição de
            memoria;
 - p3.txt: Calcula o fatorial de um número
 - p4.txt: Ordena um vetor por bubble sort.
 - p5.txt: Dada a entrada de um numero 'n' inteiro, o p5 calcula os n primeiros numeros da sequencia de fibonacci, depois dos dois primeiros numeros da sequencia.
           Ex.: Entrada 5 retorna os valores 0 1 1 2 3 5 8.
 - p6.txt: Calcula os 50 primeiros numeros de fibonacci, dando erro de acesso de memoria para fins de simulaçao de erro.
 - p7.txt: Calcula o fatorial de um numero e escreve o seu valor pelo Console, para fins de simulaçao de saída.
