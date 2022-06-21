# Multithreaded_TicTacToeServer
This is a multithreaded tictactoe application implemented in C where players can join to the server.This game utilized Linux sockets programming (TCP/IP) to provide for a networked gaming experience.

Used mutex locks to avoid race conditions when multiple clients tries to access the critical section.
## Guidelines to run(Include all dependencies)
  1. Install gcc compiler
  2. [Click this for a video demo](https://drive.google.com/file/d/153g_Y-dZkiSnC1qc_gfP8N9RrJFPIh2N/view?usp=sharing)
  3. Open the Ubuntu terminal and change the directory to the project.
  4. First setup the server.
  5. make a connection request from client side.
  6. After a succesful coonection of both the clients enjoy the game!!
  7. Open the command file which is attached and look at the different commands used.
## Concepts of working scheme
  #### Server
   * Creates a new thread for each client that connects
   * Mutexes used for avoiding race conditions of critical section(in this case, count of the active clients).
   * Listens to the client inputs and passes it over the network
      
  #### Client
   * Connects to the server over TCP/IP
   * Retrieves and validates user input
   * Displays results of each move in the console
 
## Internal working
  1. On the server side it shows number of active players.
  2. After two players has joined the game, the client who joined first will be given the first chance to play.
  3. The players will not be allowed to place their current coin in an already allocated position.
  4. After each player's move, board is updated and checks the state of the game and send the messages to both the players in the network accordingly.
  5. If any of the row or column or diagnol is matching then that player will be said to be won or if there is no outcome then its a draw.
  6. After the completion of the game both of the clients connections will be terminated.

## Additional tasks implemented
  1. Printing the number of active clients using mutex locks.
  2. sending the feedback messages to both the clients after every chance.(Like printing players count after every new player arrival and so on.. many other similar  things)
  3. 50 players can play this game at a time (grouping will be done pair wise based on their arrival time).

## Learnings
 Got to know about socket programming, client server model and understood the uses of OS concepts like multi threading and mutex in real life.

