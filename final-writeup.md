
# Final Writeup

## hacking into the box
To be honest, this wasn't my first experience with hackthebox so getting an access code wasn't as difficult as it was the first time around. But in the spirit of the final, I'll try and recall my initial thought process. 

When first visiting hackthebox.eu/invite you're prompted with a invite code entry and not much else to go off of. 

![cheat sheet](images/htb1.PNG)

My first inclination was to click furiously around the page hoping to trigger a invite code generation but that didn't go to well, so I eventually moved to inspect the input form itself. Upon further investigation into the page you can see a minified js file as an import, and what do you know it has a makeInviteCode exposed.

![cheat sheet](images/htb2.PNG)

After calling the inviteCode generator you get a request back from a server containing some base64 encoded text, once decoded the text says to send a post request to api/invite/generate. After sending a curl* request I got back my invitation code Woohoo!

* initially I had used a web-based http request generator and I ran into a IP specific error that blocked me for quite some time.


## you_can_do_it!.txt -Crypto Challenge 10 pts

![cheat sheet](images/ycdi.PNG)

## forest.jpg -Steganography Challenge 40 pts

![cheat sheet](images/forest.PNG)

## Cartographer -WebPenetration Challenge 30 pts

![cheat sheet](images/cartographer.PNG)


![cheat sheet](images/completion.PNG)
