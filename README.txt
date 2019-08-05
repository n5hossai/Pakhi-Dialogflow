There are 53 parent intents for the pakhi, and then some of them have child intents. I am forming a tree below for the names:

 0 End Conversation
 1 Get Started
 2 Welcome + Choose Language
 3 Type of Service (Customer, Merchant, Agent)
 4 General options for Customer
 5.1 General Information (Customer)
 5.1 General Information (Customer) - Cash In
 5.1 General Information (Customer) - Change PIN
 5.1 General Information (Customer) - Check Balance
 5.1 General Information (Customer) - Limits
 5.1 General Information (Customer) - Mobile Recharge
 5.1 General Information (Customer) - Pay Bills
 5.1 General Information (Customer) - Payment
 
 5.1 General Information (Customer) - Send Money {
  > 5.1 General Information (Customer) - Send Money - Sender's Number {
	> 5.1 General Information (Customer) - Send Money - Sender's Number - Receiver's Number Add follow-up intent  {
	 > 5.1 General Information (Customer) - Send Money - Sender's Number - Receiver's Number - amount
	 }    
	}   
 }

 5.2 General Information (Customer)
 5.2 General Information (Customer) - Balance Statement
 5.2 General Information (Customer) - Bank Transfer
 5.2 General Information (Customer) - Remittance
 6 I forgot my PIN
 7 About Offers
 8 Open a new bKash Account
 9 FAQ
 About App
 About App - Supported Devices
 About App - Supported Devices - 1 Rooted Android
 About App - Supported Devices - 2 Jailbreak Apple
 About App - Supported Devices - 3 Not Rooted Device
 About App - Supported Devices - 4 MFS app use
 About App -How to use bKash App
 After converting my mobile network (MNP), I don’t get any confirmation texts and OTP.
 
 Agent as Service Type {
  > Agent as Service Type - 1. Becoming an Agent
 }
 
 App not working
 Ask a question
 bKash Calculator
 
 Cash out {
 >Cash out - Agent 
 }
          {
 >Cash out - ATM
 }
 
 Cash/Money Input
 Default Fallback Intent
 Fallback when Bangla chosen
 I can’t use the app. The text- ‘The app works only in Bangladesh’ pop up while opening the app.
 I don’t get any verification codes (OTP).
 I want to send money to 01555666777.
 input given was only agent
 input given was only PIN
 Issues
 ISSUES - I can't see bKash app without inserting bKash registered SIM card on my phone.
 ISSUES - The app keeps crashing continuously on my phone.
 ISSUES - Why can’t I use bKash app even if I don’t use a rooted device?
 ISSUES - Why can’t I use bKash app on Jailbreak Apple devices?
 ISSUES I can't log in via bKash app
 ISSUES-Why can't I used bKash app on Rooted Android devices?
 Merchant as a service type
 Merchant as a service type - open account
 web view test
 #######################################################################################################
 In the folder you will see three sub folders: entities, intents and small talks. For the small talks, you have to manually type in the respones.
 
 For the entities, upload the json file in the entity section, by clicking on the three vertical dots, on the top right corner, beside "Create Entity"
 
 For the intents part, at first you have to understand that you cannot upload more than one intent at a go. The picture with "upload intent 1" shows, the upload intent part and then upload the jspon files.
 
 Now, upload the intents json files which are not inside any folders. This json files are without any child.
 
 The json files which are inside folders, have child and those inside have others. Follow the tree of the json files given above.
 
 
 
 The json files have their parent root id mentioned properly, but in case, you have problem, follow the steps (also see "upload intent 2"):
 
 1. Let's talk about putting "Agent as Service Type - 1. Becoming an Agent" as a follow up intent inside "Agent as Service Type"
 2.  The child has three id. The first is the child's unique id. The second one, parent id, is the child's immediate parent id. And the root id is the very very first id, which can be the gradnfather, or even higher.

      "id": "0a123158-2137-4a6a-9226-c292d03b577f",
      "parentId": "7e64ca6f-9e03-4ae1-9c4b-3bba1c2804b0",
      "rootParentId": "7e64ca6f-9e03-4ae1-9c4b-3bba1c2804b0",
	  
3. Therefore, if you can copy the id of the parent and then copy paste and change it inside the json file of the child id, when you upload it, it will automatically form as a follow up intent, and you won't have to bother on how to upload follow up intents.
In case you still face difficulty, please feel free to shoot an email at n5hossai@edu.uwaterloo.ca 	  
 
 