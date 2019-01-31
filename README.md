# iOS Develope Tips
## ISSUES
### 1.issues:image not found. solve:Embedded Binaries.
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
- First,pod lib create LIB_NAME
- When project is created,you should replace ReplaceMe.m by your files.
- Modfiy LIB_NAME.podspec.(summary,homepage,description,source...)
- Create git repo private,upload your lib to this repo.
- pod update
- pod lib lint 
- Local lib push remote origin master & you can make tag version
- pod spec lint
- Make a pod repo on git.
- pod repo add POD_REPO_NAME POD_GIT_URL
- pod repo push POD_REPO_NAME SPEC_NAME.podspec
- Success.You can use podlib in project.
- Write cocoapods source & your custom spec in .podfile.
- If lib display multiple,you should pod 'LIB_NAME',:git=>'SOURCE_URL' 
