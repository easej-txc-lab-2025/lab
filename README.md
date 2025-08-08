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



# Configure the EASeJ Service Instance

1. In a browser, access your EASeJ instance using the URL provided by the instructors.  You will need to use your instructor provided web mail account for 2-factor authentication.
2. Once signed click on `Open dashboard`
<img width="596" height="259" alt="image" src="https://github.com/user-attachments/assets/78c1c44d-e8ab-4759-9817-3d03018866ed" />

3. Review and click through the introductory screens, for example:
<img width="585" height="515" alt="image" src="https://github.com/user-attachments/assets/e16e36fd-a4fb-4760-a901-7ffe2c88ceec" />

4. Click `Install and configure` to begin the setup process
<img width="393" height="296" alt="image" src="https://github.com/user-attachments/assets/0260ede4-47b0-44ce-85dc-18abc603bd34" />

5. EASeJ provides built-in build and deploy pipelines. If you already have a build pipeline, you can use EASeJ's "Deploy and run your application" option. In this lab you will use both pipelines, so select the `Build, deploy and run your application` option and click `Next`
<img width="602" height="320" alt="image" src="https://github.com/user-attachments/assets/e9909416-a60f-45f0-bd16-23969fba22c7" />

6. EASeJ's build and deploy pipelines are driven by events from GitHub.  To set up this integration, you need to authorize EASeJ to access GitHub.  EASeJ only limited GitHub access. Click `Authorize Access to GitHub`
<img width="600" height="322" alt="image" src="https://github.com/user-attachments/assets/3afa05a3-194a-42e4-9fb1-1a03079e5ef6" />

7. A GitHub page will pop up asking you to authorize EASeJ. This GitHub page is using the GitHub account you are already signed in with.  Click `Authorize IBM Enterprise Application Service`
<img width="477" height="516" alt="image" src="https://github.com/user-attachments/assets/08e09255-1c7e-4d66-a538-96003bf64696" />

8. You should see that authorization was successful.  Click `Next` to proceed
<img width="603" height="313" alt="image" src="https://github.com/user-attachments/assets/de606ba3-4ccb-402b-ae72-7cb619fa63ee" />

9. Next you'll select the github organization where the src and cfg repos reside.  Choose what should be the only option, which is your GitHub id
<img width="600" height="309" alt="image" src="https://github.com/user-attachments/assets/395873e2-2265-4996-9f45-f33f68a3945e" />
   
10. A dialog will appear asking you to install the EASeJ GitHub App.  This app is the thing that lives in GitHub and provides the integration between GitHub and EASeJ.  Click `Install GitHub App`
<img width="595" height="281" alt="image" src="https://github.com/user-attachments/assets/6d453a43-6770-4229-a8ce-bd6e6e0701e1" />

11. Another GitHub page will appear to ask which repositories the EASeJ GitHub App should have access to.  You could pick the specific src and cfg repositories, but to keep things simple leave as `All repositories` and click `Install`.  If prompted to, log in with your lab GitHub password.
<img width="379" height="517" alt="image" src="https://github.com/user-attachments/assets/69eda77f-8321-4dc0-a362-f74de9eb727f" />

12. You should see that the app install was successful.  Click `Next` to proceed.
<img width="602" height="312" alt="image" src="https://github.com/user-attachments/assets/c37c160b-6074-4a08-8918-6a32b2421ddf" />

13. Next you'll tell EASeJ which repository contains the source code.  Select `mod-resorts-src` and click `Next`
<img width="600" height="313" alt="image" src="https://github.com/user-attachments/assets/b741a462-1dfb-468a-a55b-77cdd179751d" />

14. Now tell EASeJ which repository contains the deployment configuration.  Select `mod-resorts-cfg` and click `Next`
<img width="606" height="311" alt="image" src="https://github.com/user-attachments/assets/fd4acbe5-4778-4dd2-92d4-5937e60c24aa" />

