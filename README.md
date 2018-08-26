# scrub

Go here, scrub: https://pnutus.github.io/scrub

Works best on Safari, okay on Chrome, and lags on Firefox. Other browsers: ???

## How

I used `ffmpeg` to create video from a bunch of jpegs. Here's the full command: 

`ffmpeg -framerate 60 -pattern_type glob -i "chili jpegs/*.JPG" -g 1 -vf scale=-1:482 -vcodec libx264 -crf 15 -pix_fmt yuv420p chili.mp4`

I needed to encode the videos with every frame being a keyframe (or I-frame, in video compression parlance) to make seeking fast enough. That's what the `-g 1` option above does.

## Attribution

Uses a modified copy of <https://github.com/spaciecat/spring-slider>. Thanks, Spacie!
