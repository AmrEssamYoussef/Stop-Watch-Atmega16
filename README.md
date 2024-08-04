# Stop-Watch-Atmega32
Overview
This project involves designing a Stop Watch system using an ATmega32 microcontroller with a frequency of 1MHz. The system uses six common anode 7-segment displays controlled via multiplexing.

System Requirements
Microcontroller: ATmega32 running at 1 MHz.
Timer Configuration: Configure Timer1 in CTC mode to count the Stop Watch time.
Display: Use six Common Anode 7-segments with multiplexing.
Multiplexing: Use one 7447 decoder for all 7-segments and control the enable/disable for each 7-segment using an NPN BJT transistor connected to an MCU pin.
Connections:
Connect the 7447 decoder's 4-pins to the first 4-pins in PORTC.
Use the first 6-pins in PORTA as enable/disable pins for the six 7-segments.
Stop Watch Functionality:
Start counting when the power is connected to the MCU.
Reset: Configure External Interrupt INT0 (falling edge) with a push button using an internal pull-up resistor.
Pause: Configure External Interrupt INT1 (rising edge) with a push button using an external pull-down resistor.
Resume: Configure External Interrupt INT2 (falling edge) with a push button using an internal pull-up resistor.
Multiplexing Technique
Multiplexing Method: Only one 7-segment display is driven by the Microcontroller at a time while the rest are OFF. This rapid switching creates the appearance of a normal display due to the persistence of vision.

Getting Started
Clone the Repository:
git clone https://github.com/AmrEssamYoussef/Stop-Watch-Atmega32.git
Build the Project: Follow your IDE/compiler instructions to build and upload the code to the ATmega16 microcontroller.
Connect the Hardware: Ensure all components are connected as per the specifications.
Run the System: Power up the system and observe the stop watch functionality based on the described interrupts.

Video Demonstration

For a visual demonstration of the project, check this video https://drive.google.com/file/d/1MF9Nh-c2yVZIvvTpDbAqgxe8VOLd3GB0/view?usp=sharing.
