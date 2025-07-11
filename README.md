# Enterprise Application Service for Java TechXchange 2025 Lab

# Lab Structure

TODO: timing estimates

Source repos prepopulated with mod-resorts
Config repo prepopulated with Staging and Production environment yamls.

IBM Cloud Logs - Need cloud credits (no work for the people to do).  Monitoring is more problemmatic.  

0. Intro slides to EASeJ - 10m
0.1 Install EASeJ Tools - 10m - need to check if it will be feasible for us to install the night before
1. Getting IDs and Repositories - 10m
2. Configure Service Instance - 10m
3. Familiarize with the UI - WalkMe + anything not covered by WalkMe (use this to capture new WalkMe requirements) - 5m
4. Make an application change and test locally - Start VS Code, Dev Mode, code change, see results, run tests, etc - 10m
6. Create a pull-request to test in EASeJ - commit change, create PR, go see the build, view tests, etc.  - 10m
7. Merge pull-request to deliver, build, and test change - merge PR, go see the build, view test results, etc.
8. Update staging config and create pull-request to validate - copy the version, update yaml, commit change, create PR, view config validation
9. Merge pull-request to deploy to staging - merge PR, view deployment job, see results
10. Validate application working in staging - go to staging, see the instance, view the app.
(optional Production)
11. Update production config and create pull-request to validate - promote by copying version, update yaml, commit change, create PR, view config validation
8. Merge pull-request to deploy to production - merge PR, view deployment job, see results
9. Validate application working in production - go to production, see the instance, view the app.
11. Party like it's 1999!
12. Bonus - server dump, trace log
13. 