15. Review the settings and click `Finish` followed by `Confirm` on the dialog.
<img width="607" height="309" alt="image" src="https://github.com/user-attachments/assets/6f649db6-85f6-48b1-8e4c-6a36ae29f883" />

16. You will be automatically take to the EASeJ dashboard that looks like this
<img width="599" height="330" alt="image" src="https://github.com/user-attachments/assets/ff6718b1-a95e-478d-ab6c-78bd0b412069" />

# Familiarize yourself with the EASeJ UI 

The dashboard is the place that summarizes the status of your application and its delivery.  At the top you'll see information on the GitHub configuration:

<img width="596" height="174" alt="image" src="https://github.com/user-attachments/assets/675f51dc-a377-4ce3-99ff-69627c72e510" />

Below that are Actions.  Actions are steps EASeJ recommends you take to ensure your applications is in good shape.  This may be empty, but if the initial release build (more on this in a minute) has completed, you'll see an action like this.  

<img width="571" height="286" alt="image" src="https://github.com/user-attachments/assets/d53dd0ad-ff99-45c8-9cc8-2469fbc219b6" />

This action is just to help you get started with EASeJ so it not essential, but EASeJ Actions beyond this are strong recommendations. 

Further down the page you will see the two built-in environments where the application runs; Production, and Stating.  They are in this order because Production is more important.  In fact, the whole Dashboard is ordered in this way.  We haven't deployed anything yet, so there's not a lot to see.

<img width="597" height="145" alt="image" src="https://github.com/user-attachments/assets/29435fb5-25bb-42cd-8419-27bd1197d36d" />

Scrolling down will show the `Deployment jobs`. These are the deployment pipeline jobs run to deploy a release build to staging or production.  By default, Production deployment jobs are show, but you can click `Staging` to switch to Staging.  Again, we haven't deployed anything so there's nothing to see.

<img width="597" height="216" alt="image" src="https://github.com/user-attachments/assets/44ac46d5-1d5c-471d-a30b-5389f719186e" />

At the bottom of the dashboard are Release Builds.  EASeJ automatically starts a Release Build after initial setup using the contents of the source repository.  If the bar is blue, then the build is in progress.  Once successfully completed, the bar turns green.  Hoverring over the bar shows a summary of the build, including tests.

<img width="597" height="326" alt="image" src="https://github.com/user-attachments/assets/69574339-9e67-4ed4-88e1-712024c06396" />

Each Dashboard tile links to the details for the things it represents.  Also, clicking on the green (or blue) Release Build bar takes you to the Release Build details page.  One that page, you can view the build log, test results, and download the artefacts produced by the build.

<img width="599" height="276" alt="image" src="https://github.com/user-attachments/assets/d31102f3-4dee-4a11-b51a-5b607a1971f2" />

Clicking on `Enterprise Application Service for Java` brings you back to the Dashboard

<img width="488" height="250" alt="image" src="https://github.com/user-attachments/assets/bf17ec86-bff9-4fa7-a7e8-fd131c10483f" />

Lastly, to see all the UI features available, you can click on the hamburger menu

<img width="486" height="253" alt="image" src="https://github.com/user-attachments/assets/34d6b397-3b02-4e74-96d1-a50e61fac1cd" />

And this will display a menu of all the EASeJ options:

<img width="274" height="505" alt="image" src="https://github.com/user-attachments/assets/7adf2a17-a07b-412f-9f7f-0b149d5a5f0d" />

You'll see that there are more options displayed than are on the dashboard.  These are:
* `Home`: returns to the dashboard
* `Pull request builds`: view builds initiated by a pull request being created in the source repository
* `Config validation`: view config validations initiated by a pull request being created in the configuration repository
* `Secrets`: provides built-in secrets management.
* `Integrations`: provides assitance in integration with Db2, MQ, on-premise systems, external logs and monoitoring.
* `Settings` (partially obscured at the bottom): shows service configuration information and enables updating, for example, repository integrations.


