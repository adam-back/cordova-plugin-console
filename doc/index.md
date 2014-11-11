<!---
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
-->

# org.apache.cordova.console

This plugin is meant to ensure that console.log() is as useful as it can be.
It adds additional function for iOS, Ubuntu, Windows Phone 8, and Windows 8. If
you are happy with how console.log() works for you, then you probably
don't need this plugin.

## Installation

    cordova plugin add org.apache.cordova.console
    
### Configuration
After installation, you will need to rebuild your platforms locally. Remove, then re-add the platforms (iOS, Android, etc.) using these commands in the terminal:
```
cordova platform rm ios
cordova platform add ios
```

### Usage
1. Add a console.log statement to your code.
1. Type `cordova prepare` in the terminal.
1. Open Xcode, then File > Open your project's Xcode file: `*.xcodeproj`.
1. Complete a clean by clicking Product > Clean.
1. Open the console by clicking View > Debug Area > Activate Console. You also may need to Show Console.
1. Press the play button in the upper-left hand corner to build the app. If build succeeds, you should see your `console.log` statments in the Xcode console.

### Android Quirks

On some platforms other than Android, console.log() will act on multiple
arguments, such as console.log("1", "2", "3"). However, Android will act only
on the first argument. Subsequent arguments to console.log() will be ignored.
This plugin is not the cause of that, it is a limitation of Android itself.
