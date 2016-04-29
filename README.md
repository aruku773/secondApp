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
