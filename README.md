# Multithreaded_TicTacToeServer
This is a multithreaded tictactoe application implemented in C where players can join to the server.This game was developed in C and utilized Linux sockets programming (TCP/IP) to provide for a networked gaming experience.

Used mutex locks to avoid race conditions when multiple clients tries to access the critical section.
## Guidelines to run(Include all dependencies)
  1. Install gcc compiler
  2. [Clik this a video demo](https://drive.google.com/file/d/153g_Y-dZkiSnC1qc_gfP8N9RrJFPIh2N/view?usp=sharing)
  3. Open the Ubuntu terminal and change the directory to the project.
  4. First setup the server.
  5. make a connection request from client side.
  6. After a succesful coonection of both the clients enjoy the game!!
  7. Open the command file which is attached and look at the different commands used.
## Working(Try to explain the theory of your project in this part)
  #### Server
      * Creates a new thread for each client that connects
      * Mutexes used for avoiding race conditions of critical section(in this case, count of the active clients).
      * Listens to the client inputs and passes it over the network
      
  #### Client
      * Connects to the server over TCP/IP
      * Retrieves and validates user input
      * Displays results of each move in the console

## Learnings

## Additional task
