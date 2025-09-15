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
4. In a terminal window, set the git user.name and user.password using the following commands:

TODO: Work out if this is needed and where it goes.  It has to be after the OAuth login in VS Code....
```
git config --global user.name "YOUR GITHUB NAME"
git config --global user.email "EMAILID@wweasej.com"
```

## Fork the mod-resorts-src and mod-resorts-cfg repositories

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

2. **Install VS Code Plug for GitHub Pull Requests:** Unfortunately, the VS Code installation in the VM is missing a plugin so we need to install it. In VS Code, select the plugins Icon, filter for `GitHub`, and click `Install` for the `GitHub Pull Requests` plugin.
<img width="429" height="363" alt="image" src="https://github.com/user-attachments/assets/2a6c8ddb-de74-4c5e-a2e1-3c30a48c8300" />

3. On the Welcome page, choose `Clone Git Repository...`
<img width="370" height="428" alt="image" src="https://github.com/user-attachments/assets/82c4a97f-47cb-44b7-bb46-bc01e5a74a1c" />

4. Enter the URL for the source repository into the command field - https://github.com/YOUR_GITHUB_ID/mod-resorts-src (remembering to replace `YOUR_GITHUB_ID` and choose `Clone from GitHub`
<img width="584" height="98" alt="image" src="https://github.com/user-attachments/assets/982c3bae-669a-4b85-9f75-93ff020d80ce" />

5. Follow the step to authorize VS Code to access github under your github id, which end with this final confirmation.  Click `Authorize Visual-Studio-Code`
<img width="547" height="268" alt="image" src="https://github.com/user-attachments/assets/0fce8092-cc1b-4208-9cd8-2001965ba21f" />

6. Select the `mod-resorts-src` repository from the list
<img width="581" height="131" alt="image" src="https://github.com/user-attachments/assets/a002e222-7448-491d-bba1-4c57a65a82eb" />

7. In the dialog, click `Select as Repository Destination` to clone the repository to the `Home` directory
<img width="495" height="53" alt="image" src="https://github.com/user-attachments/assets/9d9e1435-bf83-4525-b784-09e38b0baf72" />

8. Choose `Open in New Window` to open a new VS Code window to work in
<img width="562" height="152" alt="image" src="https://github.com/user-attachments/assets/23fbe429-b11a-43b4-8ce0-b2c42f034969" />


### Clone the configuration repository

1. On the Welcome page of the **first VS Code window**, choose `Clone Git Repository...`.
2. Enter the URL for the config repository into the command field - https://github.com/YOUR_GITHUB_ID/mod-resorts-cfg (remembering to replace `YOUR_GITHUB_ID`) and choose `Clone from GitHub`

3. Select the `mod-resorts-cfg` repository from the list
<img width="582" height="134" alt="image" src="https://github.com/user-attachments/assets/a1771c3b-a458-41b3-b8ef-93616e0f81da" />

4. In the dialog, click `Select as Repository Destination` to clone the repository to the `Home` directory
<img width="495" height="53" alt="image" src="https://github.com/user-attachments/assets/9d9e1435-bf83-4525-b784-09e38b0baf72" />

5. This time, choose `Open` to open in the same VS Code window to work in
<img width="564" height="159" alt="image" src="https://github.com/user-attachments/assets/0251e740-16fd-4d69-865c-4b1669687ae4" />

You should now have two VS Code instances, one for working on the `mod-resorts-src` repo and the other for working on the `mod-resorts-cfg` repo.

# Configure the EASeJ Service Instance

TODO: Update these instructions to go via https://cloud.ibm.com and then select their correct instance.  This avoid the long URLs.

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

Further down the page you will see the two built-in environments where the application runs; Production, and Staging.  They are in this order because Production is more important.  In fact, the whole Dashboard is ordered in this way.  We haven't deployed anything yet, so there's not a lot to see.

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

## Start Dev Mode and review the app

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

## Create a 'dev' branch

When working in teams it's a best practice to use a code branch to keep your changes separate and then deliver them when ready.  Teams would typicaly do this via a pull-request so you can have EASeJ validate your code changes, and then have another team member review the changes, and approve and merge them.  So before modifying the app, you're going to create a branch for your work.

To make the next few steps a bit simpler, we're going to do them in the GitHub terminal.  

1. Open the terminal by choose `View` > `Terminal`
<img width="395" height="430" alt="image" src="https://github.com/user-attachments/assets/e27f59ba-52a5-4ab0-bccd-ff281f6fbc34" />

