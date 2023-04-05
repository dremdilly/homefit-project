# homefit-project

# Pose Detector for Bicep Curl Counter

This is a simple Flask application that utilizes the `PoseModule` to detect and count bicep curls in a given video. The application takes an input video and processes it, then generates an output video with a curl count, angle percentage, and a visual indicator.


Install the required packages:

pip install -r requirements.txt

## Running the Application

1. Start the Flask application:

python app.py

2. Send a request to the `/curl` endpoint with the video parameter:

- Replace `<path_to_video>` with the actual path to the input video:

curl "http://localhost:5000/curl?video=<path_to_video>"

3. The output video will be generated in the `video` folder with a `_processed.mp4` suffix. The JSON response will also contain the absolute path to the output video.

## Example

If you have a video file named `curls.mp4` in your project directory, run the following command to process it:

curl "http://localhost:5000/curl?video=curls.mp4"

After processing, the output video will be saved as `curls_processed.mp4` in the `video` folder.
