# Piano-with-8051-and-IC-555
Small project with assembly and music skill

• First we will build the circuit using IC 555 to determine the frequency of music notes that we use for our songs
(In this project I use only White notes from C3 to G4).

![image](https://user-images.githubusercontent.com/104365389/165517091-e6d82bc6-c4d4-473b-b8cb-c6b6077793b9.png)

IC 555 calculate the output voltage frequency

![image](https://user-images.githubusercontent.com/104365389/165499814-e5025105-e0da-4c92-a9a5-f60d3089d9cc.png)

The 555 timer shown above is configured as an astable circuit. This means that the output voltage is a periodic pulse that alternates between the VCC value and 0 volts.
![image](https://user-images.githubusercontent.com/104365389/165500153-e20450ad-cdf5-4c60-9580-70bb7132f939.png)

The frequency is the number of pulses per second. The formula to calculate the frequency of the output voltage is:

![image](https://user-images.githubusercontent.com/104365389/165500538-47bf0ebb-959f-43bc-b3c7-8c25be1451c9.png)

So in our circuit to calculate the frequency, the formula will be:

![image](https://user-images.githubusercontent.com/104365389/165518632-9a6366fc-6075-4470-8cbb-3df3b7145e49.png)

with x is the music note.

Now we will calculate the value of resistor Rx base on the frequency of music notes, following this table below:
![image](https://user-images.githubusercontent.com/104365389/165517789-95b587b1-16bd-40c9-8705-3ab9f558e9c3.png)

Example: calculate the Resistor of C3, so x = C3

![image](https://user-images.githubusercontent.com/104365389/165518513-ffc96137-e7d2-4242-af8b-c8dec84a9e9e.png)

• Second is the full circuit with microcontroller 8051 and GPIOs connection.

![image](https://user-images.githubusercontent.com/104365389/165520619-815d0f3a-c2a8-4286-b953-ad21745448ac.png)

I use tristate gate to not turn on two music notes in the same time.

• Third I wil use 8051 code to test 1 music note (C3).

![image](https://user-images.githubusercontent.com/104365389/165528687-09bb16a1-3c8a-4b8a-b849-f9f747c7352a.png)

First I enable the tristate gate, then turn on the buzzer for 1 second. After that I turn off the buzzer and wait for 1 second to disable the tristate gate and wait for another music note.

• Finally I will demo the project with Cannon in C songs through GoogleDrive link:

https://drive.google.com/file/d/1sgVnA7uTdVQ8pQVtDn6njXhJWmUeFd5d/view?usp=sharing
