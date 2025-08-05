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

**Make sure you have these before proceeding!**

# Setting up GitHub repositories

In these steps we'll create the Mod Resorts source and configuration repositories that will be used to develop and deploy the application.  We'll do this by forking two exiting repositories.

## Sign in to GitHub

1. In a browser, sign in to the email account provided by the instructors at https://login.one.com/mail.  This will be used for 2-factor authentication when signing into GitHub
2. In a second browser tab, sign into https://github.com with the ID provided by the instructors.  Use the code sent to the email account to complete the sign-in.

## Fork the source and config repositories

1. In the browser, go to https://github.com/easej-txc-lab-2025/mod-resorts-src
2. Click the "Fork" button to begin creating a fork
<img width="595" height="151" alt="image" src="https://github.com/user-attachments/assets/35b75d06-5fa8-4cb0-9722-01340d87c555" />

3. Then click "Create Fork" button to complete forking the repository into your student github account
<img width="596" height="455" alt="image" src="https://github.com/user-attachments/assets/d8def60a-89c7-476f-b6bc-0e9df717ba2a" />

4. In the browser, go to https://github.com/easej-txc-lab-2025/mod-resorts-cfg
5. Click the "Fork" button to begin creating a fork
6. Then click "Create Fork" button to complete forking the repository into your student github account





7. Configure Service Instance - 10m
8. Familiarize with the UI - WalkMe + anything not covered by WalkMe (use this to capture new WalkMe requirements) - 5m
9. Make an application change and test locally - Start VS Code, Dev Mode, code change, see results, run tests, etc - 10m
10. Create a pull-request to test in EASeJ - commit change, create PR, go see the build, view tests, etc.  - 10m
11. Merge pull-request to deliver, build, and test change - merge PR, go see the build, view test results, etc.
12. Update staging config and create pull-request to validate - copy the version, update yaml, commit change, create PR, view config validation
13. Merge pull-request to deploy to staging - merge PR, view deployment job, see results
14. Validate application working in staging - go to staging, see the instance, view the app.
(optional Production)
15. Update production config and create pull-request to validate - promote by copying version, update yaml, commit change, create PR, view config validation
8. Merge pull-request to deploy to production - merge PR, view deployment job, see results
9. Validate application working in production - go to production, see the instance, view the app.
11. Party like it's 1999!
12. Bonus - server dump, trace log
13. 
