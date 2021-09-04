


SOC FLOW:Introduction 


![image](https://user-images.githubusercontent.com/73343230/132099895-03e65384-1971-49fe-ad7a-b91c8f32c199.png)

1) Using metagen gui one can create specificatin called metagen mot. Mot are files which contain specification .

2) To build and applicaiton first we need to provide the IP for which rtl will be generated and SOC MOT ( which all ip used and its connection ) and IP MOT . 
After this firmware will be automatically generated. 

3) For the firmware we use firmware MOT which enables the behaviour of firmware generation . 

4) Once the firmware and RTL are generated we can write application code and compile with necessary compiler . 
5) During complilaiton phase we use compiler MOT as well . 

Referece block diagram for SOC flow.

![image](https://user-images.githubusercontent.com/73343230/132100206-b34fe919-ef7c-43cb-a8ba-c5970ccb82b9.png)


1) We have difference IPs PROM , DROM , DRAM  and timer which measure the performance . 
2) CPU is the riscv5 . IP connected to instruction and data bus via slave interface . CPU throught master interface. 


SOC flow HW.
![image](https://user-images.githubusercontent.com/73343230/132101648-3e186cc5-285b-422f-a982-d6ed42db0420.png)

First layer :
Designer wiht SOC arch in mind , fills the SOC and IP Mot and pass to the SOC flow (diagram) . The SOC flow generates 
the meta RTL . 
Interface MOT which used to connecte with different IP will be automatically genrated with the soc flow. 

Second layer :
![image](https://user-images.githubusercontent.com/73343230/132101783-cadd6a2c-c33f-40a3-9fdd-615ee94cd440.png)

Once the RTL is generated  . The firmware corresponding to it is generated using Metafirm . 


Third layer :
![image](https://user-images.githubusercontent.com/73343230/132101824-c9d271bc-db13-47ff-be97-ea2476e10c78.png)

One the RTL and frimware available . Need to generate the appliaction code for the firmware

The applicaiton code is written in the C language. 
![image](https://user-images.githubusercontent.com/73343230/132101953-dd0e5f1c-a12e-41b3-94a5-61f44ff28f63.png)

The application code has the timer driver . Once the applicaiton code is ready . Metacomplier can be used to compile the code. 

Here we use a meta lib called a meta compiler . 

![image](https://user-images.githubusercontent.com/73343230/132101975-dee270fe-7a38-46ec-a717-7bab3792c246.png)

Scoring :

![image](https://user-images.githubusercontent.com/73343230/132102059-fa4d9057-fe7c-4575-b305-da3fad3e2760.png)

First two dependant on applicaiton code and tune the firmware .

Second two dependant on the harwared used.

We have many different option available to be used in hardware and software 

