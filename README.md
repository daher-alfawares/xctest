# xctest
Creates a test matrix for xcode projects.

Typical usage in your script is to use something like this:

```    
    ./xctest -version
    ./xctest \
     -workspace MyApp.xcworkspace \
     -scheme MyApp \
     -devices "iPhone 6" "iPhone 7" \
     -os-list "10.3.1" \
     -slack-channel "#app-builds-channel" \
     -slack-message "Hello @john @emma pay attention!" \
     -slack-url https://hooks.slack.com/services/##########/###########/#######################
```

The list of -devices and -os-list are optional. The app will display what it defaults to when you don't provide a specific command.

```
$ ./xctest -version
```
Output:
```
xctest v1.0 by Daher Alfawares
```

You can get a list of command line switches by using -help.

```
$ ./xctest -help
```

Output:

```
Usage: xctest -[switch] value1 value2 ...

 +-----------------------------------------------------------+
 |options                                                    |
 +----------------+------------------------------------------+
 | switch         | description                              |
 +----------------+------------------------------------------+
 | -clean         | clean the project before building.       |
 | -devices       | overrides the list of devices.           |
 | -help          | produces the usage of this tool.         |
 | -os-list       | overrides the list of operating systems. |
 | -platform      | the platform. (default: iOS Simulator.   |
 | -scheme        | the scheme from your xcode project.      |
 | -sdk           | the sdk. (default: iphonesimulator).     |
 | -slack-channel | the name of the channel on slack.        |
 | -slack-message | the extra message to add to slack.       |
 | -slack-url     | the url to access your slack.            |
 | -verbose       | displays more output than usual.         |
 | -version       | displays the version of the tool.        |
 | -workspace     | the xcode workspace file.                |
 +----------------+------------------------------------------+
 ```
 
 
