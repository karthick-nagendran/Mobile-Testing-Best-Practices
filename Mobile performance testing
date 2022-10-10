# Mobile Performance Testing

What is performance testing?
Performance testing, a non-functional testing technique performed to determine the system parameters in terms of responsiveness and stability under the various workloads. Performance testing measures the quality attributes of the system, such as scalability, reliability, and resource usage.

What is mobile app performance testing?
Application performance testing on mobile is to measure CPU utilization, RAM memory consumption, Battery consumption, and Network utilization while the app is running on the foreground or in the background.

How it is different from server performance testing?
As you have seen the web-based or API performance testing more focused on workload, concurrency, and responsiveness of the system, Whereas mobile apps performance testing is more focused on how our application impacting device factors like CPU, Memory, Battery, etc.

So we have to think differently to achieve mobile app performance testing compare to web/API performance testing. So what is the difference?

1. No concurrency
We have to check, how our application behaves while running in the foreground and the background in a single device. There is no difference whether its 1 device or 10 devices. 

2. No workload
We can able to measure our app behavior precisely. Also, it's not in our control if the user opens 10 applications or 100 applications parallelly with our application, it’s OS issue, not our app issue.

What are the metrics capturing as part of mobile performance testing?
The following factors are measuring as part of Mobile performance testing.

CPU utilization
RAM  memory utilization
Battery consumption
Network  consumption
App startup Time
Frozen frames
Installer App footage size
App device memory consumption
How to capture the performance metrics?
Android
Android has an Android profile to capture most of the performance metrics.

 https://developer.android.com/studio/profile

iOS
Xcode has a quick peek view of the CPU utilization once we run the app open the "Show the Debug Navigator" navigator tab, It will provide an ample amount of information. For deeper analysis, we can use Instruments Application.

A good article about iOS performance testing.

https://medium.com/@phillfarrugia/xcode-instruments-measuring-launch-time-cpu-usage-memory-leaks-energy-impact-and-frame-rate-1caf8905079f

CPU Utilization

Improving CPU usage of the application will improve the faster and smoother experience also increasing battery life.

The impact of the CPU usage is more common when we have any background process like Syncing, Navigation, and running Application in the background. As of now, we don't any such process so we are good at this category. 

Android
Android developer page to illustrate about CPU utilization

https://developer.android.com/studio/profile/cpu-profiler

iOS
Xcode has a quick peek view of the CPU utilization once we run the app open the "Show the Debug Navigator" navigator tab, It will provide an ample amount of information. For deeper analysis, we can use Instruments Application

RAM  memory utilization

Memory management is a very important factor in the performance of the application. Both iOS and Android will terminate the application if an application consuming more than allotted memory. Memory allocation will be different between the devices.

Removing the unused objects is good practice will improve the performance and speed of the application.

Android
Android developer page to illustrate about RAM memory utilization

https://developer.android.com/studio/profile/memory-profiler

A good article about android memory concepts

https://stackoverflow.com/a/2299813/3929709

iOS
Xcode has a quick peek view of the CPU utilization once we run the app open the "Show the Debug Navigator" navigator tab, It will provide an ample amount of information. For deeper analysis, we can use Instruments Application.

Battery consumption

Battery consumption is the direct impact of CPU and RAM consumption of the application. 

Android
Android developer page to illustrate about battery consumption

https://developer.android.com/studio/profile/energy-profiler

Battery Historian is an Android native to tool to visualize the battery consumption

Android developer page to illustrate about Battery Historian

https://developer.android.com/topic/performance/power/battery-historian

iOS
Xcode has a quick peek view of the CPU utilization once we run the app open the "Show the Debug Navigator" navigator tab, It will provide an ample amount of information. For deeper analysis, we can use Instruments Application.

Network  consumption

How much data transferred and received by our application, It depends upon user usage of the application. Also, we want to make sure there is no unnecessary calls and sync operation made to the server, which gonna cause the hight data transfer rate.

Android
Android developer page to illustrate about Network consumption

https://developer.android.com/studio/profile/network-profiler

iOS
Xcode has a quick peek view of the CPU utilization once we run the app open the "Show the Debug Navigator" navigator tab, It will provide an ample amount of information. For deeper analysis, we can use Instruments Application.

App startup Time

Users expect apps to be responsive and fast to load. An app with a slow start time doesn’t meet this expectation and can be disappointing to users. This sort of poor experience may cause a user to rate our app poorly, or even abandon our app altogether.

Three types of states there at the start of the application

Cold start
Warm start
Hot start
Android
Android we use adb logcat tool to get the app starts numbers.

Android developer page to illustrate an app startup time

https://developer.android.com/topic/performance/vitals/launch-time

iOS
A good article about iOS startup time

https://medium.com/globant-mobile-studio-india/ios-app-launch-time-analysis-and-optimization-a219ee81447c

Frozen frames

Android
Android developer page to illustrate about Network consumption

https://developer.android.com/topic/performance/vitals/frozen

iOS
We user Instruments to measure the frozen frames in iOS

Installer App footage size

Article about installer app footage size

https://sweetpricing.com/blog/2017/02/average-app-file-size/

App device memory consumption

This category we are forcing on how the app constantly 

Scenarios for Performance Testing?
We don't have any specific scenario as such to measure the performance of the application, haven't said that we will be monitoring the memory, CPU, battery utilization for each screen of the application.

Performance Benchmarks metrics?
For memory, App lunchtime we will be using the 1.0.0 app performance metric as a baseline.

