# Parallax

## What is it

This app uses the depth data captured on 2-camera phones to mask a photo according to depth. We use this to do two different things. Firstly, we apply filters to photos (blur, spotlight, color) according to depth. Secondly, we use the distinct layers created by depth masking to project the image into 3D space, and use the Iphone's truedepth front facing sensor for pupil and face tracking, in order to give the illusion of depth. 

While that was our initial idea, due to our limited (read: no) prior usage of Swift, Xcode, and Unity, we faced considerable trouble while trying to implement our idea. In the end we have two seperate apps, built following two seperate tutorials. The first, built in Xcode using Swift creates masks with the depth data and applies filters to the masks. The second, built using Unity, shows a monocular 3D seen, using Unity's ARkit for face tracking.

Tom built the Swift depth app following this tutorial: https://www.raywenderlich.com/314-image-depth-maps-tutorial-for-ios-getting-started

Gabe built the 3D Unity app following these two tutorials: http://www.anxious-bored.com/blog/2018/2/25/theparallaxview-illusion-of-depth-by-3d-head-tracking-on-iphone-x

https://www.lynda.com/Unity-3D-tutorials/Unity-basics/96677/109238-4.html

** due to file size limits on git, when running the unity portion of this project locally you must first open the zip file `/iOSBuild7/Libraries/libil2cpp.a.zip`
You must also download and place the file located at this link https://www.dropbox.com/s/yh3xvu98ev0e3uz/libiPhone-lib.a?dl=0 in the `/iOSBuild7/Libraries` directory

## What We Learned

##### Tom
I learned the semantics of Swift, as well as how to develop and debug using Xcode, including building a UI with the visual manifests. On top of that, I also learned a lot about the way images are stored in IOS and how to perform pixel-wise operations on them. 

##### Gabe
I learned how to use Unity and UnityARKit to a build and run an application on iOS that tracks the eye positioning of the user to create a perspective effect when viewing images and other 3D models like boxes and spheres. I also learned the basics of creating Scenes in Unity using camera position and lighting tools. I utilize simple shaders on the surfaces of 3D objects to create a sheen effect based on lighting position.

## How It Relates To Project Ideas
With over 90 million people in the US alone owning IOS devices, we felt that learning the principles of IOS development would be a powerful tool for any consumer (or even enterprise) facing project. In the same vein, with ARkit being one of the most cutting edge tools for IOS development, we felt that working on a Unity app would be a good way to get familiar with this new technology.

## What Didn't Work

On the Swift side of things, we had extreme difficulty making a Unity scene within the app, such that the entire app wasn't a unity project. On the Unity side we had difficulties creating new objects in the Eye Tracker Scene because of camera and light issues which led us to reference the second Unity tutorial. We also experienced issues trying to get the eye tracking to work in portrait mode, so currently on landscape is compatible.
