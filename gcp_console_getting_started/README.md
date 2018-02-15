# Getting started once you've created a free GCP account



 ## The First thing you see upon logging into the console of you GCP account is the Dashboard:




<kbd>
  <img src="figs/0_after_creating_instance.png">
</kbd>




# Step 1: Select Compute Engine >> VM instances


<kbd>
  <img src="figs/1_vm_instance.png">
</kbd>



# Step 2: Select Create under VM Instances

<kbd>
  <img src="figs/2_create_instance.png">
</kbd>

# Step 3: Customize your VM

 ## Name your instance, pick region us-west1-b as they have GPU's and click customize.


<kbd>
  <img src="figs/3_name_customize.png">
</kbd>!


# Step 4: Select No. of Cores, Ram, GPU

 ## Click GPU's


<kbd>
  <img src="figs/4_gpu.png">
</kbd>

 ## Select 1 NVIDIA Tesla K80


<kbd>
  <img src="figs/4_1_gpu.png">
</kbd>


# Step 5: Change Operating System & Storage

 ## Select Ubuntu 14.04 and 100GB Standard Persistant Disk

<kbd>
  <img src="figs/6_os_100_gb.png">
</kbd>


# Step 6: Firewall & SSH KEY

##  [Generate](https://github.com/s3p02/create_ssh_mac_and_linux) an ssh key on your system, copy it to the highlighted area below.
 
 ## Under Firewall, check for HTTP & HTTPS traffic

<kbd>
  <img src="figs/7_firewall_ssh_key.png">
</kbd>

 # Step 7: Create Instance

 ## Enter the SSH Key [Generated](https://github.com/s3p02/create_ssh_mac_and_linux/blob/master/README.md), and click create to create an instance

You are most likely going to encounter an error after clicking create. This is primarily because, GPU's are not allotted directly with a free account. A Quota request is required for GPU.

# Step 8: Error Creating Instance 

<kbd>
  <img src="figs/8_error_request_for_quota.png">
</kbd>

# Step 9: Request for increase in Quota

<kbd>
  <img src="figs/9_Request_Increase.png">
</kbd>

## Upon Selecting 'REQUEST INCREASE', you are brought to the Quota's page, Click on 'Upgrade account'.

<kbd>
  <img src="figs/10_quotas.png">
</kbd>

## Select 'Upgrade'.

<kbd>
  <img src="figs/11_upgrade.png">
</kbd>

## Under 'All regions' drop down option, select 'None'.

<kbd>
  <img src="figs/12_region_none.png">
</kbd>


## Scroll down to select 'us-west1'.

<kbd>
  <img src="figs/13_west_1.png">
</kbd>


## Now, Scroll down to the bottom of the Quotas page and select 'Google Compute Engine API - NVIDIA K80 GPUs' and then click on 'EDIT QUOTAS'

<kbd>
  <img src="figs/14_k80_edit_quota.png">
</kbd>

## Upon Selecting 'EDIT QUOTAS', Fill in your Name, Email and Phone number and Click 'Next'

<kbd>
  <img src="figs/15_request.png">
</kbd>

## For the Request to be Approved, 'Change to 1' and Justify your request with a reason and click 'Next'

<kbd>
  <img src="figs/16_request_1_justify.png">
</kbd>

## Click Submit Request

<kbd>
  <img src="figs/17_submit_request.png">
</kbd>

## Once your request is complete, you can close the pop-up.

<kbd>
  <img src="figs/18_complete.png">
</kbd>

## You will get an email from Google Cloud Support, with your case number.

<kbd>
  <img src="figs/19_Response_for_quota_increase.png">
</kbd>

## Usually the turn around time is fast, I got mine in one minute.

<kbd>
  <img src="figs/20_turn_around_time.png">
</kbd>

# Step 10: Re-Launch your VM Instance

## You can re-launch your instance from the notifications icon at the right hand corner of the console, by clicking 'RETRY'

<kbd>
  <img src="figs/21_retry_launching_instance.png">
</kbd>

## Once Your Instance Launches successfully, you will see a green check mark besides your instance's name, you will get an External IP for your instance.

<kbd>
  <img src="figs/22_instance_complete.png">
</kbd>

# Start/Stop Instance

## You will be charged, immediately once you run out of free credit. It's highly recommended that one stop's the VM when it's not being utilized, as the charge per hour is ~$1. Approx. you can get less than 300 hours with the free credit to play around with a GPU VM on GCP.

<kbd>
  <img src="figs/23_stop_instance.png">
</kbd>

[Back to Main](https://github.com/s3p02/jupyter_gcp_nvidia-docker_digits)
