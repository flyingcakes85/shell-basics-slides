<!-- .slide: data-background="#232323" -->

# USEFUL COMMANDS <!-- .element: class="r-fit-text" -->

---

## `convert`

Comes from `imagemagik` - the swiss army knife for image manipulation.

`convert source.ext dest.ext`

Convert from *any* format to *any* format.

<!-- .slide: data-background="#232323" -->

---
Can limit filesize too

`convert original.jpeg -define jpeg:extent=30kb output.jpg`

`convert original.jpeg -define jpeg:extent=300kb -scale 50% output.jpg`

<!-- .slide: data-background="#232323" -->
---

## `ffmpeg`

Same as imagemagick, but for videos.

`ffmpeg -i input-video.mp4 ouptut.ext`

<!-- .slide: data-background="#232323" -->



---
Extracting frames

`ffmpeg -i video.mp4 frames/frame-%04d.jpg`

<!-- .slide: data-background="#232323" -->

---

## Downloading YouTube Videos

`youtube-dl "https://www.youtube.com/watch?v=TFT9binq5Cw"`
<!-- .slide: data-background="#232323" -->


---

Can pass loads of links in one go

`youtube-dl https://www.youtube.com/watch?v=98fqXx-KFgI https://www.youtube.com/watch?v=IslOnO0WgIg https://www.youtube.com/watch?v=lBeiuhb36RY ...more links"`

Downloads them one by one.
<!-- .slide: data-background="#232323" -->

---

Or store links in a file

`youtube-dl -a links.txt`
<!-- .slide: data-background="#232323" -->
---

Maybe show possible output formats

`youtube-dl "https://www.youtube.com/watch?v=c68g_6mQyiE" -F`

`youtube-dl "https://www.youtube.com/watch?v=c68g_6mQyiE" -f 22`
<!-- .slide: data-background="#232323" -->


---

Streaming Videos?

`mpv "https://www.youtube.com/watch?v=pBX2T7R_DgY"`


For only audio, pass `--no-video`
`mpv "https://www.youtube.com/watch?v=pBX2T7R_DgY" --no-video`

I even got a detailed blog post about this. [Click here](https://flyingcakes85.github.io/blog/shell/2021/06/01/mpv-yt.html)
<!-- .slide: data-background="#232323" -->


---

### Final cheat code!

`alias ytmp3="youtube-dl --extract-audio --audio-format mp3 --audio-quality 256K --add-metadata --metadata-from-title \"%(artist)s - %(title)s\" -o \"%(title)s.%(ext)s\""
`
<!-- .slide: data-background="#232323" -->
