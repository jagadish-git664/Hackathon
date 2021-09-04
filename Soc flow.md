


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


1) We have difference IPs PROM , DROM , DRAM and timer which measure the performance . 
2) 
