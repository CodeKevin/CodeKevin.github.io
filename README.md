# iOS Develope Tips
## Issues
### 1.If found images of Library not found. solve:Embedded Binaries.
### 2.Two Mac A and B,A can upload app to store successfully,but B cannot.
### slove:You should use Apple developer account to login in and download the app Distribution .mobileprovision on B mac,
### then,double tap this file.Next,export the .p12 file from A mac to B,and double tap p.12 on B mac.Everything will be OK.

### 1.If found images of Library not found. solve:Embedded Binaries.
## Cocoapods tips
### 1.Pod common
    + cache         Manipulate the CocoaPods cache
    + deintegrate   Deintegrate CocoaPods from your project
    + env           Display pod environment
    + init          Generate a Podfile for the current directory
    + install       Install project dependencies according to versions from a Podfile.lock
    + ipc           Inter-process communication
    + lib           Develop pods
    + list          List pods
    + outdated      Show outdated project dependencies
    + plugins       Show available CocoaPods plugins
    + repo          Manage spec-repositories
    + search        Search for pods
    + setup         Setup the CocoaPods environment
    + spec          Manage pod specs
    + trunk         Interact with the CocoaPods API (e.g. publishing new specs)
    + try           Try a Pod!
    + update        Update outdated project dependencies and create new Podfile.lock
### 2.Create a pod lib (Private)
#### 1.create lib first project
    pod lib create LIB_NAME
#### 2.When project is created,you should replace ReplaceMe.m by your files.
#### 3.Modfiy LIB_NAME.podspec.(summary,homepage,description,source...)
#### 4.Create git repo private,upload your lib to this repo.
#### 5.update & liblint
    pod update
    pod lib lint 
#### 6.Local lib push remote origin master & you can make tag version
#### 7.spec lint
    pod spec lint
#### 8.Make a pod repo on git.
#### 9.pod add & push
    pod repo add POD_REPO_NAME POD_GIT_URL
    pod repo push POD_REPO_NAME SPEC_NAME.podspec
#### 10.Success.You can use podlib in project.
#### 11.Write cocoapods source & your custom spec in .podfile.
#### 12.If lib display multiple,you should pod 'LIB_NAME',:git=>'SOURCE_URL' 
## Git tips
### 1.remove remote repo file or dir,local file will lose git record. 
    git rm -r --cache (file or path)
### 2.ignore check specific file or path
    git update-index --assume-unchanged (file or path)
