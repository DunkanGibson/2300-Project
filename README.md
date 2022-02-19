# CITC-2300 PROJECT TEAM 3 - Alpha Team
This repository is the workspace for the CITC app for RSCC

## Reminder
Make sure your master branch is up to date before creating your clone to ensure you're not editing something with old code.
If your app is not running using the VPS IP address, contact Mike to get the server up and running again, or to get instructions on how to do it yourself.

## To-Do List
- Initialize functionality of the Call button.
- Initialize functionality of the Email button.
- Write report on debugging, added features, and functionality of the app.

## Idea List for To-Do List
- Dark-mode switch at top right of app screen.
- Implement GitHub button to replace Skype button.
- Replace icons with missing icon images.
- Debloat app files ... Probably not.

## Code changes that need to be explained in more detail
```javascript

#Original

task cdvPrintProps << {
    println('cdvCompileSdkVersion=' + cdvCompileSdkVersion)
    println('cdvBuildToolsVersion=' + cdvBuildToolsVersion)
    println('cdvVersionCode=' + cdvVersionCode)
    println('cdvVersionCodeForceAbiDigit=' + cdvVersionCodeForceAbiDigit)
    println('cdvMinSdkVersion=' + cdvMinSdkVersion)
    println('cdvBuildMultipleApks=' + cdvBuildMultipleApks)
    println('cdvReleaseSigningPropertiesFile=' + cdvReleaseSigningPropertiesFile)
    println('cdvDebugSigningPropertiesFile=' + cdvDebugSigningPropertiesFile)
    println('cdvBuildArch=' + cdvBuildArch)
    println('computedVersionCode=' + android.defaultConfig.versionCode)
    android.productFlavors.each { flavor ->
        println('computed' + flavor.name.capitalize() + 'VersionCode=' + flavor.versionCode)
    }   
}

#Changed-to-debug

task cdvPrintProps {
doLast {
    println('cdvCompileSdkVersion=' + cdvCompileSdkVersion)
    println('cdvBuildToolsVersion=' + cdvBuildToolsVersion)
    println('cdvVersionCode=' + cdvVersionCode)
    println('cdvVersionCodeForceAbiDigit=' + cdvVersionCodeForceAbiDigit)
    println('cdvMinSdkVersion=' + cdvMinSdkVersion)
    println('cdvBuildMultipleApks=' + cdvBuildMultipleApks)
    println('cdvReleaseSigningPropertiesFile=' + cdvReleaseSigningPropertiesFile)
    println('cdvDebugSigningPropertiesFile=' + cdvDebugSigningPropertiesFile)
    println('cdvBuildArch=' + cdvBuildArch)
    println('computedVersionCode=' + android.defaultConfig.versionCode)
    android.productFlavors.each { flavor ->
        println('computed' + flavor.name.capitalize() + 'VersionCode=' + flavor.versionCode)
        }
    }
}
```