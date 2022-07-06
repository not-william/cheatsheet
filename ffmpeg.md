```bash
# Convert audio to mp3
ffmpeg -i '<INPUT_FILE>' -vn -c:a libmp3lame -b:a 320k out.mp3

# Convert every flac file in the current directory to mp3
for f in *.flac; do ffmpeg -i  "$f" -vn -c:a libmp3lame -b:a 320k "${f%.flac}.mp3"; done;

# convert a video to gif with okay quality
ffmpeg -i '<INPUT_FILE>' -r 15 -vf "scale=512:-1,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" '<OUTPUT_FILE>'

# Trim audio/video (ex: start at 5 sec and go until 2 min)
ffmpeg -i '<INPUT_FILE>' -c:a copy -c:v copy -ss 5 -to 120 '<OUTPUT_FILE>'
```

