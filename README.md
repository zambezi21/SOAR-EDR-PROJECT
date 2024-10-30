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

- The third step is to generate telemetry using LaZagne and create a detection and response rule. Start by downloading LaZagne on the server, then go to Tines to view the LaZagne event details. This information will assist in creating a detection rule. Use an existing rule as a template and modify it for your use case to create both the detection and response components. Test the rule in LimaCharlie to ensure accuracy. Finally, run ./LaZagne.exe all in the PowerShell command line on the Windows server. Return to Tines, where the event will appear in the Detections tab.
  
  ![Lazagne 1](https://github.com/user-attachments/assets/d44bb59e-b140-4c7e-8db4-4e366f24ed31)
  *Ref 5: Downloading Lazagne onto the Windows server*

  ![Lazagne 2](https://github.com/user-attachments/assets/44b10564-1641-4d16-b593-c38610c534b1)
  *Ref 6: Lazagne Event*

  ![Lazagne 3](https://github.com/user-attachments/assets/e958d0a4-f73c-43be-a449-733df96268d6)
  ![Lazagne 4](https://github.com/user-attachments/assets/7c4c2596-c789-43f4-a0cf-84056a2df6c5)
  *Ref 7: Detection and Response part of rule*

  ![Screenshot (7)](https://github.com/user-attachments/assets/bbd2c603-075f-4587-807b-21605d0bef6f)
  *Ref 8: Testing of the rule*

  ![Screenshot (8)](https://github.com/user-attachments/assets/462a6440-a86a-40d0-85f2-daeb81e306b3)
  *Ref 9: The event in LimaCharlie*

- The fourth step was to set up Slack and Tines as well as test connection with LimaCharle + Tines.

  ![Tines 3](https://github.com/user-attachments/assets/afaad2b7-dda0-4c21-b9d6-e8f8dd8bfa95)
  *Ref 10: Set up Slack Channel*
  
  ![Tines 1](https://github.com/user-attachments/assets/aa3a961d-6c38-4aaf-b249-34498c654f63)
  *Ref 11: Set up Tines*

  ![Tines 3 (2)](https://github.com/user-attachments/assets/69c771d2-f1eb-4aaa-b395-b7d6dcae4f87)
  ![Tines 4](https://github.com/user-attachments/assets/e33cf832-5ac5-42b0-9db5-0be51269a84a)
  *Ref 12: Test connection btw LimaCharle + Tines*

- TThe fifth step involves sending a Slack message, emailing information about the detection, and generating a user prompt to request machine isolation. If the response is "yes," proceed to isolate the machine. Begin by setting up the integration between Tines and Slack and testing both the Slack and email links from Tines. Next, configure the user prompt with actions for "yes" and "no" responses, specifying the message to send to Slack if the response is "no" and initiating communication with LimaCharlie if the response is "yes." Run the entire workflow to test its functionality and ensure the machine is isolated as expected. Finally, verify by pinging a website from the Windows server; the result should indicate "General failure."
  
  ![Slack 1 (2)](https://github.com/user-attachments/assets/38a44b69-20cd-4836-9b2a-8e6a8b17285d)
  ![Slack 2](https://github.com/user-attachments/assets/b0eed4bf-e02e-474c-bf87-966ffd475238)
  ![Slack 3](https://github.com/user-attachments/assets/981d18cc-93a5-402d-9742-05bf45e1f499)
  *Ref 13: Conection with Tines and Slack, Testing the link betwwen them as well as email*

  ![Mutende-SOAR-EDR-Project-storyboard](https://github.com/user-attachments/assets/c5e27be9-9dff-4d18-9d78-158a621fc207)
  *Ref 14: Tines whole playbook graph*
  ![Slack 2](https://github.com/user-attachments/assets/b0eed4bf-e02e-474c-bf87-966ffd475238)
  ![Slack 3](https://github.com/user-attachments/assets/981d18cc-93a5-402d-9742-05bf45e1f499)
  ![Slack 4](https://github.com/user-attachments/assets/881fe428-0178-4a71-9891-c1b539774061)
  ![Slack 5](https://github.com/user-attachments/assets/0942cf80-6025-44be-8910-0517fd7af277)
  ![Slack 6](https://github.com/user-attachments/assets/be355f01-2a11-4f60-a871-25530d03a261)
  ![Slack 7](https://github.com/user-attachments/assets/3656f427-bd29-49ae-8314-00603d94c482)
  *Ref 15: Workflow test run with yes as user prompt*
