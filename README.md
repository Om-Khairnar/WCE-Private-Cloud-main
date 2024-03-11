## Private Cloud for WCE

## Implementation and Results
  For creating a cluster we need 2 computers in the same network, let's say one a Controller Node and other a Compute Node. Configure them with a static IP as restarts can initiate a DHCP and IP address might change. Also make sure these machines have VT support if they are virtual machines on some hypervisor like VMware ESXi.

Following steps will provide a path to configure these nodes from scratch and spin up an instance from Private Cloud Console and associate Proxy ports for external access. 

**Setting up Controller Node:**
  **1. Install Microstack from snap.**
    ![1](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/c57f32ad-ecb0-419a-be40-68094eab1508)
      
  **2.Initiate Microstack as control node and configure cinder to use LVM backend. Also add ssl certificate to glance config file and restart the microstack.cinder.uwsgi, microstack.cinder.scheduler and microstack.cinder.volume services.**
    ![2](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/a74ad9d1-8f13-4603-a0ba-41f57d9ca2a0)
     
  **3.Command microstack to add another compute node to the cluster. It gives us the connection string that we will use while setting up microstack on the compute node.**
    ![3](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/001cf49a-1011-440a-8c6e-0c3a715c6139)

## Private Cloud Console :
   **1. Login using Moodle Credentials.**
   
   ![1](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/d11ffb8e-5a75-4e53-af47-68c80131bf7e)

   **2. Following is the interface for viewing, configuring and creating instances.**
   
   ![2](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/f55cc197-7e3b-46f0-b66f-6aa622625f39)

   **3. Create Instance by naming it and choosing image and RAM size.**

   ![3](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/9a54820a-a1c6-4f6f-9e69-087e9fd2c62b)

   **4. View instances that is created**
     
  ![4](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/027c217e-2d55-469a-9c34-1f277e387e92)
     
   **5. Associate one or more public ports. Here maximum 3 public associations are allowed.**
   
   ![5 1](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/2d667dcd-3c2c-445a-804d-2897c94609d4)
      
  ![5 2](https://github.com/Om-Khairnar/WCE-Private-Cloud-main/assets/143726540/2b9d69c1-3567-43a5-b786-ab85c039e9a0)

## References  
  [1] Sarvesh Kumar, Omkara Murthy: Cloud Computing for Universities: A Prototype
      Suggestion and use of Cloud Computing in Academic Institutions, International Journal
      of Computer Applications (0975 – 8887) Volume 70– No, May 2013.
    
  [2] Guoxia Zou: The Design Of Private Cloud Platform For Colleges And Universities
      Education Resources Based On Openstack, Dec 2015.
      
  [3] Nikhil Wagh, Vikul Pawar and Kailash Kharat, Implementation of Stable Private Cloud
      using OpenStack with Virtual Machine Results, International Journal of Computer
      Engineering and Technology, 10(2), 2019, pp. 258-269.
  
  [4] SudhaDevi, D. & Yamuna Devi, Loganathan & Thilagavathy, K. & P, Aruna & Priya,
      Navya & Vasantha, s. (2013). Private Cloud in Educational Institutions: An
      Implementation using UEC. International Journal of Computer Applications. 78. 8-12.
      10.5120/13451-1059.
