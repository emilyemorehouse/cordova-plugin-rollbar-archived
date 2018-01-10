Rollbar Cordova Plugin
=======================

PhoneGap / Cordova plugin for using the Rollbar service. Currently supports Android and iOS allowing for capturing native exceptions that occur outside the context of the Web View (i.e. native crashes).

For tracking within your Web View, see [the Rollbar plugin for Angular](https://github.com/tandibar/ng-rollbar).

Rollbar
--------
This plugin requires a Rollbar account. Sign up for your free Rollbar account [here](https://rollbar.com/).

### Installation ###
#### Stable ####
You can install the plugin by running the following command.
```
cordova plugin add cordova-plugin-rollbar --variable ROLLBAR_ACCESS_TOKEN="<ROLLBAR_ACCESS_TOKEN>" --variable ROLLBAR_ENVIRONMENT="<ROLLBAR_ENVIRONMENT>"
```

If you're using Cordova 7+, use the following command:
```
cordova plugin add cordova-plugin-rollbar --variable ROLLBAR_ACCESS_TOKEN="<ROLLBAR_ACCESS_TOKEN>" --variable ROLLBAR_ENVIRONMENT="<ROLLBAR_ENVIRONMENT>" --nofetch
```

#### Bleeding edge ####
To install the most recent version in development, use:

```
cordova plugin add https://github.com/emilyemorehouse/cordova-plugin-rollbar.git --variable ROLLBAR_ACCESS_TOKEN="<ROLLBAR_ACCESS_TOKEN>" --variable ROLLBAR_ENVIRONMENT="<ROLLBAR_ENVIRONMENT>"
```

If you're using Cordova 7+, use the following command:

```
cordova plugin add https://github.com/emilyemorehouse/cordova-plugin-rollbar.git --variable ROLLBAR_ACCESS_TOKEN="<ROLLBAR_ACCESS_TOKEN>" --variable ROLLBAR_ENVIRONMENT="<ROLLBAR_ENVIRONMENT>" --nofetch
```

### Usage ###
#### Initialization ####
After the device is ready, call the following line of code to initialize the Rollbar plugin. Note that the token and environment are pulled form the plugin variables.

```
window.cordova.plugins.Rollbar.init();
```

There are many ways to wait until the device ready event has fired, but here is one example:

```
$ionicPlatform.ready(function() {
    window.cordova.plugins.Rollbar.init();
}
```

#### Debugging ####
On iOS, there is a helper method to simulate a crash. To do so, simply call:
```
window.cordova.plugins.Rollbar.simulateCrash();
```


### Supported Platforms ###

- Android
- iOS

### Notes ###
Currently in development, we welcome PR's and other fixes. Hope to have it production ready soon.

### Authors ###
* Shawn Jackson (Twitter: @DesignLimbo Blog: http://designlimbo.com)
* Jason Jarrett (Twitter: @staxmanade Blog: http://staxmanade.com)

### Special Thanks ###
* Halkeye (https://github.com/halkeye)

### License ###
Apache 2.0
