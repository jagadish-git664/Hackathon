# Hackathon

![image](https://user-images.githubusercontent.com/73343230/132094854-6d04fde6-1086-451a-a5b4-ee5acaa77679.png)


Key takeaway
![image](https://user-images.githubusercontent.com/73343230/132094895-b0ef70e1-3590-49a9-af71-cf369fe895a0.png)
Initally we have SOC idea. 
1) We need to implement this in meta RTL for this using gui .
2) we need to difine the SOC configuration in the gui . 
3) Generation Framwork :With this we can generate the entire hardware along with the compiler configuration . With this we can have
the hard ware and firmware part.
4)Application code :User have to define the applicaiton code . Compile this on configured compiler . 


Image processing:Edge detection 
![image](https://user-images.githubusercontent.com/73343230/132095390-91305a4d-a0c9-4fc4-968c-bd0b99c93ac8.png)

Problem Statement: Edge detection of an image.
![image](https://user-images.githubusercontent.com/73343230/132095417-5d92e5e8-612a-4320-bfd2-fc18246bcd15.png)

1) We need convolution for edge detection . The image is in grey scale which is 8 bit (0-255) 
2) Based on the type of matric chosen we get different edge detection . 

Challenge 
![image](https://user-images.githubusercontent.com/73343230/132095520-899a6628-e52f-4d88-9107-b7dd00bc514e.png)
1) We need to device  egde detecting algorithm usign above constraints 

Scoring Criteria
![image](https://user-images.githubusercontent.com/73343230/132095613-b8b1d5d0-47b4-4fce-ae24-44e756f9465d.png)

Execution Flow
![image](https://user-images.githubusercontent.com/73343230/132095693-d7340e6e-8478-4e00-882f-a01a77d4c387.png)

![image](https://user-images.githubusercontent.com/73343230/132095813-71a6bac0-133e-471a-81da-2bf8ffd265be.png)
1) Bus infrastructure to connect with different IP . Since this is a SOC we can have CPU , peripherals ,timer , memory etc. 
2) Configuration we have to provide. 

What is SOC :
![image](https://user-images.githubusercontent.com/73343230/132095930-7c7783bc-8738-4f1e-a932-5db428b9e17b.png)


![image](https://user-images.githubusercontent.com/73343230/132095997-4cf03251-2c8b-45af-908e-40b783fef9fd.png)

1) Interface in orange is master interface (controller) and slave interface. 
2) CPU connects with different peripherals. For this we need bus matric.

SOC design life cycle :
![image](https://user-images.githubusercontent.com/73343230/132096135-2ffb9958-212c-4586-a634-1ce3b7c7a341.png)
1) Requirements and spec: 2 req , CPU is riscv and application is edge detecgion . 


Requirementes and system specificaiton :
![image](https://user-images.githubusercontent.com/73343230/132096211-3b7be8f9-b8e3-48c2-ad45-9ac9928d59b3.png)
Funcional req :  We want this edge deteciton as func req. 

Architecture analysis and prototype 
![image](https://user-images.githubusercontent.com/73343230/132096266-adddbf32-d31e-4c08-af3f-73dc12022f72.png)

RTL 
![image](https://user-images.githubusercontent.com/73343230/132096352-0ef3967a-0fec-4732-9e22-bc0a1acaa5a7.png)
1) RTL can be developed by reusing the hardware or buy 3rd party vendor IP . 

![image](https://user-images.githubusercontent.com/73343230/132096432-896bd533-816a-4d3a-8932-3b8af980239c.png)

If we have to write RTL we need to write  RTL from scratch 

![image](https://user-images.githubusercontent.com/73343230/132096501-23a9b0d5-9963-4154-9517-c8d4585f100a.png)

Logic synthesis:
![image](https://user-images.githubusercontent.com/73343230/132096516-7732a9bb-f6f5-4ce1-b64a-69c335e20a54.png)

![image](https://user-images.githubusercontent.com/73343230/132096566-b8eda0cf-4033-4336-b69b-6a4873527e20.png)

META RTL :

Soc design using PBF (product build flow) {Metal RTL}
![image](https://user-images.githubusercontent.com/73343230/132096586-3c392342-1ae0-41c6-8b9b-15eea788c5d7.png)

1) We have top level, sub system  . IP interfaces , when one IP wants to  talk to other IPs.Inside IP we have SFR . This are coverted by PBF.

What else is missing 
![image](https://user-images.githubusercontent.com/73343230/132096775-e0abae3c-4a77-4069-9105-5fe63a0536a1.png)
We have IP structure , registers , connections ,interfaces .

What about behaviour code ?

![image](https://user-images.githubusercontent.com/73343230/132096744-ff5688c1-27a0-4975-8274-14379e1abe3c.png)


Motivation behind META RTL 
![image](https://user-images.githubusercontent.com/73343230/132096814-7cc6b272-98b8-4b32-bba8-ce997e4cee23.png)

![image](https://user-images.githubusercontent.com/73343230/132098035-e040cb18-7b2c-47d1-aeb8-4bb9e25ed809.png)
Need to provide the formal specifiatin to metal rtl frame work which will generate the behaviour code , this can 
be provided to FPGA for bit stream  . 

![image](https://user-images.githubusercontent.com/73343230/132098092-32a83b17-7726-4b4f-9367-7a03a173aeb1.png)
Libraries to be used for Hackathon  . 
We need to provide the configuration . 

META RTL SOC FLOW AND DEMO :

![image](https://user-images.githubusercontent.com/73343230/132098222-a666a2c6-157c-4bc8-bf5d-b428ae3dd218.png)
1) Basic idea of Metal rtl to convert soc idea to implementation flow in few hours. Using the tool set we can 
use the existing Ip and configure to generate RTL and firmware as well . 
2) Write application code and compile with necessary compiler extension . 
3) We can use this in fpga for now using vidado for synthesis and simulation . 




