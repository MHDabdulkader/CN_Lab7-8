# CN_Lab7-8
Router static routing 192.168.102.0/24 4 subneting
Topology design with ip address and submask
![CNN](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/87b2d5cc-719d-4c3f-acf7-8cf7261e6679)


Assign PC ip address

PC1> ip 192.168.102.2     255.255.255.192     192.168.102.1
        (PC ip address)    (Submask)          (gateway Router R1 ip address)

![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/471dbe69-7b72-4733-8810-ce4b258fd197)

Save in pc code:

PC1> save
![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/172a3b67-ec43-435a-a4aa-c2a6b0640a29)

Check ip address: 
![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/5eae4cb2-0f67-40e5-b57e-d5785c9a3b7f)


Assign Router paths address 
IN code
f0/0 switch to router : 
      IP address 192.168.102.1 submask 255.255.255.192
s1/0 router to router (For R1 router connect to R2):
      IP address 10.0.0.1 submask 255.255.255.252
s1/1 router to router (For R1 router connect to R4) :
      IP address 10.0.0.2 submask 255.255.255.252

Router address assign code: 
Becareful to 
1. assign submask different interface fastEthernet and Serial.
2. no shut after the ip address assign. if you forget just Click here
3. use "write" to save code
conf t
  int f0/0
  ip address 192.168.102.1 255.255.255.192
  no shut
  exit
  ![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/99c8da29-bde1-4970-9032-1eec73526c1b)

  int s1/0
  ip address 10.0.0.1 255.255.255.252
  no shut
  exit
  ![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/3bab2f0a-08ec-40f4-acaa-e2e470989e13)

  int s1/1
  ip address 40.0.0.2 255.255.255.252
  no shut
  exit
  ![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/1a8c8570-eb9f-4200-8dea-d048f208a413)


exit
write
![image](https://github.com/MHDabdulkader/CN_Lab7-8/assets/81324227/0b72bb45-7c84-4cda-bf68-1f0d5b53a698)
press Enter to confirm







