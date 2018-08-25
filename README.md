# scrub

Works best on Safari. Works okay on Chrome and Firefox.

I needed to encode the videos with every frame being a keyframe (or I-frame) to make seeking fast enough. Can be achieved using this ffmpeg command:
`ffmpeg -framerate 60 -pattern_type glob -i "chili jpegs/*.JPG" -g 1 -vf scale=-1:482 -vcodec libx264 -crf 15 -pix_fmt yuv420p chili.mp4`

Uses a modified copy of <https://github.com/spaciecat/spring-slider>. Thanks!
