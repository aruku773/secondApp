## QumuV8 - Qumu SDK




## Usage

**Development Environment**

> Sample application pod file that uses qumu-sdk pod in development environment
```ruby
platform :ios, '8.0'
use_frameworks!
target 'TestApp' do
pod 'MBProgressHUD'
#This installs pod using code from local folder. Using local folder you can do the hot edits to the ios-sdk project
pod 'qumu-sdk' , :path => '~/Documents/WorkArea/ios-sdk'
#This installs pod fetching code from remote repo
#pod 'qumu-sdk' , :git => 'https://INTERNAL_REPO_URL/ios-sdk.git', :branch => 'develop'
end
```

- [Complete Documentation](https://confluence.qumu.com/pages/viewpage.action?title=Private+Pods&spaceKey=mobile)


## Note

- [x] Always create a folder when a new group is created in Xcode to maintain folder structure in pods


### QumuSDK Swift 2.3 migration steps

1. Install CocoaPods 1.1.0-rc.2 with the below command

   ```sh 
    $ gem install cocoapods --pre 

```

2. Install pods

  ```sh  
   $ pod install 

```

3. Open workspace and change Target build settings to use legacy swift version

   Target->BuildSettings ->Use legacy Swift Language Version = YES

4. Edit->Convert->To Current Swift Syntax-> Convert to Swift 2.3

5. Changes will be made in ServerTrustPolicy.swift . Accept those changes and save
