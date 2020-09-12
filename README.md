# movie-music-kitchen

# separate movie into audio file and movie-only file
e.x
`ls movies/ | xargs -L 1 -I @  ffmpeg -i ./movies/@  -acodec copy -map 0:1 ./output/audio/@.aac`
`ls movies/ | xargs -L 1 -I {}  ffmpeg -i ./movies/{}  -vcodec copy -map 0:0 ./output/audio/{}.mp4`
