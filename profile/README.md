# FTP Client-Server

In this client-server project, a client can request a file or a set of files from the server. The 
server searches for the file/s in its file directory rooted at its ~ and returns the tar.gz of the 
file/files requested to the client (or an appropriate message otherwise). Multiple clients can 
connect to the server from different machines and can request file/s as per the commands such as:

findfile filename
o If the file filename is found in its file directory tree rooted at ~, the server must 
return the filename, size(in bytes), and date created to the client and the 
client prints the received information on its terminal. 
 Note: if the file with the same name exists in multiple folders in the 
directory tree rooted at ~, the server sends information pertaining to 
the first successful search/match of filename
 Else the client prints “File not found” 
o Ex: C$ findfile sample.txt

sgetfiles size1 size2 <-u> 
o The server must return to the client temp.tar.gz that contains all the files in 
the directory tree rooted at its ~ whose file-size in bytes is >=size1 and <=size2 
 size1 < = size2 (size1>= 0 and size2>=0) 
o -u unzip temp.tar.gz in the pwd of the client 
o Ex: C$ sgetfiles 1240 12450 -u

quit 

o The command is transferred to the server and the client process is terminated


[screen-capture.webm](https://user-images.githubusercontent.com/70006863/234746255-745a3a51-1222-4f27-ba87-43fe98d9c064.webm)
