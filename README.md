# Virtual Machine and OS
A virtual machine, that runs a simple Operational System. Everything here is implemented in Java, for OS subject's final test, in PUCRS university. 

## Description
The OS, that runs in the virtual machine, simulates the basic aspects of a real OS, just as process management, memory management, memory pagination, PCBs, etc. All of this was made for learning pouposes only. The processes that can run in it are individual programs, writen in its assembly language. You can also try writing new programs and run them. The group implemented this project using Java Threads as well, so that everything could be concurrent, just as in a real OS.

## OS Main Parts
In this section, you will cover al the basic classes of the OS and how they work and are related.

### GP
The GP, meaning Process Manager (Gerenciador de Processos), is reponsible for creating and finalizing processes. When created, the process is stored in a segment of the memory, which is allocated by the Memory Manager (GM), and then, it is sent to the Ready Queue. When finalized, the process is cleared from the memory. 
### GM
This is the Memory Manager (Gerente de Memória), responsible for allocating and deallocating the memory, mapping each program to its correct memory frame.
### Thread Escalonador
### Thread CPU
### Rotinas
### Thread Shell
### Thread Console

## Usage
COMANDOS
 - Rodar Application.java;
 - Para escolher o programa, rodar o comando 's <numero do programa>'. Ex.: 's 1' roda o programa p1.txt
 - Para digitar valores nos programas que solicitam entrada, digitar 'c <valor>'. Ex.: 'c 5' envia o número 5 para o console.

## Programs
PROGRAMAS
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
