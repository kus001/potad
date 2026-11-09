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

#### 2026/11/07
Honestly, here I just had a bunch of issues with Footprints in KiCad, which took me a while to figure out. My god, I am starting to notice the major differences between EasyEDA and KiCad. 

But in the end, here is what a part of the footprints looks like:

<img width="3434" height="1190" alt="image" src="https://github.com/user-attachments/assets/5e7cd760-c751-41f8-b814-bc1d7ccdb0f3" />

#### 2026/11/08
Today (and a bit of last night), I converted my schematic into a PCB and started arranging the switches for our keyboard. By now, I have completed the first row of the main (middle) keyboard.

<img width="1196" height="679" alt="image" src="https://github.com/user-attachments/assets/24895c29-63c5-4abd-a29b-3cd3ce9fae3f" />

#### 2026/11/08
Okayyyyy, row 2 has been placed onto the keyboard! 

I had to increase the width of the Edge.cuts layer because the switches+diodes were NOT fitting on the 145mm width. For now, the width has been raised to 152.5mm (I might increase it in the future to add more buffer, because right now everything is super tightly packed). 

<img width="1201" height="687" alt="image" src="https://github.com/user-attachments/assets/bfceb3df-6267-4824-a038-60c51498fcf8" />

#### 2026/11/08
Row 3 done! I have come to the realization that I need to do more electronic hardware projects... 

When I compare my software vs. electronic skills, there is definitely a difference. But anyways, you can get better at anything by practing!

Here is my current progress btw:

<img width="1199" height="685" alt="image" src="https://github.com/user-attachments/assets/b3ce58da-5dfc-4e4a-b44b-50039864f6d6" />

#### 2026/11/08
Row 4 done; only one more left on the big middle board.

<img width="1254" height="711" alt="image" src="https://github.com/user-attachments/assets/38c8f3c2-2387-4f07-8777-9104e51d7aa6" />

#### 2026/11/08
Row 5 done, now going to work on the 2 smaller parts of the keyboard.

3D:
<img width="1060" height="618" alt="image" src="https://github.com/user-attachments/assets/3799c9be-73d7-4dcf-9878-fad76b6a0003" />

Pcb:
<img width="1253" height="706" alt="image" src="https://github.com/user-attachments/assets/bf3fe676-dfe7-42d6-b6bd-65f701468ea7" />

#### 2026/11/08
Made the 2 smaller boards. This went by so much faster because at this point, I was in the flow state and had the method figured out.

Here is what the schematic is looking like right now:

<img width="1787" height="606" alt="image" src="https://github.com/user-attachments/assets/d51a8121-0626-4543-9a4b-d02cc192c443" />

<img width="1173" height="353" alt="image" src="https://github.com/user-attachments/assets/0c733449-2481-436f-912d-5ada8f985b7e" />

#### 2026/11/08
Here, I tried to route as much of the keyboard as I could. 

Honestly, I was not very familiar with the power part of POTAD, so I left any power-related routing to my teammates who worked on this project for a lot longer than we (me and Madhav) did. 

But yeah, a majority of the switches and diodes have been connected, the rows have been connected with each other (just missing the ribbon cable, but FlyingFish wants to handle that), and a couple of columns are still left to do. 

##### PCB 2D View

| Function keys | Arrow keys + some more |
|:---:|:---:|
| <img width="406" height="804" alt="image" src="https://github.com/user-attachments/assets/a6283754-965d-4649-a1dc-17057a7a5cc2" /> | <img width="597" height="797" alt="image" src="https://github.com/user-attachments/assets/cd2c21b5-f275-4f7e-b5c0-7d0584558a7c" /> |

| Main middle keyboard |
|:---:|
| <img width="1548" height="791" alt="image" src="https://github.com/user-attachments/assets/45279f69-076c-4f1d-8056-8287d88076b7" />|

##### PCB 3D View

| Function keys | Arrow keys + some more |
|:---:|:---:|
| <img width="244" height="483" alt="image" src="https://github.com/user-attachments/assets/0d38c6b3-e80f-41e0-8e59-aaf8535a7ceb" /> | <img width="355" height="475" alt="image" src="https://github.com/user-attachments/assets/9f7b81bd-f9a4-4769-a4ed-365124fd84d1" /> |

| Main middle keyboard |
|:---:|
| <img width="926" height="475" alt="image" src="https://github.com/user-attachments/assets/e0e3c9f4-4476-4916-828b-9b951c01ad68" /> |
