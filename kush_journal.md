# Journal.md

#### 2026/11/06 (0.9 hrs)
Worked on cleaning up the keyboard schematic. 

AT the beginning of this, the schematic looked a bit messy. 

<img width="2231" height="792" alt="image" src="https://github.com/user-attachments/assets/6841e309-b7a3-4132-947b-0ff09257f243" />

There were no net values (hence why the schematic look like a bunch of spaghetti), and there were no diodes in the keyboard (there were supposed to be). 

For the first little bit, I actually had to understand how this keyboard schematic worked because I had not built a project like this in the past. So, I found a great [doc](https://keeb.hackclub.com/docs/pcb-design/) that helped me really understand how this works. 

After that, I worked on adding net values to the columns and rows, and that's honestly about it for today. Here is my current progress:

<img width="1927" height="782" alt="image" src="https://github.com/user-attachments/assets/e662d520-a8da-44e0-ba1d-91de704d77ce" />

ALSO, this is my first time working in KiCad, coming over from EasyEDA so within this session, I had to do learn how to use KiCad and learn its shortcuts, etc. I've gotta say, though, I'm starting to get the hang of KiCad now!!

#### 2026/11/07 (0.9 hrs)
Worked on cleaning up the schematic again.

Honestly, I found a few too many mistakes in the schematic, so I figured I'd redo the schematic cleanly. This session, I tried to connect the columns, but some columns were misaligned, and some connections weren't done, so I figured I'd start from scratch and do it in a clean, grid-like pattern. 

Here is what I am at right now; I'm adding the diodes along the way (another reason why I thought to just start again) and I have 3 rows wired up: 

<img width="2217" height="701" alt="image" src="https://github.com/user-attachments/assets/622ff35a-1510-460e-bc2b-3bcf25060a7a" />

Honestly, going back and fixing the mistakes would take a lot longer than if I just started from the beginning and then did it!

#### 2026/11/07 
The actual layout of the keyboard schematic is a lot better now!

<img width="1457" height="722" alt="image" src="https://github.com/user-attachments/assets/cd90482b-ab55-48f1-bed9-565aff619781" />

#### 2026/11/07
Okay, finally, I can say that the keyboard schematic has now been connected to the RP2040. I also added no-connects to the RP2040 for now. 

<img width="1997" height="755" alt="image" src="https://github.com/user-attachments/assets/414e5986-ece0-4321-892a-94d84d7c5fc4" />

#### 2026/11/07
Learning something new every entry... 

Anyways, I worked on adding decoupling capacitors, a crystal oscillator, and QUAD SPI flash memory! These things were new to me (aside from decoupling capacitors) so I will try my best to summarize what I learned below ↓↓↓

A crystal oscillator generates a signal that is precise and has a steady frequency. Flash storage is faster than an HDD. A lot of boards already have flash memory built in, but our RP2040 does not have it, so we have to add it ourselves :)

Decoupling Capacitors: 
<img width="1066" height="149" alt="image" src="https://github.com/user-attachments/assets/de4e951c-a5c9-4225-bb6f-40e9035246ac" />

Crystal Oscillator:
<img width="278" height="201" alt="image" src="https://github.com/user-attachments/assets/120f8370-6266-464a-afb2-2c08eafc6391" />

Flash Storage:
<img width="506" height="338" alt="image" src="https://github.com/user-attachments/assets/f0589abf-5330-4ace-9a8d-79051a5ec24a" />

Full schematic:
<img width="1747" height="670" alt="image" src="https://github.com/user-attachments/assets/97bd4de2-739c-44cc-b82a-deb93ff20676" />




