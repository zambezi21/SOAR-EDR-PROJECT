# SOAR-EDR-PROJECT

## Objective

The SOAR EDR project aimed to establish a controlled environment for automating and responding to cybersecurity incidents. The primary focus was to integrate Endpoint Detection and Response (EDR) tools with Security Orchestration, Automation, and Response (SOAR) platforms, by using LimaCharlie and Tines, enabling automated workflows to detect, analyze, and mitigate threats in real-time. This hands-on experience was designed to deepen understanding of automated incident response, threat hunting, and advanced attack detection strategies.

### Skills Learned

### Tools Used
- Windows Server
- Tines
- LimaCharlie
- Slack

## Steps
- The first step that was taken was to create a diagram of the project.

  ![Diagram](https://github.com/user-attachments/assets/3b7aca6d-597b-4c3c-bb03-4e44ec90f4f0)
   *Ref 1: Network Diagram*

- The second step was to install and setup LimaCharlie. As well as confim events. Once there has been a LimaCharlie account created and installed on the Windows VM, on the host one will be able to click on the sensor of the VM and find infomation about the server. As well as find and view much more event info from the VM.

  ![LimaCharlie 1](https://github.com/user-attachments/assets/1f026962-2d8d-41bc-b180-eb4e0174f4c6)
  *Ref 2: Creating a LimaCharlie account base line from host machine*

  ![LimaCharlie 2](https://github.com/user-attachments/assets/06c0e98d-a20f-4b78-a2e9-168e9c0e7bc4)
  *Ref 3: Install LimaCharle onto the Windows VM*

  ![LimaCharlie 3](https://github.com/user-attachments/assets/7f94fdf6-ccf4-4368-83fa-972a28293dbf)
 *Ref 4: Sensor info from the VM to LimaCharlie from the host*

- The thrid step was to generate telemetry using Lazagne as well as create a detection and response rule. Through the server, download Lazagne and then go to Tines and and view the Lazagne event info to help with creating a detection rule. Then using the info from the Lazagne event create both a detection and response
  
  ![Lazagne 1](https://github.com/user-attachments/assets/d44bb59e-b140-4c7e-8db4-4e366f24ed31)
  *Ref 5: Downloading Lazagne onto the Windows server*

  ![Lazagne 2](https://github.com/user-attachments/assets/44b10564-1641-4d16-b593-c38610c534b1)
  *Ref 6: Lazagne Event*

  ![Lazagne 3](https://github.com/user-attachments/assets/e958d0a4-f73c-43be-a449-733df96268d6)
  ![Lazagne 4](https://github.com/user-attachments/assets/7c4c2596-c789-43f4-a0cf-84056a2df6c5)
  *Ref 7: Detection and Respon part of rule*

  

- The fourth step was to set up Slack and Tines as well as test connection with LimaCharle + Tines.
- The fith step was to send a Slack message, send an email containing info about the detection, and generate a user prompt to ask to isolate the machine and if yes then isolate the machine.
