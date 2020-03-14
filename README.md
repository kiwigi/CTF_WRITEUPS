# b01lers CTF

# Web: 

Welcome to Earth (100p)
When you click on the link in the challenge description you're brought to 
http://web.ctf.b01lers.com:1000/
Where it wants you to play an almost impossible minigame since the page keeps going to http://web.ctf.b01lers.com:1000/die/.
----
Basically, I used the curl linux command to vide the source code since it kept refreshing too fast for me to properly look at at. When I did this, I basically just examined the code of the webpage and found the link to the next page! 
Eg: when you enter 'curl http://web.ctf.b01lers.com:1000/' it will spit out the site's source code and in it you will find an instruction that brings you to /die/ but there's another one that brings you to /chase/, which is where you wanna go to advanse the mini-game. You basically keep doing this until you get to the /fight/ part. Here we can open it in a browser and take a look at it's source code using the normal right click method. Brows over to the 'Sources' tab to find the 'fight.js' file. When you look at the code for it, you can see that the flag is at the bottom! It's just scambled. 
I'm not sure if we were supposed to do another step to un-scramble it, but it's fairly easy to un-scramble it to fit the flag format and we get:
Flag:pctf{hey_boys_im_baaaaaaaaaack!}
