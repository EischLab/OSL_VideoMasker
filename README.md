# OSL_VideoMasker
This program will let you add a circle of whatever size you want to a .mp4 file and will regenerate the video with that circle. 


Please go to Line 78, and paste the pathway to your .mp4 in the text between the quotation marks - e.g. "/Users/primalkarma/Desktop/OSL Red Light July 25th 2023/NoneT1.mp4."

Click on the center of the petri dish and then click on the edge of the petri dish to make the circle. If you find this circle to be the right size, please press "y" if not press "n" to let the program close itself and you will need to run the program again to reselect the circle. 

In the black terminal on your Visual Code Studio, or whatever program you are using you will see a progress bar like so E.G. "Processing Frames:  80%|█████████████████████████████████         | 71/89 [00:00<00:00, 79.52frame/s]" 

- This indicates that your video is being generated.
- Your video will be generated and SAVED onto your desktop titled the same as your video you have chosen except with "_Masked" tacked to the end of the title.

You will need to do this for every video file, but this should be a lot easier for you. 


████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████

**GENERAL OVERVIEW OF CODE: SKIP IF YOU DONT CARE ABOUT HOW THE PROGRAM WORKS:**

This Python script allows you to select a circular region in a video and process the video with the selected circular mask. Here's how the script works:

The script imports necessary libraries, including OpenCV (cv2) for video processing, numpy for numerical operations, threading for background video processing, os for file operations, and tqdm for a progress bar.

It defines global variables to store the circle center point, radius, and other flags to keep track of user interactions.

The draw_circle function is used as a callback function to handle mouse events. When you left-click on the video frame, it allows you to select the circle center and radius by clicking twice: once for the center and again for the radius. The selected circle is previewed on the video frame.

The get_confirmation function is used to ask the user for confirmation if they are okay with the selected circle.

The process_video function takes the input video file path, processes the video frames by drawing the selected circle on each frame, and saves the output video with the applied circular mask.

In the main section of the script:

The input video file path is provided.
The script reads the first frame of the video and displays it for the user to select the circular region.
The user can left-click twice on the video frame to select the circle center and radius. The selected circle is previewed on the video frame in real-time.
After the user confirms the selected circle, a new thread is started to process the video with the circular mask applied in the background. A progress bar shows the progress of video processing.
If the user presses 'q' or selects 'N' during the circle selection, the script terminates without processing the video.
Please note that this script is designed to work with the OpenCV version installed on your system. You should have OpenCV and the necessary libraries (numpy, tqdm) installed to run this script successfully.

Remember to adjust the input_video_file variable with the path to the video you want to process before running the script. Additionally, make sure the necessary video codecs are available on your system to save the output video in the desired format.


