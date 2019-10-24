# image_labeling

We need more data to train the model, so here's some instructions on how to label it. Inside the img folder I'll place the photos in groups of 25 to make it easy to manage.

## Setting Up Yolo_mark

1. Go to [OpenCV](https://opencv.org/releases/) and download the 3.4.7 version for Windows
	- Once downloaded, run the .exe
	- Extract to C:/ or somewhere you will remember.
2. If not already installed, download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/)
3. Download [Yolo_mark](https://github.com/AlexeyAB/Yolo_mark)
	- Follow the directions in the Yolo_mark github README, here is where you will need the OpenCV directory.
4. Copy obj.names and obj.data from this github and paste them into Yolo_mark/x64/Release/Data
	- Yes, replace them
5. Copy images to label into Yolo_mark/x64/Release/Data/img
	- Make sure to delete the original images first.

## Adding OpenCV to Path

1. Search for "Edit environment variables"/
2. Click the "Environment Variables ..." button.
3. Under "System Variables" find the row where the variable is named "Path". Select it and click edit.
4. A new window should appear, click "New" on the right hand side.
5. Either type in directory or hit browse and find it.
	- Should be similar to C:\OpenCV\build\x64

> If it still doesn't run change Path variable above to C:\OpenCV\build\x64\vc14\bin\

## Using Yolo_mark

There should be a windows command script named yolo_mark.cmd, double click to run the program. If you receive an error saying "could not find opencv_worldxxx" then you did not add OpenCV to your Path correctly. There are two sliders at the top, the first will change the photo you are currently looking at, the second changes the label. To label an object, select the correct label at the top, then draw a box around it using LMB. RMB will allow you to move the box, and press r to delete the selected box. Press h in the program to see additional options if needed.

## Pushing to git

Once finished labeling images:
1. Perform a pull from github to make sure your folder is up to date.
1. Copy images and .txt files back to original folder in git.
2. Copy train.txt to the same folder as above.
	- train.txt found at /Yolo_mark/x64/Release/data
3. Push to data to github.

> If you have limited experience with git, just google `git no deep shit` and go to the first link.
