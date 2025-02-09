# generate-image-flux

## Overview
Takes a video file and generates a stereoscopic 3D side-by-side version using depth information computed with Depth Anything V2.

## Module Inputs
- **input-file**: (Text) Input video file path
- **output dir**: (Text) Directory where output files will be saved
- **resize-video**: (True/False) Whether to resize the input video
- **resize-resolution**: (Select) Target resolution for resizing ["480x360", "720x480", "1280x720", "1920x1080", "2560x1440"]
- **conversion-chunk**: (Number) Number of frames to process in each batch
- **depth strength**: (Number) Strength of the depth effect (default: 1)
- **save depth**: (True/False) Whether to save the depth map video
- **progress bar**: (Any) UI progress bar element
- **ui-video**: (Any) UI video preview element

## Module Outputs
- **output-file**: (Text) Path to the generated stereoscopic video file
- **src-path**: (Text) Source video file path
- **video-width**: (Number) Width of the processed video
- **video-height**: (Number) Height of the processed video

## Notes
- The depth map is generated using Depth Anything V2
- Output includes side-by-side stereoscopic 3D format
- Optional depth map video can be saved separately
- Progress is shown via UI elements during processing
- Video can be optionally resized to standard resolutions
- Processing is done in chunks to manage memory usage
