# My Custom Build of Cesium for Unreal
This is a custom build of Cesium for Unreal that I'm using for an app that I'm working on.

Anyone is welcome to use it for any purpose; I have no stipulations on it's usage other than those presented by Cesium.

This build script:
  1. downloads unreal engine
  2. builds unreal engine
  3. zips unreal engine
  4. unzips unreal engine to a target directory
  5. downloads cesium for unreal
  6. modifies cesium for unreal
  7. builds cesium for unreal for windows
  8. builds cesium for unreal for android
  9. combines the windows and android build into one packaged plugin

The only modification made to the Cesium build is that PRIVATE_SQLITE is turned off, meaning that you can utilize their sqlite3 library in the entire Unreal Engine project with normal sqlite3 syntax.
If you also want to do this, you have to include the built sqlite3 library in your build.cs file, and also manually paste the header file for sqlite3 that is used by Cesium into your project's source folder.

If you read through the steps mentioned above, you'll notice an inefficiency in the Unreal Engine build/usage process. That's on purpose.
If you want to do this process the way that Cesium does it, you need that zip file, and an AWS S3 bucket.
I'll probably need to do something like that in the future, so this serves as my reference build for that.

Oh yeah, and the reason why this repository has an unintelligable name is not because I was trying to obscure it - it's due to a long paths constraint during the github checkout process.
For more info on that, read the comments in build-UnrealEngine-Win64-selfhosted.yml.
If anyone knows some way to fix that, please let me know - or fork this repo, I'll see it eventually!

- Tim
