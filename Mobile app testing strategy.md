# Mobile app testing strategy


This doc going to describe the fundamental testing strategy for mobile app on delivery point of view.

### Mobile Application testing covers following testing approaches and tools

- Functional testing
- Automation testing
- Performance testing
- Security testing
- Testing tools
- Application distribution
- Some of mobile based testing
- No network testing
- Kill/ minimise the application
- Clear the application data (Android)
- Upgrade scenarios
- API handlings & Error cases
- OS version & device resolution compatibility
- Rooted & Jail broken devices testing
- Token session
- Device date & time

1.1. Functional testing
As part of functional testing we cover the functionality of the application and make sure app meets the business requirements and mobility standards. We split the functional testing into deeper levels following are

a. Story Verification
Verify that the feature meets the Acceptance criteria of the story

b. SIT/ Regression Testing
Covering the overall functionality of the application before release to the production and make sure all the scenarios of the business requirement covered and no bugs leaked to the production

c. Sanity Testing
Testing the basic functionality of the application mostly on master build or every develop build (through automation)

d. Bug Verification
Verifying the defects as part of Bug life cycle

1.2. Automation Testing of Mobile application
For mobile app UI/Functional automation we are using following tools

Espresso (Android)
XCUITest (iOS)
Warning: We are not covering the following cases as part of automation, Will try to cover as much as possible in subsequent releases but not in the first release

Any native controls (Camera, Touch ID, Setting changes)
API Negative test cases (timeout, error, abort, etc..)
Data dependency cases (Different AWF combinations and flows) 

Note: Will be separate wiki doc for Automation framework and approach in detail

1.3.  Performance Testing
In terms of mobile app performance or non functional testing we cover the following aspects of the mobile behaviour based on our app usage

- Battery consumption
- CPU consumption
- Memory consumption
- Network data consumption
- Time to First Byte (Launch time)
- App crash rate

a. Battery Consumption
App should not consume too much battery of the phone

b. CPU consumption
App should not consume too much CPU usage of the phone while running or in background

c. Memory Consumption
App should not use too much disk space once after installing the app

d. Data Consumption
App should not use too much network data

e. Launch time
App should not take more than 2 sec to launch the app

f.  App crash rate
App crash rate should not be more than 1%

For performance testing we are using following tools to catch the above metrics
Android [FREE]:
Battery Historian (https://developer.android.com/topic/performance/power/battery-historian)

iOS [FREE]:
Instruments (https://help.apple.com/instruments/mac/current/)


1.4. Security Testing

     TBD about this topic but will be giving overview about PEN testing on mobile in below link

(https://github.com/tanprathan/MobileApp-Pentest-Cheatsheet)


1.5. Testing Tools

We are using different testing tools to test the mobile application on various aspects following are the some of the tools

a. Charles [PAID and FREE TRAIL]
Charles is a network monitoring tool which will be helpful on mocking, monitoring and interrupt the APIs to test the API layer of the application

b. Xcode [FREE]
Installing the build on real devices, Automation, Getting Crash Logs

c. Instruments [FREE]
To track the iOS app performance behaviour

d. adb [FREE]
To install the Android application and get the crash and logs of the application

e. Battery Historian [FREE]
To track the Android app performance behaviour

f. Postman [FEREE]
To check the APIs and Send the push notification to Android devices

g. Knuff [FREE]
To send the push notification to iOS devices 

1.6. Application distribution
Where to deploy the our development application is yet to be finalised, But the suggestions are

a. App centre [FREE/PAID]
App centre is Microsoft application deployment tool we can use the free version for just upload the app, it has paid version for build the apps and distribute.

b. Test Flight [FREE]
Test Flight is iOS beta testing deployment tool

c. App store
To deploy the iOS application to the production

d. Play store
To deploy the Android beta build and also production