2. In the terminal window, do the following commands:
```
git branch dev
git switch dev
git remote remove upstream
```

3. Click on `Publish Branch` to publish the branch to GitHub.  Ignore the notification to create a pull request.
<img width="419" height="216" alt="image" src="https://github.com/user-attachments/assets/c33d4159-534a-41f2-8dcb-270f213e6ac2" />


# Update the app

You're now ready to update the application in your `dev` branch.

1. In the VS Code IDE for mod-resorts-src, expand `WebContent` and click on `index.html` to open it for editing.  Scroll about of quarter of the way down the file to where the destinations are listed
<img width="723" height="285" alt="image" src="https://github.com/user-attachments/assets/99580da4-2952-404b-a8f9-02d1c03b504f" />

2. Add a new destination, e.g. `<option value="Orlando">Orlando, USA</option>` and save the file with `Ctrl-S`
<img width="595" height="233" alt="image" src="https://github.com/user-attachments/assets/3caf06b1-2188-4fc9-b5b0-0179d281650b" />

3. In the modresort browser tab, reload the page with `Ctrl-R` and expand `Where to?` to see the new destination.  Note, to make this update, all you did was modify the source.  You didn't have to run a new build, package the app, restart the server.  Dev Mod handled the update for you.  This was a static file change, but if it had been a Java change, Dev Mod would have handled it the same. It's that easy.
<img width="315" height="376" alt="image" src="https://github.com/user-attachments/assets/e3f1c807-8db0-4769-ade8-6121e3f95213" />

# Create a pull-request to build and test in EASeJ

You've completed the development and tested locally, next you want to build and test the update in EASeJ before the code is integrated into the main delivery branch.  To do this, you'll commit the code and create a pull-request.  Whenever a pull-request is created, EASeJ starts a Pull-request Build to build and test the code changes.

1. In the VS Code IDE for mod-resorts-src, click on the `Source Control` icon.  This should be showing a blue circle notification to say there is 1 pending change (the change made in the previous section).
<img width="413" height="366" alt="image" src="https://github.com/user-attachments/assets/2ca0bc1d-3fc4-4871-b393-e88165459395" />

2. You'll see that the index.html change is listed.
<img width="412" height="216" alt="image" src="https://github.com/user-attachments/assets/ab6b8a5c-453f-4195-b44d-80f5d1a3b673" />

3. `Right-click` on index.html to bring up the context menu and choose `Stage Changes`
<img width="370" height="382" alt="image" src="https://github.com/user-attachments/assets/56f0c43c-c32f-4b1c-abc6-3cdb2ea7d339" />

4. Expand the `Commit` options and choose `Commit & Create Pull Request`
<img width="597" height="342" alt="image" src="https://github.com/user-attachments/assets/4b15e50c-4a26-4527-9609-4b05e33c1a7d" />

5. An editor will appear for you to enter the commit message.  Type a meaningful message, e.g. "Added Orlando" and save with `Ctrl-S`.  
<img width="599" height="279" alt="image" src="https://github.com/user-attachments/assets/c880ef21-9eb8-4ee5-83a1-47d90f648844" />

6. Close the commit message file by clicking the "X"
<img width="431" height="156" alt="image" src="https://github.com/user-attachments/assets/9b3c5cda-9df3-4f6b-ace6-895b6ee36c3c" />

7. You will now see a summary of the pull request.  It will show that code is to be merged from `YOUR_GITHUB_ID/dev` to `YOUR_GITHUB_ID/main`.  Click the `Create` button.
<img width="293" height="434" alt="image" src="https://github.com/user-attachments/assets/e03c8edc-a90e-42e8-b166-c16791f05410" />

8. A new tab will open showing the created pull request.  EASeJ will now kick of a "Pull Request Build" to build and test the update.
<img width="594" height="372" alt="image" src="https://github.com/user-attachments/assets/5f2c6841-9a94-4eaa-8e39-24902f341f61" />

9. To view the pull-request build, in the EASeJ service UI, select the hamburger menu (top-left) and choose `Pull request builds`
<img width="233" height="298" alt="image" src="https://github.com/user-attachments/assets/8a31d8dc-7860-486c-b949-0cfbd6fe9bda" />

10. The page will show the pull-request build which may be in progress or completed
<img width="860" height="264" alt="image" src="https://github.com/user-attachments/assets/e69b73e2-a492-4079-b92e-c640fe66edfe" />

11. Click on the build id (1000) to view the pull request build details
<img width="587" height="89" alt="image" src="https://github.com/user-attachments/assets/c60d8257-714b-4315-8ca6-1031dc34a3e2" />

