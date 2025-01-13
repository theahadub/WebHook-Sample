# Mac-Tricks

Sample code for a Webhook to connect to Microsoft teams.  

How to make the webhook on Teams:
  doc and example about making webhooks at  https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/connectors-using?tabs=cURL
  Adaptive Card samples and templates https://adaptivecards.io/samples/

One way to use this in Jamf
- Copy this script into Jamf > Settings > Computer Management > Scripts filling out the options for the parameters and set a trigger (installstart)
- Create a policy to call the script filling in the parameters (remote installation started)
- Run the policy
  - sudo jamf policy -event installstart
  - sudo jamf policy -event remoteinstallstart
Now you will have an alert in Teams that the remote install event started.  You can clone the policy and make a installended hook as well.

sample script<br>
<img width="732" alt="image" src="https://github.com/user-attachments/assets/e9739f7e-f13b-434c-a58a-0bf5187ee501" />
<br>
sample output<br>
<img width="371" alt="image" src="https://github.com/user-attachments/assets/23da4c76-9133-473c-bc5b-435f8138be1a" />

