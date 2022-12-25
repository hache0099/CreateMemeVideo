# CreateVideoMeme
This is a Shell script to put caption on top of videos (thus, making them memes)

# Getting Started
## Dependencies
[ffmpeg](https://ffmpeg.org/) (*ffmpeg* and *ffprobe*)  
[imagemagick](https://github.com/ImageMagick/ImageMagick) (*convert*) 

## Installation
Just copy `video-meme` to your **$PATH** and make it executable (`sudo chmod +x $PATH/video-meme`)

# Usage
```   
video-meme <VIDEO_PATH> <TEXT> [--textsize SIZE]
	[--showimage] [--font FONT | --font <FONT_FILE_PATH>] OUTPUT_FILE
	
Options
	--textsize SIZE		Set the size of the text (default 75)
	--showimage		Show the caption image before making the video
	--font FONT		Set a font for the caption text (default: helvetica)
```

To see a list of available fonts run 
```
convert -list font
```
