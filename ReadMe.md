## EVALUATOR PLEASE READ 
I do not know the experience level of the person evalauting this lab and 
I am making the following assumptions 

1. The person evaluating the lab has some familiarity with terrafrom. 
2. The steps below will be automated and inlcuded as part of the terraform script 
3. Plurasight has a preffered authentication method that allows the user to login to the virtual machine
4. 


### Prerequisites for the environment setup 

Run the terraform script to create the test vm in the azure cloud. 

Extract the private key and save localy by executing the following command 

`.\terraform output -raw tls_private_key > id_rsa`

Extract the public IP address and note the address 

`.\terraform output public_ip_address <public IP Address>`

SSH into the virtual machine

`ssh -i id_rsa azureuser@<public_ip_address>`

Copy the pcap file to the virtual machine to the /tmp directory

`scp -i id_rsa teardrop.cap azureuser@74.235.17.169:/tmp`

The environment is ready for the lab. 
