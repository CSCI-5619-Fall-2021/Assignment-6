# Assignment 6: User Interfaces in Babylon.js

**Due: Thursday, December 16, 10:00pm CDT**

The purpose of this assignment is to gain experience in designing and implementing graphical user interfaces using Babylon.js and WebXR .  This is an **optional bonus** assignment.  If you choose to complete this assignment, your lowest score from the previous six assignments will be dropped and replaced with this one.  If you receive a lower score on this assignment, it will not be counted against you.

## Submission Information

You should fill out this information before submitting your assignment.  Make sure to document the name and source of any third party assets such as 3D models, textures, or any other content used that was not solely written by you.  Include sufficient detail for the instructor or TA to easily find them, such as asset store or download links.

Name: 

UMN Email:

Build URL:

Third Party Assets:

Custom GUI Instructions:

## Rubric

Graded out of 20 points.  

1. Add at least six mesh objects to your environment. (1)
2. Implement selection and de-selection using the laser pointer. Make sure to provide a visual indicator for the currently selected object. (1)
3. Create a GUI plane that is attached to the controller held in the user's non-dominant hand. Make sure to position the plane so that it is comfortable for the user to view. (2)
4. Add a [ColorPicker](https://doc.babylonjs.com/divingDeeper/gui/gui#colorpicker) to the handheld GUI. (2)
5. The handheld GUI should remain hidden when no object is currently selected.  When the user selects an object, the GUI panel should be made visible, and the value of the ColorPicker should be set the object's current material color. (2)
6. Use the ColorPicker to set the material color of the currently selected object. The material should be modified in real-time as the user changes the currently selected color. (2)
7. Create your own custom spatial GUI! You are free to design any type of user interface that you want. However, the GUI should contain at least five distinct types of interactive controls. (Non-interactive controls such as a static text block do not count.) You can find a list of control types in the [Babylon documentation](https://doc.babylonjs.com/divingDeeper/gui/gui).   You can use both 2D and 3D controls, and you can split them up among one or more GUI planes as appropriate. (1 point per control type, 5 points max)
8. Link the GUI controls to perform useful functions such as object manipulation, locomotion, or other 3D tasks. Creativity is encouraged! Again, you are free to implement any type of object manipulation that you want. However, make sure to include instructions for using your custom GUI in the documentation above. (1 point per control type, 5 points max)

Make sure to document all third party assets. ***Be aware that points will be deducted for using third party assets that are not properly documented.***

## Submission

You will need to check out and submit the project through GitHub classroom.  The project folder should contain just the additions to the sample project that are needed to implement the project.  Do not add extra files, and do not remove the `.gitignore` file (we do not want the "node_modules" directory in your repository.)

**Do not change the names** of the existing files.  The TA needs to be able to test your program as follows:

1. cd into the directory and run ```npm install```
2. start a local web server and compile by running ```npm run start``` and pointing the browser at your ```index.html```

Please test that your submission meets these requirements.  For example, after you check in your final version of the assignment to GitHub, check it out again to a new directory and make sure everything builds and runs correctly.

## Local Development 

After checking out the project, you need to initialize by pulling the dependencies with:

```
npm install
```

After that, you can compile and run a server with:

```
npm run start
```

Under the hood, we are using the `npx` command to both build the project (with webpack) and run a local http webserver on your machine.  The included ```package.json``` file is set up to do this automatically.  You do not have to run ```tsc``` to compile the .js files from the .ts files;  ```npx``` builds them on the fly as part of running webpack.

You can run the program by pointing your web browser at ```http://localhost:8080```.

To connect from your Oculus Quest, you can use [ngrok](https://ngrok.com/) to redirect a public IP address to your local machine.

## License

Material for [CSCI 5619 Fall 2021](https://canvas.umn.edu/courses/268490) by [Evan Suma Rosenberg](https://illusioneering.umn.edu/) is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

The intent of choosing CC BY-NC-SA 4.0 is to allow individuals and instructors at non-profit entities to use this content.  This includes not-for-profit schools (K-12 and post-secondary). For-profit entities (or people creating courses for those sites) may not use this content without permission (this includes, but is not limited to, for-profit schools and universities and commercial education sites such as Coursera, Udacity, LinkedIn Learning, and other similar sites).   

## Acknowledgments

This assignment was partially based upon content from the [3D User Interfaces Fall 2020](https://github.blairmacintyre.me/3dui-class-f20) course by Blair MacIntyre.