# Make an application change and test locally

## Start Dev Mod and review the app

You're now going to act as a developer for the application.  In this section, you'll develop and test a change locally, and in subsequent sections, you'll deliver the code and eventually deploy the updated application it to an environment.

1. In your VS Code instance that's opened with the source code, open the `Explorer` view, if it's not already, and expand the `LIBERTY DASHBOARD` accordion.  You should see `moderesorts` listed.
<img width="345" height="491" alt="image" src="https://github.com/user-attachments/assets/db5449fb-5e96-4288-81f5-22ebbbddd3f8" />

2. Right click on `modresorts` to bring up the context menu and choose `start`.  This will start Liberty locally in what is called `Dev Mode`.  Dev Mode makes it really quick and easy to develop applications because it does TODO....
<img width="340" height="461" alt="image" src="https://github.com/user-attachments/assets/023582d0-9b19-47e8-9806-213f1334c93f" />

3. In the terminal tab, you'll see a maven build runs that download and installs Liberty (just the features used by the app), builds the modresorts app, and then starts the server with the app deployed.  Once complete you should see a screen like this:
<img width="959" height="276" alt="image" src="https://github.com/user-attachments/assets/406740b6-3b04-480c-b03f-07c2e7e53817" />

4. Hovver over the URL in the message that begins with `Web application available...` and press `Ctrl-Click`.  This will bring up a dialog, choose `Open`.
<img width="595" height="189" alt="image" src="https://github.com/user-attachments/assets/c71b92f3-75c1-4efc-98eb-2aab8ac75f24" />

5. You will see the modresorts app load in a new browser tab.
<img width="1383" height="597" alt="image" src="https://github.com/user-attachments/assets/1ede5dd6-f4ca-4027-a715-bd99da7cd914" />

6. Expand the "Where to?" to see the list of destinations.  You're going to add a new destination to the app.
<img width="327" height="343" alt="image" src="https://github.com/user-attachments/assets/cfc33d72-58fb-4fcc-a421-bef2003bef68" />

## Update the app

1. In the VS Code IDE for mod-resorts-src, expand `WebContent` and click on `index.html` to open it for editing.  Scroll about of quarter of the way down the file to where the destinations are listed
<img width="723" height="285" alt="image" src="https://github.com/user-attachments/assets/99580da4-2952-404b-a8f9-02d1c03b504f" />

2. Add a new destination, e.g. `<option value="Orlando">Orlando, USA</option>` and save the file with `Ctrl-S`
<img width="595" height="233" alt="image" src="https://github.com/user-attachments/assets/3caf06b1-2188-4fc9-b5b0-0179d281650b" />

3. In the modresort browser tab, reload the page with `Ctrl-R` and expand `Where to?` to see the new destination.  Note, to make this update, all you did was modify the source.  You didn't have to run a new build, package the app, restart the server.  Dev Mod handled the update for you.  This was a static file change, but if it had been a Java change, Dev Mod would have handled it the same. It's that easy.
<img width="315" height="376" alt="image" src="https://github.com/user-attachments/assets/e3f1c807-8db0-4769-ade8-6121e3f95213" />

# Create a pull-request to build and test in EASeJ

You've completed the development and tested locally, next you want to build and test the update in EASeJ before the code is integrated into the main branch.

# Merge pull-request to deliver, build, and test change - merge PR, go see the build, view test results, etc.

# Update staging config and create pull-request to validate - copy the version, update yaml, commit change, create PR, view config validation

# Merge pull-request to deploy to staging - merge PR, view deployment job, see results

# Validate application working in staging - go to staging, see the instance, view the app.

# (Optional) Update production config and create pull-request to validate - promote by copying version, update yaml, commit change, create PR, view config validation

# (Optional) Merge pull-request to deploy to production - merge PR, view deployment job, see results

# (Optional) Validate application working in production - go to production, see the instance, view the app.

# Party like it's 1999!

# Bonus - server dump, trace log

