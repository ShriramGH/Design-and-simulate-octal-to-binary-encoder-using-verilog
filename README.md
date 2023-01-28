# Design-and-simulate-octal-to-binary-encoder-using-verilog

### AIM: To implement octal to binary Encoder using verilog and validate its output

### HARDWARE REQUIRED: – PC, Cyclone II , USB flasher

### SOFTWARE REQUIRED: Quartus prime

### THEORY
## Encoder
Binary code of N digits can be used to store 2N distinct elements of coded information. This is what encoders and decoders are used for. Encoders convert 2N lines of input into a code of N bits and Decoders decode the N bits into 2N lines.

Encoders – An encoder is a combinational circuit that converts binary information in the form of a 2N input lines into N output lines, which represent N bit code for the input. For simple encoders, it is assumed that only one input line is active at a time.
As an example, let’s consider Octal to Binary encoder. As shown in the following figure, an octal-to-binary encoder takes 8 input lines and generates 3 output lines.


## Logic Diagram:

![encoderld](https://user-images.githubusercontent.com/117991122/215278894-0e843d21-6a1b-490e-b585-bc32de5e013d.png)

## Logical Expression:
An octal to binary encoder can be represented using a logical expression. Each octal digit (0-7) is mapped to a 3-bit binary number. The logical expression for the encoder can be represented using a truth table, with each octal digit as one input and the corresponding 3-bit binary output.

For example, if the input is the octal digit 3, the binary output would be 011. Therefore, the logical expression for the 3 input would be: output = (input = 3) ? 011 : (other inputs)

This can be extended to include all 8 digits by using multiple expressions connected by logical operators such as AND, OR, and NOT.

## Block Diagram:

![encoder](https://user-images.githubusercontent.com/117991122/215278640-3c911103-d434-4baa-90c2-e98991303e6c.png)

### PROGRAM 


Program for Endocers and Decoders  and verify its truth table in quartus using Verilog programming.

Developed by:  Shriram S

RegisterNumber:  22008494

#### Encoder

```
module EX8(a,b,c,d0,d1,d2,d3,d4,d5,d6,d7);
output a,b,c;
input d0,d1,d2,d3,d4,d5,d6,d7;
or(a,d4,d5,d6,d7);
or(b,d2,d3,d6,d7);
or(c,d1,d3,d5,d7);
endmodule
```

## RTL LOGIC  


#### Encoder

![image](https://user-images.githubusercontent.com/117991122/215281774-baa5ace5-d51a-4147-b58e-f6678d4e7643.png)

## Timing Diagram:

![image](https://user-images.githubusercontent.com/117991122/215281805-ae0134dd-b8a2-4066-a511-1f087e5c1675.png)

## Truth Table:

#### Encoder
![image](https://user-images.githubusercontent.com/117991122/215281844-d2944d41-1331-4a4e-a289-005b897a07cd.png)

## RESULTS
Thus the program to implement encoder using verilog is verified.

 
