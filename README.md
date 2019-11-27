# Parallel_Banking
To implement a distributed banking system where the different terminal windows will simulate the independent clients/users which will try to simultaneously access a server emulated by a database and controlled by a java program. Once they are granted the access they can perform basic transaction operations like deposit, withdrawal, inquiry and bank statement receipt. 

## Software Requirements
• Eclipse IDE 
• JDK (Java Development Kit) 
• JRE (Java Runtime Environment) 
• Windows Command Line (module of Windows OS) 

## Compilation Steps 
Open a command prompt window. Navigate to the source code directory. 
Type: javac -cp interfaces\*.java  
This will compile the interfaces into .class files. 
Next Type: javac client\ATM.java  
This will compile the client files. 
Next Type: javac server\*.java 
This will compile the server files. 
Next Type: rmiregistry 7777 
This will start the RMI at port 7777. 
In a new command window, 
Type: java -Djava.security.policy=all.policy server.Bank 7777 
This will start the server, grant it permissions and bind it to port 7777. 
In a new command window,  
Type: java client.ATM localhost 7777 login user1 pass1  
This will start ATM client and login to user1.
