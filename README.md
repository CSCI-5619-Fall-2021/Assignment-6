# Assignment 6: User Interfaces in Babylon.js

**Due: Thursday, December 16, 10:00pm CDT**

The purpose of this assignment is to gain experience in designing and implementing graphical user interfaces using Babylon.js and WebXR .  This is an **optional bonus** assignment.  If you choose to complete this assignment, your lowest score from the previous assignments will be dropped and replaced with this one.  If you receive a lower score on this assignment, it will not be counted against you.

## Submission Information

You should fill out this information before submitting your assignment.  Make sure to document the name and source of any third party assets such as 3D models, textures, or any other content used that was not solely written by you.  Include sufficient detail for the instructor or TA to easily find them, such as asset store or download links.

Name: 

UMN Email:

Build URL:

Third Party Assets:

Custom GUI Description:

## Prerequisites

To work with this code, you will need to install [Node.js](https://nodejs.org/en/).

The instructor is using [Visual Studio Code](https://code.visualstudio.com/).  However, you can use any code or text editor.

## Getting Started

The code implements the general structure that we reviewed in lecture, including basic scene creation, WebXR setup, polling for controller input, grabbing objects, and simple virtual locomotion. 

You set up the initial project by pulling the dependencies from npm with: 

```
npm install
```

After that, you can compile and run a server with:
```
npm run start
```

You can run the sample by pointing your web browser at ```http://localhost:8080```.  

To connect from your Oculus Quest, you can use [ngrok](https://ngrok.com/) to redirect a public IP address to your local machine. Download the ngrok executable, follow the instructions to set up your authtoken, and then run the following command:

```
ngrok http http://localhost:8080
```

## Creating Babylon GUIs

There are two methods for creating spatial user interfaces in Babylon.  The standard [Babylon GUI](https://doc.babylonjs.com/divingDeeper/gui/gui) works similarly Unity.  First, you create a plane with a dynamic texture.  Then, you can add a variety of 2D controls to the texture, and position the plane in 3D space.  A simple example has been provided in the code.

The second method uses a specialized [Babylon 3D GUI](https://doc.babylonjs.com/divingDeeper/gui/gui3D) library.  In this method, you create a `GUI3DManager` and then can add buttons directly as 3D objects in your scene.  The manager provides a variety of panels to assist with 3D spatial layouts; however, this library is limited only to 3D buttons, and it does not provide the wide assortment of controls present in the standard GUI.  

There are extensive tutorials with code samples available in the Babylon online documentation. In this assignment, you will be expected to read this documentation on your own and then create your own custom GUI.  Note that the code samples use the prefix `BABYLON.GUI` when creating new objects, but you should remove that part in your code and then add an import statement at the top of the file instead.

## Rubric

Graded out of 20 points.  

1. Replace the default virtual environment with a virtual scene using third party assets.  You can use [UnityGLTF](https://github.com/KhronosGroup/UnityGLTF) to export assets from Unity.  If you are running Windows, there is a prebuilt Unity package posted on Canvas that you can import into your project (under Assets->Import Package).  For platforms other than Windows, you will need to download the source from GitHub and compile the C# module manually.  (6)

2. Make at least four objects in your virtual scene grabbable.  (4)

3. Create your own custom spatial interfaces using the Babylon GUI! You are free to design any type of user interface that you want, and you can use both of the GUI creation methods described above.  Your project should contain at least **five distinct types** of interactive controls. Non-interactive controls such as a static text block do not count.  (2 points per control type, 10 points max)

4. Add event handlers to five GUI controls that perform useful functions such as object manipulation, locomotion, or other 3D tasks. You are free to implement any type of object manipulation that you want. Creativity is encouraged!  However, make sure to include a description of your custom GUI functions in the readme file.  (2 point per control, 10 points max)
   *Hint: you will need to add an observable to your controls to achieve this.  For example:*

   ```
   exampleButton.onPointerDownObservable.add(() => {
               Logger.Log("Hello world!");
           });
   ```

Make sure to document all third party assets. ***Be aware that points will be deducted for using third party assets that are not properly documented.***

## Submission

You will need to check out and submit the project through GitHub classroom.  The project folder should contain just the additions to the sample project that are needed to implement the project.  Do not add extra files, and do not remove the `.gitignore` file (we do not want the "node_modules" directory in your repository.)

**Do not change the names** of the existing files.  The TA needs to be able to test your program as follows:

1. cd into the directory and run ```npm install```
2. start a local web server and compile by running ```npm run start``` and pointing the browser at your ```index.html```

Please test that your submission meets these requirements.  For example, after you check in your final version of the assignment to GitHub, check it out again to a new directory and make sure everything builds and runs correctly.

## License

Material for [CSCI 5619 Fall 2021](https://canvas.umn.edu/courses/268490) by [Evan Suma Rosenberg](https://illusioneering.umn.edu/) is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

The intent of choosing CC BY-NC-SA 4.0 is to allow individuals and instructors at non-profit entities to use this content.  This includes not-for-profit schools (K-12 and post-secondary). For-profit entities (or people creating courses for those sites) may not use this content without permission (this includes, but is not limited to, for-profit schools and universities and commercial education sites such as Coursera, Udacity, LinkedIn Learning, and other similar sites).   
