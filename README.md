# Enterprise Application Service for Java TechXchange 2025 Lab

# Lab Structure

Source repos prepopulated with mod-resorts
Config repo prepopulated with Staging and Production environment yamls.

IBM Cloud Logs - Need cloud credits (no work for the people to do).  Monitoring is more problemmatic.  

0. Intro slides to EASeJ - 10m
0.1 Install EASeJ Tools - 10m - need to check if it will be feasible for us to install the night before

# Install the EASeJ Tools _beta_

The EASeJ Tools Beta was released after the lab VM was created, so we first need to install the tools.

TODO: Add the steps

1. 
   
# Get your lab IDs

Each student will be provided with the following:
1. A GitHub ID
2. A web email email address
3. Lab VM login

**Make sure you have these before proceeding!**

# Setting up GitHub repositories

In these steps you'll create the Mod Resorts source and configuration repositories that will be used to develop and deploy the application.  You'll do this by forking two exiting repositories.

## Sign in to GitHub

1. Log in to the Lab VM using using the `admin` id and the password provided by the instructors
2. In a browser, sign in to the email account provided by the instructors at https://login.one.com/mail.  This will be used for 2-factor authentication when signing into GitHub
3. In a second browser tab, sign into https://github.com with the ID provided by the instructors.  Use the code sent to the email account to complete the sign-in.

## Fork the source and config repositories

Pre-populated source and configuration repositories are provided.  You need to fork them into your github account to use them separate from the other lab participants.


1. Open the Firefox browser by clicking on `Activities` -> `Show Applications` and choosing the Firefox icon.
2. In the browser, go to https://github.com/easej-txc-lab-2025/mod-resorts-src
3. Click the "Fork" button to begin creating a fork
<img width="595" height="151" alt="image" src="https://github.com/user-attachments/assets/35b75d06-5fa8-4cb0-9722-01340d87c555" />

4. Then click "Create Fork" button to complete forking the repository into your student github account
<img width="596" height="455" alt="image" src="https://github.com/user-attachments/assets/d8def60a-89c7-476f-b6bc-0e9df717ba2a" />

5. In the browser, go to https://github.com/easej-txc-lab-2025/mod-resorts-cfg
6. Click the "Fork" button to begin creating a fork
7. Then click "Create Fork" button to complete forking the repository into your student github account

## Clone the repositories

Cloning the source and configuration repositories copies them to the Lab VM so you can work with them locally.

### Clone the source repository

1. Start Visual Studio Code by clicking on `Activities` and `Show Applications` and choosing the VS Code icon.
2. On the Welcome page, choose `Clone Git Repository...`
<img width="370" height="428" alt="image" src="https://github.com/user-attachments/assets/82c4a97f-47cb-44b7-bb46-bc01e5a74a1c" />

3. Enter the URL for the source repository into the command field - https://github.com/easej-txc-lab-2025/mod-resorts-src and choose `Clone from GitHub`
<img width="584" height="98" alt="image" src="https://github.com/user-attachments/assets/982c3bae-669a-4b85-9f75-93ff020d80ce" />

4. Follow the step to authorize VS Code to access github under your github id, which end with this final confirmation.  Click `Authorize Visual-Studio-Code`
<img width="342" height="35" alt="image" src="https://github.com/user-attachments/assets/ab46a671-b2f6-42e1-8f2f-0a79723903b7" />

5. Select the `mod-resorts-src` repository from the list
<img width="581" height="131" alt="image" src="https://github.com/user-attachments/assets/a002e222-7448-491d-bba1-4c57a65a82eb" />

6. In the dialog, click `Select as Repository Destination` to clone the repository to the `Home` directory
<img width="495" height="53" alt="image" src="https://github.com/user-attachments/assets/9d9e1435-bf83-4525-b784-09e38b0baf72" />

7. Choose `Open in New Window` to open a new VS Code window to work in
8. <img width="562" height="152" alt="image" src="https://github.com/user-attachments/assets/23fbe429-b11a-43b4-8ce0-b2c42f034969" />

### Clone the configuration repository

1. On the Welcome page of the **first VS Code window**, choose `Clone Git Repository...`.
2. Enter the URL for the config repository into the command field - https://github.com/easej-txc-lab-2025/mod-resorts-cfg and choose `Clone from GitHub`

3. Select the `mod-resorts-cfg` repository from the list
<img width="582" height="134" alt="image" src="https://github.com/user-attachments/assets/a1771c3b-a458-41b3-b8ef-93616e0f81da" />

4. In the dialog, click `Select as Repository Destination` to clone the repository to the `Home` directory
<img width="495" height="53" alt="image" src="https://github.com/user-attachments/assets/9d9e1435-bf83-4525-b784-09e38b0baf72" />

5. This time, choose `Open` to open in the same VS Code window to work in
<img width="564" height="159" alt="image" src="https://github.com/user-attachments/assets/0251e740-16fd-4d69-865c-4b1669687ae4" />

You should now have two VS Code instances, one for working on the `src` repo and the other for working on the `cfg` repo.



# Configure Service Instance - 10m

# Familiarize with the UI - WalkMe + anything not covered by WalkMe (use this to capture new WalkMe requirements) - 5m

# Make an application change and test locally - Start VS Code, Dev Mode, code change, see results, run tests, etc - 10m

# Create a pull-request to test in EASeJ - commit change, create PR, go see the build, view tests, etc.  - 10m

# Merge pull-request to deliver, build, and test change - merge PR, go see the build, view test results, etc.

# Update staging config and create pull-request to validate - copy the version, update yaml, commit change, create PR, view config validation

# Merge pull-request to deploy to staging - merge PR, view deployment job, see results

# Validate application working in staging - go to staging, see the instance, view the app.

# (Optional) Update production config and create pull-request to validate - promote by copying version, update yaml, commit change, create PR, view config validation

# (Optional) Merge pull-request to deploy to production - merge PR, view deployment job, see results

# (Optional) Validate application working in production - go to production, see the instance, view the app.

# Party like it's 1999!

# Bonus - server dump, trace log

