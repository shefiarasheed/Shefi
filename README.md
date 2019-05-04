# NYTimes
NyTimes Popular

Completedfollowing 
Create API key from https://developer.nytimes.com/get-started 
and replace the key in the URL http://api.nytimes.com/svc/mostpopular/v2/viewed/{period}.json?api-key=sample-key.
This API return json response.

Done bellow things

1.Created an Android project
2.Created a recycleView with adapter to list the NY times polular
3.Set the duration as 7 in the URL
5.Created the Model class for the json response.
6.Call the API using retrofit to parse the result. 
7.Parse the Json result and display in recycleview as per requirement 
8.Used MVC pattern to develop this app.(Model view and controller strategy)
9.Implemeted Junittest. The testing implemented for checking the API key is valid or not
10.Used good Java coding pattern to implemet this app.
11.Implemented Espresso UI testing.The testing is implemeted  for validating matching the textview text values with constant String values.For testing this, 
Turn off animation on your test device, go to Settings > Developer Options and turn off all the following options under the "Drawing" section: 
Window animation scale
Transition animation scale
Animator duration scale
12.Scripts for Gradle,
Gradle Script 
######## To Build the project#####
buildscript {
    repositories {
        jcenter()
        google()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.4.0'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}
To build from command line --- gradlew installDebug

######### For Linting #########
gradlew lint

####### To run Instrumented unit test & code coverage ########
gradlew test



13.Scripts forFastline Script 
######## To Build the project#####

lane :slackbuild do
  gradle(task: "assembleRelease")
  slack(message: "Build Successful!")
  upload_to_slack()
end
command ---fastlane slackbuild


######### For Linting #########
fastlane run pod_lib_lint

####### To run Instrumented unit test & code coverage ########
fastlane tests


