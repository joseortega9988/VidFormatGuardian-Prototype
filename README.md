# VidFormatGuardian Prototype

## Propuse of the Client: 
An Online Film Festival receives every year a lot of films. The problem is that some of these films are not submitted in the format specified by the festival organisation, and they must be converted.
The organisation wants to automate this process by developing an application for examining the format of the films and, if necessary, convert them to the right format

## Overview

VidFormatGuardian is an automated tool designed to ensure video files adhere to predefined format criteria. Leveraging FFmpeg and FFprobe, this application checks and converts video files, guaranteeing compliance with specified standards for video and audio formats, frame rates, aspect ratios, and more.

<img width="367" alt="Screenshot 2024-03-26 145617" src="https://github.com/joseortega9988/VidFormatGuardian-Prototype/assets/77720475/99ecd541-56ea-4f3b-8ed2-70b9af0a1af9">

## Installation

### Windows

- **FFmpeg and FFprobe Installation**: Essential for video and audio processing, offering capabilities for encoding, decoding, transcoding, and analysis.
  1. Download and extract FFmpeg.
  2. Navigate to the `bin` directory containing the FFmpeg and FFprobe executables.
  3. Create a directory on your hard drive, preferably within the Program Files folder, and move the executables there.
  4. Add the directory to your computer's PATH environment variable.
  5. Verify installation via command prompt with 'ffmpeg'.
For detailed installation instructions, refer to [this video](https://www.youtube.com/watch?v=IECI72XEox0).

- **Run the File**:
  1. Download the zip file un unzip in a directory of yuor preference
  2. Open the file in a IDE that run jypyter notebooks and run all the cells


## Helper Functions

VidFormatGuardian includes several helper functions for tasks not natively supported by FFmpeg, such as calculating video aspect ratios, converting bit rates, and retrieving video metadata.

## Processing and Verification

<img width="327" alt="Screenshot 2024-03-26 145224" src="https://github.com/joseortega9988/VidFormatGuardian-Prototype/assets/77720475/7678ad3d-ba5d-42b4-b0ab-fd78bee8fde0">

The `validate_file` function is key to the application's operation, extracting metadata to verify file format compliance against the criteria the festival have, this criteria is the following:

- Video format (container): mp4
- Video codec: h.264
- Audio codec: aac
- Frame rate: 25 FPS
- Aspect ratio: 16:9
- Resolution: 640 x 360
- Video bit rate: 2 – 5 Mb/s
- Audio bit rate: up to 256 kb/s
- Audio channels: stereo

Files failing to meet these standards are identified, reported, and subsequently converted to the correct format, ensuring uniformity across all processed videos.

<img width="433" alt="Screenshot 2024-03-26 145625" src="https://github.com/joseortega9988/VidFormatGuardian-Prototype/assets/77720475/1f203484-1b5c-491d-a46c-fad8b9abc334">

## Conclusion

VidFormatGuardian automates the meticulous process of video file format verification and conversion, embodying a comprehensive solution for maintaining format consistency across digital video libraries.

****For info of details, please check the documentation or the comments in the code****
