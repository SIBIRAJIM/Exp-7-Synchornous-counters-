### Name:SIBIRAJI M 
### Register number: 212223050048

## Experiment-06 Synchornous counters up counter

### AIM: To implement 4 bit up and down counters and validate  functionality.

### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



### Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors: 
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.



### PROGRAM 
Program for flipflops  and verify its truth table in quartus using Verilog programming.

## UP COUNTER 
![Screenshot 2023-12-30 101427](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/b87b3fed-7a90-4b1c-9f83-59c5be738d55)

## DOWN COUNTER 
![Screenshot 2023-12-30 101001](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/e74b924b-598c-4b95-ba5f-9cad81f775e1)

### RTL REALIZATION

## UP COUNTER 
![Screenshot 2023-12-21 170942](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/535fdb71-86cb-496d-8ee9-6e2f18933e81)

## DOWN COUNTER 
![Screenshot 2023-12-21 180236](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/c5536993-4bef-40ea-8ce9-21bb7d8664c1)

### TIMING DIGRAMS 

## UP COUNTER  
![Screenshot 2023-12-21 170827](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/5a05d875-3d36-4173-ab9a-dc83fdedf0ba)

## DOWN COUNTER 
![Screenshot 2023-12-21 181221](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/d7a763f3-db25-424c-811c-464f31ca2a33)

### TRUTH TABLE 

## UP COUNTER
![Screenshot 2023-12-30 101128](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/15773950-67d2-42ff-8628-9ae8619a91e7)

## DOWN COUNTER 
![Screenshot 2023-12-30 101139](https://github.com/SIBIRAJIM/Exp-7-Synchornous-counters-/assets/154588445/d488e0c3-7083-4616-9e49-84f2cc97c619)

### RESULTS 
By this we have verified the truth table of 4-bit up-counter using verilog.
