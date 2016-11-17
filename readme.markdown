# Qumu SDK Documentation

==================================

<!---
 Copy the generated  docset (com.qumu.QumuSDK.docset) to the following location and restart Xcode.
 
 ~/Library/Developer/Shared/Documentation/DocSets/-->

**QumuSDK** is a ios Objective-C SDK for implementing RESTFul web services for VCC 7.5 and traditional web services for VCC 7 and below. It has all the APIs to make accessing and modeling RESTFul/traditionals resources to respective DTOs.

## **Qumu SDK Integration**
Qumu SDK encapsulates the requirements for communicating with the typical Qumu VCC services used to present video content to a viewer. Any app intended to embed the VCC functionality has to integrate with the Qumu SDK to talk to VCC.


### **Configure SDK**
You will receive a folder named QumuSDK with the following files

1. libQumuSDK.a
2. include folder (with all the SDK headers)
3. SDK documentation


### **Steps to integrate**
1. Add libQumuSDK.a as a static library to your project.
2. Add the include folder with all the headers to your project.
3. Build your project.
￼

In some special cases, when you receive the SDK source code and you plan to integrate the QUMU SDK as dependency project, please follow the following steps.

**Step 1: Qumu SDK dependencies**

Qumu SDK has a dependency on the cocoa pod “DCKeyValueObjectMapping”. This can be referenced in 2 different ways.


1. If your project is set-up to use cocoa pods then add the following line to your podfile.
pod 'DCKeyValueObjectMapping'
2. If your project is not set-up to use cocoa pods then just add the “DCKeyValueObjectMapping” folder (present in the Pods folder of the SDK archive you received) to the Qumu SDK project.


**Step 2: Adding Qumu SDK to your project**

Add Qumu SDK as a dependency to your project.

1. Right clicking on your project in the Xcode navigator and “Add files to ...”.
2. Select the “QumuSDK.xcodeproj”
3. Add the Qumu SDK header path to the 'Header Search Paths' section of the
“Build Settings” tab of your target. Typically, you can find the sdk header path by building the Qumu SDK target and right clicking on the libQumuSDK.a and say show in finder which will point you to an include folder.
4. Add the “QumuSDK” to the “Target Dependencies” section of the “Build Phases” tab of your target.
5. Build your target.

### **Configure OAuth Client for VCC 7.5**
OAuth Client must be created for the client applications that will be accessing the VCC. To add an OAuth client, go to **adminportal** and on the left hand navigation bar and select User Management -> OAuth Clients. There a system wide list of Clients will be displayed. You will click the “plus” button to add a new Client and fill out the web form that is displayed.

## **SDK Setup**

* Include all the necessary SDK files.
* First configure the **QumuSDK** by call **initSDKWithConfigurationParams:** from **QUConfigurationManager** class.
* All the APIs related to VCC 7.5 or below can be access using below manager classes.



### **Managers**
| Class                    | Description             |
| -------------            |-------------            | 
| QUConfigurationManager        | To be used for all configuration related API’s of the SDK. | 
| QUEGCProgramManager        | To be used for all EGC related API’s of the SDK. | 
| QUProgramManager        | To be used for programs related API’s like EGC, program details, live broadcast, poll & survey, comment, playlist etc. | 
| QUSearchManager        | To be used for search and speech search related API’s. | 
| QUUserAccountManager        | To be used for User Account related API’s login, relogin, logout, get current user etc.| 
| QUViewerManager        | To be used for viewer related API’s like pods, channels, category etc. | 

