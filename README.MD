## Development Instructions
* Always create branch from develop branch to work on your feature/request and raise a pull request to merge back to develop so that code can be reviewed.
* WIP in commit message means "Work in Progress"
* Custom folder : All the branding relted stuff resides in custom folders or classes with custom in their name

### Integrate QumuSDK as framework
* Add the QumuSDK framework to the project.
* Make sure to add QumuSDK.framework to your target embedded binaries from "General" tab of your target.
* Add the following dependencies to your Podfile
    * pod 'AlamofireObjectMapper'
    * pod 'AlamofireImage'

## Build Instructions
* Always make sure you select "Generic iOS Device" as the scheme while archiving
* 
### Build failure tips
* Issue 1: ERROR ITMS-90206: "Invalid Bundle. The bundle at 'Qu Capture.app/Frameworks/QumuSDK.framework' contains disallowed file 'Frameworks'."
```sh
Fix : Make the following change in the Build settings of the corresponding targets
• For main project (QuCapture) : Embedded Content Contains Swift Code to YES
• Custom Framework (QumuSDK) : Embedded Content Contains Swift Code to NO
• Custom Framework (QumuSDK) : Runpath Search Path = @executable_path/../../Frameworks

```

# Release Notes
### 1.0.0


***


### QumuSDK Swift 2.3 migration steps

1. Install CocoaPods 1.1.0-rc.2 with the below command

``` $ gem install cocoapods --pre```

2. Install pods

``` $ pod install```

3. Open workspace and change Target build settings to use legacy swift version

Target->BuildSettings ->Use legacy Swift Language Version = YES

4. Edit->Convert->To Current Swift Syntax-> Convert to Swift 2.3

5. Select projects XLActionController and DKImagePickerController

6. Accept changes suggested and save
