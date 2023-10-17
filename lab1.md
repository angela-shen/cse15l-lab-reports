# Lab 1
## ls
current working directory: `/home`

`ls` with no arguments shows the contents of the current directory, which in this case is `/home`. The command works as intended and does not produce an error.  

![Image](ls1.png)  

current working directory: `/home`

`ls` with a directory as an argument shows the contents of that directory, which in this case is `/home/lecture1`. The command works as intended and does not produce an error.  

![Image](ls2.png)  

current working directory: `/home`

`ls` with a file as an argument just shows the path to that directory, which in this case is `/home/lecture1/README`. The command works as intended and does not produce an error.  

![Image](ls3.png)  

## cd
current working directory: `/home/lecture1`

`cd` with no arguments returns the user to the home directory. If the user is in the home directory, the current working directory will not change. The command works as intended and does not produce an error.

![Image](cd1.png)   

current working directory: `/home`

`cd` with a directory as an argument changes the current working directory, in this case the argument given was `/home/lecture1`. The command works as intended and does not produce an error.  

![Image](cd2.png)  

current working directory: `/home/lecture1`

`cd` with a file as an argument produces an error. This is because change directory uses a path to a directory as an argument, so passing in a path to a file produces an error.  

![Image](cd3.png)  

## cat

current working directory: `/home`

`cat` with no arguments waits for user input and then outputs what the user types. To exit, use `ctrl + d`. The command works as intended and does not produce an error.  

![Image](cat1.png)  

current working directory: `/home`

`cat` with a directory as an argument states that the directory is a directory, in this case `/home/lecture1`. The command works as intended and does not produce an error.  

![Image](cat2.png)  

current working directory: `/home`

`cat` with a file outputs the contents of that file, in this case the contents of `/home/lecture1/README`. The command works as intended and does not produce an error.  

![Image](cat3.png)  

