# CreateVideoMeme
This is a Shell script to put caption on top of videos (thus, making them memes)

# Getting Started
## Dependencies
[ffmpeg](https://ffmpeg.org/) (*ffmpeg* and *ffprobe*)  
[imagemagick](https://github.com/ImageMagick/ImageMagick) (*convert*) 

## Installation
Just copy `video-meme` to your **$PATH** and make it executable (`sudo chmod +x $PATH/video-meme`)

# Usage
Simple example  
If you use it this way, the script will try to find an optimal size for the text.
```
$ video-meme input.mp4 "Your text here" output.mp4
```

To use a different font
```
$ video-meme --font <font> input.mp4 "<text>" output.mp4
```
You can use a font installed in your system or a custom font file (as long as it's supported by magick)

To see a list of available fonts run 
```
$ convert -list font
```

To set the text size
(This will deactivate the auto-set-size feature)
```
$ video-meme --textsize <size> input.mp4 "<text>" output.mp4
``` 

If you want to see the caption image before the video is processed
```
$ video-meme --showimage input.mp4 "Your text here" output.mp4
```

Use `-h` to display the help message
```
video-meme <VIDEO_PATH> <TEXT> [--textsize SIZE]
	[--showimage] [--font FONT | --font <FONT_FILE_PATH>] OUTPUT_FILE
	
Options
	--textsize SIZE		Set the size of the text (default 75)
	--showimage		Show the caption image before making the video
	--font FONT		Set a font for the caption text (default: helvetica)
```

# Known bugs
The _auto-set-font-size_ feature is experimental and very slow, for now is recommended to use the `--textsize` option
