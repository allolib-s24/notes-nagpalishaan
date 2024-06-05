All code linked in demo repo: https://github.com/allolib-s24/demo1-nagpalishaan

# Simple Melody
This is my Mom's version of Do-Re-Mi that she would sing to my as a child. It is slower than the original.


https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/fee3ee53-450a-4dfe-b592-f1b4e4dd9dd6


# Sound Design Project: 
This is a good path for sound design for beginners.
Personally, I wasn’t too familiar with music theory and Professor Conrad went through a technique for people struggling with. I wanted to develop a Trumpet and Professor Conrad suggested a method using FM synthesis. Here is the steps I took and how to replicate.
1. Open FM synthesis
2. Go to the idx1 value and start moving it left and right (binary search) until you get a sound that is closer to a trumpet.
![Screenshot 2024-06-02 234539](https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/c9a09356-1073-4bb0-a652-baeea5681883)

3. Repeat the above step for idx2 and idx3.
4. Look through a website like https://www.javelinart.com/FM_Synthesis_of_Real_Instruments.pdf to see specifics about the instrument. For example, a trumpet sounds brighter when it plays louder notes. idx3 makes the trumpet sound brighter so have this be modified when amplitude changes. I used a factor of 10 times amplitude for the trumpet to accomplish this. Often, there will be more information regarding the use of carMul, modMul, and pan but for a lot of instruments using the preexisting settings works as expected.

Some examples of instruments values:

FM freq amplitude attackTime releaseTime sustain idx1 idx2 idx3 carMul modMul pan

Alto Saxophone: FM 256.869 0.2 0.1 0.1 0.75 1.5 1 2.5 1 1.0007 0

Trumpet (demo below): FM 256.869 0.5 0.1 0.1 0.75 5 7 5 1 1.0007 0 


https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/b973591d-c4ae-4da4-afb0-f61e597b7948


# Final Project:
## Imperial March by John Williams
Alto Saxophone, Clarinet, Tuba, Bass Drum, Snare Drum with FM synthesis
1083 Midi Notes

For this project, I wanted to arrange a piece but the Synth files looked awful for writing music in a clean fashion when multiple instruments are being used. I developed a python script to write music in a simpler manner. Then, the melody was developed. After you run the python script you can copy and paste it into a Synth file and run. Then run using the FM Synthesis cpp file.

## Music Only Video

https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/feb3585c-1ac8-4be4-af1d-cef0c5d200e4

## Final Project Demo

https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/c11fd614-c0ee-49a3-9796-229f5967f720

