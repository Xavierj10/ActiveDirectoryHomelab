# Active Directory Home Lab
#### I decided to do this lab to help me get exposure to Microsoft Server2019 and Active Directory. The hard part about not being in the field of IT is not having access to certain technologies so you have to get experience on your own. So this will be one of my many first home labs I will be documenting on GitHub.
## Tools Used
- [Oracle VirtualBox](https://www.virtualbox.org/)
- [Windows Server2019](https://info.microsoft.com/ww-landing-windows-server-2019.html)
- [Youtube](https://www.youtube.com/watch?v=MHsI8hJmggI)


## Lab Overview
### In this lab you will learn how to: 
  - Set up VirtualBox
  - Set up Windows Server2019
  - Set up Microsoft Active Directory
  - Add 25 users manually to Active Directory
  - Create 5 seperate workgroups to separate the users into
  
  
 ## Step One: Set up VirtualBox and Active Directory
  - To get fully set up I recommend following along to [Josh Madakdor's Youtube Video](https://www.youtube.com/watch?v=MHsI8hJmggI)
  #### I recommend this video because its straight to the point and easy to follow along. He talks about setting an internal network and using a powershell script but I wouldnt worry about those this project is meant to introduce you to Active Directory and How it works.
  
<img width="1207" alt="Screenshot 2023-01-02 at 6 03 51 PM" src="https://user-images.githubusercontent.com/121701900/210286252-3bf9f7f5-4ed2-45cd-89b6-9962c741bf41.png">

## Step Two: Add new users in Active Directory

<img width="388" alt="Screenshot_20230102_080821" src="https://user-images.githubusercontent.com/121701900/210291857-7f345703-dd71-457f-bbe2-bb5dcc8f9a39.png">

- Right Click on Users
- Go to New wait for the extend menu to load
- And then click on User and the input field will open up


<img width="395" alt="Screenshot_20230102_081310" src="https://user-images.githubusercontent.com/121701900/210292130-42d1e1ff-3f30-4c3a-929e-b432e0f9435c.png">

- Fill in First and Last Name for the New User
- For User Logon Name use the user's First Initial and Last name
- Click Next to set up the User with a password
- Once thats done click Finish and the new User will be added
-  You wanna do this at least twenty-five times or as many times as you want


## Step Three: Create AD Organizational Unit named "Groups"
#### Before you create the groups themselves you must first create an OU or an Organization Unit to put those groups into
<img width="389" alt="Screenshot_20230102_082303" src="https://user-images.githubusercontent.com/121701900/210292831-2125fe32-e7e9-4a4a-a264-b307b21bce2f.png">
 
 - First right click on the domain name you created for the server
 - Second click on New and then click Organizational Unit
 - Another input field will open up and this where you will type "Groups"

<img width="429" alt="Screenshot_20230102_083512" src="https://user-images.githubusercontent.com/121701900/210294047-5e91ccf3-7e5f-4f36-a507-80cb4b2ff2f0.png">


## Step Four: Add five workgroups to the OU named Groups simulating different workgroups within an actual organization
- Right click on Groups, go to New and add group
<img width="486" alt="Screenshot_20230102_093023" src="https://user-images.githubusercontent.com/121701900/210297136-456f5b27-a5e0-43c6-aaba-7078b83111b1.png">

- You wanna do this five times until the groups tab looks like the photo below, feel free to use the same group names I used
<img width="445" alt="Screenshot_20230102_094202" src="https://user-images.githubusercontent.com/121701900/210297418-fe5a57f8-b3ba-4479-a525-713eba0d2e2c.png">

## Step Five: Add the users you created to the separate groups
- First double-click on one of the group names to open up the group information
- Then click on members
<img width="439" alt="Screenshot_20230102_100027" src="https://user-images.githubusercontent.com/121701900/210298555-c20f6400-ab4d-4e0e-9bb2-4cf6713df877.png">

- Yours won't look like mine at least yet
- Click the add button and another window will open
<img width="438" alt="Screenshot_20230102_100627" src="https://user-images.githubusercontent.com/121701900/210298880-a7cd52e5-7c85-4a23-bbf5-c20186f60855.png">

- In the box type in the name of one your users
- And then click check names
- If you typed in the name right it should populate just like the photo below
<img width="443" alt="Screenshot_20230102_101033" src="https://user-images.githubusercontent.com/121701900/210299109-752a6e5c-115b-4559-901b-a30516187631.png">

- Once you press OK the user will be added
- After that continue adding all of your users separating them into whichever groups you like

## User Password Reset Simulation
- As an IT help desk professional there's gonna be a lot of times where you're doing password resets at least based on what I've been told from Youtube videos.
- In a real organization you will have more than 25 users so you wont be able to just scroll through the Users tab looking for the User that needs a reset.
- Instead you'll right-click on the Users tab and click find.
<img width="441" alt="Screenshot_20230102_102700" src="https://user-images.githubusercontent.com/121701900/210300088-cd4d2bdf-5c99-4787-8df5-c194136bfa20.png">

- Type in the name of the user in the field that needs the reset
- Press "Find"
- Once the user is found it will populate in the bottom of the pop up
<img width="481" alt="Screenshot_20230102_103127" src="https://user-images.githubusercontent.com/121701900/210300479-80df27a2-9d4b-4c6f-94fc-8067365027e2.png">
- Right click on the User
- Click on reset password
- And a password reset field will pop up
<img width="423" alt="Screenshot_20230102_104142" src="https://user-images.githubusercontent.com/121701900/210301120-319d4192-a36e-4873-8df0-5ab75e96b621.png">

- When resetting the password make sure the password is something simple the user will remember
- Make sure the box for user changing password on next logon is checked and the Unlock user account is unchecked before you press Ok.
### And you have successfully simulated a user password reset.