12. When the build is completed you'll be able to view the logs, tests results and downloads.  You should see that 4 tests were run, and that 3 passed and 1 was skipped.
<img width="420" height="281" alt="image" src="https://github.com/user-attachments/assets/8ca0d686-9e5c-459e-a2c1-526ab70a33fc" />

13. Click on `IBM Enterprise Application Service for Java" to go back to the EASeJ dashboard
<img width="321" height="71" alt="image" src="https://github.com/user-attachments/assets/4f7f7b38-45af-4a1a-a27c-c040df197175" />

# Merge pull-request to deliver, build, and test change - merge PR, go see the build, view test results, etc.

Your code changes built and passed the tests in EASeJ so it's time to merge the pull request into the main code branch.  A developer would typicall get a peer or team lead to review the pull request and merge it, but in this lab, you'll merge your own pull request.

1. In the VS Code tab for the pull-request, scroll down and click the `Merge Pull Request` button
<img width="594" height="432" alt="image" src="https://github.com/user-attachments/assets/bd884a60-9252-49d3-8736-3a09319497e5" />

2. In the same tab, scroll down and click the `Create Merge Commit` button.  This will cause a Release Build to start in EASeJ
<img width="595" height="422" alt="image" src="https://github.com/user-attachments/assets/24c19fb4-b4a3-43a5-9853-c75c62072bb3" />

3. In the EASeJ Dashboard, scroll down to the Release Build section and you should see a blue or green bar corresponding to the new build.  You can hover over it to see the details
<img width="539" height="425" alt="image" src="https://github.com/user-attachments/assets/bf1a3a6b-64bc-4153-95e7-d4dc0716b2e1" />

4. Click on the Release Build bar to view the details.  When the build is complete, you can view the logs, test results, and downloads.  Release builds have more artefacts available, including a SLSA provenance file that describes the application Bill of Materials (BOM).  This is useful when trying to determine if the applications is affected by a supply-chain injection attack.
<img width="473" height="228" alt="image" src="https://github.com/user-attachments/assets/d1704ca6-00c7-417a-82a5-4912559a687d" />

You've successfully contributed an update to the application. Next you'll deploy the new release build to the EAseJ Staging environment to verify that it's all working and ready for Production.

# Deploy the release to Staging

## Create an 'ops' branch

To deploy the new release to staging, you need to update the staging `environment.yaml`.  Teams would typicaly do this via a pull-request so you can have EASeJ validate the configuration, and then have another team member review the change, and approval and merge it.  To do this, you'll start by creating a branch in which you'll deliver the configuration change.

To make the next few steps a bit quicker, we're going to do them in the GitHub terminal.  

1. In the **VS Code window for mod-resorts-cfg**, Open the terminal by choose `View` > `Terminal`
<img width="432" height="448" alt="image" src="https://github.com/user-attachments/assets/33a66dfa-a793-4480-8d75-8e93a0f394c4" />

2. In the terminal window, do the following commands:
```
git branch ops
git switch ops
git remote remove upstream
```

3. Click on `Publish Branch` to publish the branch to GitHub.  Ignore the notification to create a pull request.
<img width="419" height="216" alt="image" src="https://github.com/user-attachments/assets/c33d4159-534a-41f2-8dcb-270f213e6ac2" />

## Prepare to deploy release build to staging

1. To deploy to staging, you need to set the version number in the staging `environment.yaml` to the version id of the release build to be deployed.  In the EASeJ Dashboard UI, scroll down to the `Release Builds` tile and select the left-most release build.  This is the one that was automatically run when you first configured the service instance.  A release build details page for the release build will open.
<img width="453" height="427" alt="image" src="https://github.com/user-attachments/assets/2aecf573-03f6-411e-8625-b69730ede4be" />

2. On the release build details page, click on `Deploy to staging`
<img width="763" height="329" alt="image" src="https://github.com/user-attachments/assets/11b49dcc-b4a4-4561-a9d7-321d83406b33" />

3. A tear-sheet will display instructions on how to deploy the release to staging. EASeJ doesn't not have write access to the GitHub repositories because many users would not allow this, and so the step explain how a user can do this using their GitHub id.  The first step is to copy the version id.  Use the copy icon to do this
<img width="807" height="332" alt="image" src="https://github.com/user-attachments/assets/5dc313da-8c43-4bd4-b84b-aa2e89210823" />

4. In VS Code for the `mod-resorts-cfg` repo, select the `Explorer`, expand `environments` -> `staging` and clock on `environment.yaml` to edit the file
<img width="465" height="479" alt="image" src="https://github.com/user-attachments/assets/84a35df6-9dc1-4529-8b51-663c8a9228f9" />

5. Past the version you copied earlier into the value for the version entry using `Ctrl-v`, then save the file using `Ctrl-s`
<img width="593" height="271" alt="image" src="https://github.com/user-attachments/assets/339c5aa8-c88f-42e1-bb34-fd392ae5b8c9" />

6. You've made the change, you now needs to push it to GitHub in the form of a pull-request.  Under `Source Control`, right click on the `environment.yaml` entry under Changes, and choose `Stage Changes`
<img width="380" height="401" alt="image" src="https://github.com/user-attachments/assets/96da168c-1424-49be-954a-7c57df1e1187" />

7. Choose the Commit pull-down menu and click on `Commit & Create Pull Request`, an COMMIT_EDITMSG tab should open
<img width="595" height="335" alt="image" src="https://github.com/user-attachments/assets/0b17315c-bba1-4ad4-a763-487d318eb32a" />

8. Enter a meaningful message into the `COMMIT_EDITMSG` editor and save with `Ctrl-s`, the close the tab by click on the `X`
<img width="595" height="271" alt="image" src="https://github.com/user-attachments/assets/f7a8f43b-92be-4aba-a2e2-6bc833bd552e" />

9. In the summary of the pull-request you're about to create, you will see that your `ops` branch is to be merged into the `main` branch of your fork.  Click the `Create` button to complete creation of the pull-request
<img width="401" height="430" alt="image" src="https://github.com/user-attachments/assets/c183facf-006a-4d9d-8d44-1085012891c6" />

10. A tab with a summary of your pull-request will open.  Keep this tab open, you'll use it later.
<img width="1064" height="637" alt="image" src="https://github.com/user-attachments/assets/7fb7a782-e741-426e-80d0-f141ea5c8fb5" />

11. In the EASeJ UI, click on the hamburger menu (top-left), and choose the `Config validations` menu option.
<img width="242" height="377" alt="image" src="https://github.com/user-attachments/assets/26db9915-5e5e-4143-b89f-27d37df184e1" />

12. You will see a config validation build summary.  You can click on it to view details.
<img width="593" height="244" alt="image" src="https://github.com/user-attachments/assets/fd3d3d45-39c3-42d5-a5ad-9fcced196710" />


## Merge pull-request to deploy to staging - merge PR, view deployment job, see results

You've successful contributed the configuration update.  Next it will be merged into the main branch to start the staging deployment. 

1. When the config validation build has completed successfully, go to the VS Code instances for `mod-resorts-cfg` and in the Pull Request tab, click `Merge Pull Request`
<img width="592" height="353" alt="image" src="https://github.com/user-attachments/assets/a421b1b6-c52c-4dfa-bdf6-8239c59bb829" />

2. A summary of your merge commit will appear.  click the `Create Merge Commit` button to complete the merge. Completion of the merge will start the deployment to staging
<img width="593" height="260" alt="image" src="https://github.com/user-attachments/assets/72476b2f-bf74-4087-a621-9bcb7f6835c3" />

3. To view the deployment job, go to the EASeJ Dashboard UI and scroll down to `Deployment jobs`.  Select the `Staging` option to see a summary of staging deployments.  A blue bar indicates a deployment in progress, and a green bar indicates a completed deployment.  You can hover over the base to see a summary and click on the bar to view details.
<img width="725" height="273" alt="image" src="https://github.com/user-attachments/assets/803c671a-5a1a-4275-a94a-936ca18a6ca7" />

## Validate application working in staging

1. Once the deployment job has completed, scroll up in the EASeJ Dashboard UI to view the environments.  You will see that the application is running in staging.  
<img width="836" height="159" alt="image" src="https://github.com/user-attachments/assets/d16376e5-b167-4678-a840-e4fab9bef9ea" />

2. The summary shows the Release Build that's running, the Deployment job that performed the deployment, the number of instances (and max configured), and the status. Click on `View environment ->` to open the envrionment details page
<img width="594" height="215" alt="image" src="https://github.com/user-attachments/assets/0bc35ff6-fc18-4e99-82ff-0325118078cd" />

3. In the environment details page, you can see each intances that's running and the logs from those instances.  You can perform diagnostics (capture server dumps and trace logs), you can view integrations (these are connectivity to external logs/monitoring, Db2, MQ, etc), and lastly, initiate further actions.  Click on the `Actions` menu to see the options, then choose `Open application`
<img width="813" height="272" alt="image" src="https://github.com/user-attachments/assets/9675e70c-d0ec-42b2-aa58-6dcaf20d9ed5" />

4. You will see a new browser tab where the web application is loaded for you to try it out
<img width="1473" height="604" alt="image" src="https://github.com/user-attachments/assets/40f2bef4-d3dc-46a4-b3f3-1f8fc946b9ec" />

You've successfully deployed and validated the application in staging.  This completes the core part of the labs.  There are two bunus modules for you to try if you have time.

# Bonus: capture diagnostics

Some times if you have an issue and need to diagnose it, or engage with IBM Support, you might need to capture a server dump or diagnostics trace.  EASeJ has built-in support for both.  It also manages the resulting artefacts for you so you can download them when required.  Artefacts are retained for 1 month before being cleaned up.

## Create a server dump

1. From the Staging environment tile in the EASeJ Dashboard UI, select `View environment ->`
<img width="598" height="216" alt="image" src="https://github.com/user-attachments/assets/5a7c29c0-fd9b-4951-8dcd-a2a97b680b86" />

2. On the environment details page you can choose which instances to create a server dump from.  You probably only have one instance so it's automatically chosen.  Click `Start diagnostics`
<img width="792" height="237" alt="image" src="https://github.com/user-attachments/assets/d81acb87-5a3a-4e42-bed4-2470b65b12b9" />

3. In the resulting pop-up, choose `Server dump` followed by `Start`
<img width="472" height="480" alt="image" src="https://github.com/user-attachments/assets/aba4e510-2ed4-49e7-8204-b6965dd1cfa9" />

4. You will see a notification to say the server dump has started
<img width="342" height="167" alt="image" src="https://github.com/user-attachments/assets/326c8f75-0fd6-4f25-aaa6-1518edcc293e" />

5. Select the `Diagnostics` tab to view captured server dumps and traces.  These are displayed in a tables where you should see the server dump you just captured.  This tables allow you to download or delete the diagnostics.
<img width="746" height="263" alt="image" src="https://github.com/user-attachments/assets/affb5a45-43e4-4ae3-bcca-63ea94cfb08b" />

## Capture trace for the Web container

1. From the Staging environment tile in the EASeJ Dashboard UI, select `View environment ->`
<img width="598" height="216" alt="image" src="https://github.com/user-attachments/assets/5a7c29c0-fd9b-4951-8dcd-a2a97b680b86" />

2. On the environment details page you can choose which instances to create a diagnostics trace from.  You probably only have one instance so it's automatically chosen.  Click `Start diagnostics`
<img width="792" height="237" alt="image" src="https://github.com/user-attachments/assets/388c84b7-d344-4f8c-9515-124399ea08b8" />

3. In the resulting pop-up, choose `Diagnostics trace` followed by `Start`
<img width="471" height="477" alt="image" src="https://github.com/user-attachments/assets/8b9f7d43-ea6a-4a76-811b-5313af932d7b" />

4. You now need to tell EASeJ what to trace.  Copy and paste the following into the `Trace specifications` field and click `Start`
```
*=info:com.ibm.ws.webcontainer*=all
```
<img width="435" height="445" alt="image" src="https://github.com/user-attachments/assets/bc3b3c9d-32f3-4d16-b937-d1085e5e69e0" />

5. You will see a notification to say that trace has started and also an information bar allowing you to stop the trace
<img width="827" height="170" alt="image" src="https://github.com/user-attachments/assets/dd81529a-7cfc-4942-9289-93ee065c26ed" />

6. Click on the `Diagnostics` tab and choose `Diagnostics trace`.  This will show the table summarizing all diagnostics trace you've captured.  You will see a row with status `Running` to indicate the trace is on progress.  You also have an action in the table to stop the trace.  Click the `stop` action.
<img width="870" height="305" alt="image" src="https://github.com/user-attachments/assets/c395836d-dc71-4d7e-8c0f-31192fa28331" />

7. You will see a notification to say Trace has been successfully stopped, and the table will show that you can now download or delete the captured trace
<img width="866" height="307" alt="image" src="https://github.com/user-attachments/assets/e50b8305-eee1-4ef7-b6d0-0449c01dd794" />


# Bonus 2: deploy to production

From what you learnt when deploying a release build to staging, so if you can work out how to deploy the same (or a different) release to the production environment. 

Hint: you can follow exactly the same steps, but if you want some instructions, view the `Deploy to production` Action in the staging environment details page.


# Party like it's 1999!

# Bonus - server dump, trace log

