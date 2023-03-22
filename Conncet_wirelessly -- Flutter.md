Heyyy there

Name: 
Running flutter app on android wirelessly

1 => connect you smartphone to your pc/laptop and in the project diretory in terminal enter the command
    
    **adb tcpip 5555**
  
 this should give you an output 
 **restarting in TCP mode port: 5555**
 
 2 => Now run the command **tcpip connect "ip address of your mobile device" ** 

This will establish a connection between pc/laptop and your mobile phone 
now you can disconnect your mobile phone and run flutter app wirelessly
