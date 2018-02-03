# face_ripper
This proportionally grabs video frames from batches of mp4 videos and builds a faceset of your desired face.
It sorts by recognizing the number of faces in a picture AND by recognizing the faces you do, and do not want.

By the time you have run all these scripts you should be left with a folder containing thousands of jpgs.
Each jpg in this folder will be a picture with exactly one face.
The face in each jpg will be the face of the specific person you wanted extraced from your mp4 videos.

These scripts should be used in numerical order.
Each script's output is the next script's input.
It's a good idea to make a backup, zip copy of every script's output before proceeding to the next one.

Play with the scripts with directories containing small amounts of jpgs at first so you make sure everything
is grabbing and putting everything to, and from the places you want. The tops of the scrips are heavy with comments
about how the code works but the most challenging part of using them will probably be just getting all your paths
right.

Your MP4 videos should be 1080p if not higher. As of yet there is nothing in this repo that removes a low rez/
face shot far from the camera image. ALTHOUGH most small faces far from the camera WILL BE removed because a frame with
a face far away from the camera USUALLY has more than one face in the frame. Any frame>photo with more than one face
is automatically removed during the process. If you have a lot of footage of your target face going far from the camera,
lone in the frame you may want to edit those parts out of your MP4s before using here.

It's good to suppliment your faceset with photographs. This Firefox addon scrapes Google Image searches.
https://addons.mozilla.org/en-US/firefox/addon/google-images-downloader/
Be sure to open up this dir's download folder and delete all images below x size of KB.
Skip scripts numbered 1 and 2 and feed your images into script number 3.

This code does not crop the image to isolate the faces.

# Dependancies
These scripts are dependant on the face_recognition app by ageitgey here https://github.com/ageitgey/face_recognition

All dependancies required to run that (face_recognition module) are the depancies needed to be installed to run this. You're
best off scanning the issues tab on that repo when you run into problems instead of opening a new issue here.
So, go get face_recognition installed and tested first and then you should be good to go with this repo.

face_recognition requires a package called dlib.
If you have a GPU you must install dlib in a specific way in order to get it to use your GPU.
