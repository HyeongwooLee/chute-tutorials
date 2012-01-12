
Introduction
====

This tutorial will help you successfully set up the basic things that are required for
getting started with Chute.


Basic Setup
====

* Open Eclipse and create new Android project by selecting File->New->Android Project.
* Type the name of the project, it can be anything you like, I'll name it NewProject.

  ![alt text](/home/ola/newandroidproject.png)
  
* Select build target. I'll use Android 2.1 API Level 7.  
 
  ![alt text](/home/ola/selectbuildtarget.png)
  
* Add a package name. The package name I added is: com.android.newproject

  ![alt text](/home/ola/addpackagename.png)
  
* After successfully creating a new Android project, the next thing that needs to be done
  is adding the Chute SDK as a library project.
* Chute SDK project can be found and downloaded at [example link](https://github.com/chute/Chute-SDK).
* Select Project->Properties and add ChuteSDK as a library project.

  ![alt text](home/ola/projectproperties.png)
  
    
Android manifest setup
====

* Open the AndroidManifest.xml file 

* Add the following permissions:
 ```
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
    <uses-permission android:name="android.permission.GET_ACCOUNTS" />
    <uses-permission android:name="android.permission.WAKE_LOCK" />
 ```

* Register the activities:
 ```
    <activity
            android:name=".NewProjectActivity"
            android:label="@string/app_name" >
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>     
 ```
 
* Register the GCHttpService from ChuteSDK:
 ```
    <service android:name="com.chute.sdk.api.GCHttpService" >
        </service> 
 ```
 
* Register the AccountAuthenticatorActivity from ChuteSDK:
 ```
    <activity android:name="android.accounts.AccountAuthenticatorActivity" >
        </activity> 
 ```
 
 
  