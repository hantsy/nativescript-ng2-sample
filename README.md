#Getting Started

##Installation

Assume you have installed the latest NodeJS into your system.

Install **NativeScript** via NPM.

    npm install -g nativescript

After it is installed, open your terminal and verify the installation.

    tns --version
    
You could see the following info.

    >tns --version
    >2.0.1
    
    
##Create a NativeScript project

Execute `tns create` line to create a project.

    tns create ns-sample --ng    
    
**ns-sample** is the project name. **-ng** tell `tns` command to generate the project and use **Angular** integration. It also use **Typescript** by default.

Enter the generated project folder.

    cd ns-sample
   
You will see the following project structure.

    +--app
    +--hooks
    +--node_modules
    +--platforms
     --package.json
     --references.d.ts
     --tsconfig.json
     
**app** is the app resource folder we will develop for this app.
**hooks** includes some scripts apply to the build lifecycle.
**node_modules** includes the NPM dependencies defined in the **package.json**.
**platform** will place the Android and IOS platform building codes.
**tsconfig.json** is the TypeScript configuration file.

##Run the project

Add platform support into this project.

    tns platform add ios

For Android, use the following command line alternatively.

    tns platform add android
    
In order to build the app successfully, you have to install required software to build the app successfully. Please read the [NativeScript Setup](http://docs.nativescript.org/angular/start/quick-setup.html) for more details.

If you are using Mac OS system, execute command `tns run ios` to run this app in a real device .

For Android platform, the following command will run the this app on a real Android device or a Genymotion virtual machine. Before run this command, please make sure there is a device connected or a Genymotion virtual device is started. 

    tns run android
 
It will prepare the android building environment and build the app package for Android platform, and finally run it on the target device.

![hello-tns](hello-tns.png)
    
If you want to run it in an Android emulator, append a **--emulator** to the above command.    
