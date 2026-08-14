# FTA - File Transfer App

![](C:\Buisness\FTA---SHOWCASE\resources\image - UI Main.png)

This is FTA its a C++ app using win32 and Direct2D for rendering. while the actual file transfer doesnt currently work. discovery does work, it can play gifs as animations, it has text box with proper cursor logic, clipboard support, it generates a unique id. uses diffie-hellman to create a secure channel for communication, it also uses a custom network protocol, it has device discovery using broadcasts. at the time i was also looking at using BLE but information on how to use ble on windows is limited or outdated. 

DOCUMENTATION:

https://github.com/Joshua-J-G/FTA---SHOWCASE/blob/main/FTA%20Documentation.pdf



![](C:\Buisness\FTA---SHOWCASE\resources\image - UI Stamp.png)

This is the ui for creating icons. so while developing this i had a problem. user icons. i wanted to give people the ability to customise there devices to make identifying them at a glance easier. problem was uploading images would be problematic. why because i use broadcasts anyone on the network who can reverse engineer the protocol can advertise right. this means they can show images on other people computer through the application. this create a huge problem unless you have image detection software, so instead of trying to solve user uploads i create an icon system. this system gives you a set of shapes. which you can colour, and place on a canvas which you can select the colour of. you can rotate, resize, and delete shapes that you already have added. furthermore it saves the last 10 icons you used. there was an object limit to stop people from ddosing other people computers that limit was 80 stamps. after that i encoded the ids, position, rotation, size and colour of those stamps in a base64 string and sent that along with the heartbeat. i did it this way as it provides almost instant updates when a user changes name, or icon. 



with heart beats there was also a retry method. so if someone couldn't find a specific user they would ask for them. if they failed to respond they would be removed from the list. 



![](C:\Buisness\FTA---SHOWCASE\resources\image - UI List.png)

when i stopped working on this project. i was up to creating lists. i originally stopped for 2 reasons. 1 I wanted to create apps. right but realised that im doing all this work for a ui library then making it unusable by interconnecting it with a file transfer app. and that i would have to remake it for any other future apps. 2 on some peoples computer when i was testing it. some rendering would look odd. especially on release builds. 



Anyway i hope you enjoy looking through the code. some of which is messier than i like. i have gotten considerably better at documentation since this experience and have worked on other cool items. 



Thank You 

Joshua Gessner