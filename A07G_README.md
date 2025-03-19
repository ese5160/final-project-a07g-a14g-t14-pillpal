# a07g-exploring-the-CLI

* Team Number: 14
* Team Name: PillPal
* Team Members: Suhaila Shankar and Urvi Haval
* GitHub Repository URL: https://github.com/ese5160/final-project-a07g-a14g-t14-pillpal.git
* Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc)

### Software Architecture

### Understanding Starter Code

#### 1. What does “InitializeSerialConsole()” do? In said function, what is “cbufRx” and “cbufTx”? What type of data structure is it? 

The "InitializeSerialConsole()"  initializes the UART and registers callbacks. "cbufRx" initializes the circular buffer for RX and "cbufTx" initializes the circular buffer for TX. It is a circular buffer data structure that is commonly used to implement an array and manage metadata such as a head, tail, and capacity. 

#### 2. How are “cbufRx” and “cbufTx” initialized? Where is the library that defines them (please list the *C file they come from). 
"cbufRx" and "cbufTx" is initialized usinf the circular_buf_init function. It is initialized in the circular_buffer.c file where the buffer and size are initialized. 

#### 3. Where are the character arrays where the RX and TX characters are being stored at the end? Please mention their name and size.
Tip: Please note cBufRx and cBufTx are structures.
Name is rxCharacterBuffer and txCharacterBuffer for storing received characters and characters to be sent. The size is 512 bytes. 

#### 5. Where are the interrupts for UART character received and UART character sent defined? 
The usart_read_callback function handles the UART receive interrupt and the usart_write_callback is used to handle the UART transmit interrupt. 

#### 6. What are the callback functions that are called when: 
A character is received? (RX) 
A character has been sent? (TX) 

#### 7. Explain what is being done on each of these two callbacks and how they relate to the cbufRx and cbufTx buffers. 

#### 8. Draw a diagram that explains the program flow for UART receive – starting with the user typing a character and ending with how that characters ends up in the circular buffer “cbufRx”. Please make reference to specific functions in the starter code. 


#### 9. Draw a diagram that explains the program flow for the UART transmission – starting from a string added by the program to the circular buffer “cbufTx” and ending on characters being shown on the screen of a PC (On Teraterm, for example). Please make reference to specific functions in the starter code. 

#### 10. What is done on the function “startStasks()” in main.c? How many threads are started?
