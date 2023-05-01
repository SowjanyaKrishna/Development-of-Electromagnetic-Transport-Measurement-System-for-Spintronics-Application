# Development-of-Electromagnetic-Transport-Measurement-System-for-Spintronics-Application
Bachelor Thesis

The development in the field of electronics has grown vast in the past few decades.
Conventional electronic devices rely on the transport of electric charge carriers-electrons-in a
semiconductor such as silicon device. As the Moore law gradually loses its effect, conventional
charge-based electronics is coming to an end as we have reached to a nanoscale size of
components and further reduction in size would affect the functioning of the device due to
quantum effects. Today engineers and physicists are trying to exploit the spin of an electron than
charge which gives rise to an new emerging and promising field called Spintronics which uses
the spins of electrons as information carriers and possesses potential advantages of speeding up
data processing, high circuit integration density, and low energy consumption. The key property
in Spintronics is the measurement of magnetoresistance i.e. the electrical resistance under the
influence of magnetic field and this magnetoresistance can be measured using a transport
measurement system which is the goal of our project. We have designed and fabricated a
electromagnetic transport measurement system that is compact, automated and low cost. A thin
film of Fe 3 0 4 is deposited onto the silicon substrate by using Pulsed laser Deposition(PLD)
process for injection of spin onto a semiconductor. The fabricated heterostructure is placed on
the sample holder which is automated by a robotic arm that is powered up using Arduino for the
rotation of in plane, out-off plane and anisotropic measurements. By two probe method, voltage
is supplied to the sample and the current value is measured and thereby magnetoresistance is
calculated from the slope of I-V characteristics which gives us the behaviour of the sample for
spintronics application. Multiple samples can be loaded onto this system and magnetoresistance
can be measured which will enable a fundamental understanding of new effects emerging in the
field of spintronics.

# OBJECTIVE
The objective of this project is development and implementation of an electromagnetic transport
measurement system for spintronics application which will enable a fundamental understanding
of new effects emerging in the field of spintronics. The understanding, quantification of these
effects will underpin Research & Development and future applications in metrology,
Information and Communication Technologies, and other fields. It will also take the first steps
towards future standardisation of spintronic measurements, materials, and devices by the
development of a new measurement infrastructure and a best practice guide for spintronics
material measurements.The following phases need to be completed to meet the objective,

	● To design an automated and compact electromagnetic transport measurement system
	● To create spin injection in the sample
	● To achieve the transport of the spin-polarized electrons maintaining their spin orientation.
	● To measure the magnetoresistance of the given sample
	● Simulate design using arduino microcontroller.
	● Implement the simulated design along with hardware and software specifications.

# SCHEMATIC DIAGRAM OF TRANSPORT MEASUREMENT SYSTEM
The below fig. shows a schematic view of the electromagnetic transport measurement system.
The instruments used to fabricate the system are: a electromagnet to generate magnetic field, a
electromagnetic power supply to power up the electromagnet, a gauss meter to measure the
magnetic field produced by the electromagnet, a robotic arm which holds the sample and is
programmed to rotate in-plane, out-off plane and isotropic, a heterojunction sample
Fe304/Sio2/Si to which a voltage supply is connected and simultaneously current produced is
measured on an ammeter.

![image](https://user-images.githubusercontent.com/128833366/235427433-9215c244-9cd1-4b5b-bb28-7db504be0d4a.png)

1.Dual regulated DC power supply (0-30V), 2. Gauss meter, 3.Electromagnetic power supply, 4. Ammeter, 
5.Robotic arm, 6. Sample, 7. Electromagnet

# AUTOMATION OF ROBOTIC ARM
The automation of the Robotic Arm is done with the help of Arduino UNO Microcontroller.
Arduino UNO is an open-source microcontroller board based on the Microchip ATmega328P
microcontroller and developed by Arduino.cc.The ATmega328 on the Arduino Uno comes pre-programmed with a bootloader that allows uploading new code to it without the use of an external hardware programmer. It communicates
using the original STK500 protocol.The Uno also differs from all preceding boards in that it
does not use the FTDI USB-to-serial driver chip. Instead, it uses the Atmega16U2
(Atmega8U2 up to version R2) programmed as a USB-to-serial converter.
The first phase is the software development which is done using Arduino Integrated
Development Environment(IDE) Programming software. For software programming, an
assembly language was used to construct the command to get the desired results. Assembly
language can be used to specify the exact instructions and one can control the time and
space(memory) used for each step of the program.Three servo motors(SERVO1, SERVO 2 and
SERVO 3) of the robotic arm are interfaced with the Arduino board which are programmed to
achieve the rotation of the robotic arm as well as the sample holder in desired direction to take
the measurements. The 3 servo motors used at each axis is connected to the arduino through the
input pins. The rotation of the servo motor is controlled by providing it with a pulse width
modulated signal.
Eg: (pos=0; pos<180; pos+=10)
myservo.write(pos); \\pos provides the position it needs to move
Here the servo motor moves from left to right, ranging from 0° to 180°. In the same manner
each servo motor can be programmed to rotate at a certain angle to obtain a particular position
of the sample between the magnets. Next step is to upload the programming code into
ATmega328 and all the variables to be used is written down on it. The programming interprets
and sends to PIC. The input and output is declared. After this process has complete, the program
will analyze and run it on Arduino Uno to identify and detect if there is any failure in
programming before loading to ATmega328. Next step is to upload it via universal serial bus
(USB). The USB-to-serial adapter chip or cable is implemented through USB interface. After
sending the command via USB to ATmega328, the programming will be analyzed again to the
electronic component to work.

![Image](https://user-images.githubusercontent.com/128833366/235426760-800ed698-fa6f-46d7-9824-65cd78c19edb.PNG)

<img width="1154" alt="image" src="https://user-images.githubusercontent.com/128833366/235426850-44adf1f8-0c86-45b4-ac0c-3c08491cad0f.png">
