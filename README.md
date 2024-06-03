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

Trumpet [INSERT VIDEO]: FM 256.869 0.5 0.1 0.1 0.75 5 7 5 1 1.0007 0 


https://github.com/allolib-s24/notes-nagpalishaan/assets/86748731/b973591d-c4ae-4da4-afb0-f61e597b7948


Alto Saxophone: FM 256.869 0.2 0.1 0.1 0.75 1.5 1 2.5 1 1.0007 0

# Final Project:
## Imperial March by John Williams
Alto Saxophone, Clarinet, Tuba, Bass Drum, Snare Drum with FM synthesis
1083 Midi Notes

For this project, I wanted to arrange a piece but the Synth files looked awful for writing music in a clean fashion when multiple instruments are being used. I developed a python script to write music in a simpler manner. [INSERT PICTURE OF IMPLEMENTATION] [INSERT PICTURE OF USE]. Then, the melody was developed. After you run the python script you can copy and paste it into a Synth file and run. Then run using the FM Synthesis cpp file.