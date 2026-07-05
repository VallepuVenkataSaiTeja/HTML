# HTML Images and Media

Images and media make webpages more attractive and interactive. HTML provides tags to display **images, audio, video, and embedded content**.

---

# 1. Images (`<img>`)

The `<img>` tag is used to display images on a webpage.

## Syntax

```html
<img src="image.jpg" alt="Description">
```

### Attributes

* `src` → Path of the image
* `alt` → Alternative text shown if the image cannot load
* `width` → Width of the image
* `height` → Height of the image

Example:

```html
<img src="flower.jpg" alt="Beautiful Flower">
```

---

# 2. Setting Image Size

Using HTML attributes:

```html
<img src="flower.jpg" alt="Flower" width="300" height="200">
```

Or using CSS (recommended):

```html
<img src="flower.jpg" alt="Flower" style="width:300px; height:200px;">
```

**Best Practice:** Use CSS for styling whenever possible.

---

# 3. Image Paths

## Same Folder

```text
project/
│
├── index.html
└── flower.jpg
```

```html
<img src="flower.jpg" alt="Flower">
```

---

## Inside a Folder

```text
project/
│
├── index.html
└── images/
      flower.jpg
```

```html
<img src="images/flower.jpg" alt="Flower">
```

---

## Going Back a Folder

```text
project/
│
├── images/
│      flower.jpg
│
└── pages/
       about.html
```

From `about.html`:

```html
<img src="../images/flower.jpg" alt="Flower">
```

---

# 4. Alternative Text (`alt`)

Provides a description if the image cannot load and helps screen readers.

```html
<img src="cat.jpg" alt="A white cat sleeping">
```

**Why use `alt`?**

* Improves accessibility.
* Helps search engines understand images.
* Displays text if the image fails to load.

---

# 5. Title Attribute

Displays a tooltip when the user hovers over the image.

```html
<img src="flower.jpg"
     alt="Flower"
     title="Beautiful Flower">
```

---

# 6. Image as a Link

```html
<a href="index.html">
    <img src="logo.png" alt="Company Logo">
</a>
```

Clicking the image opens the linked page.

---

# 7. Responsive Images

```html
<img src="nature.jpg"
     alt="Nature"
     style="max-width:100%; height:auto;">
```

This allows the image to resize with the screen.

---

# 8. Figure and Caption

Use `<figure>` to group an image with a caption.

```html
<figure>
    <img src="mountain.jpg" alt="Mountain">
    <figcaption>Beautiful Mountain View</figcaption>
</figure>
```

---

# 9. Audio (`<audio>`)

Used to play audio files.

## Syntax

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

### `controls`

Displays:

* Play
* Pause
* Volume
* Progress bar

---

## Multiple Audio Formats

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
    <source src="song.ogg" type="audio/ogg">
    Your browser does not support audio.
</audio>
```

---

# 10. Audio Attributes

| Attribute  | Purpose                   |
| ---------- | ------------------------- |
| `controls` | Show controls             |
| `autoplay` | Play automatically        |
| `loop`     | Repeat continuously       |
| `muted`    | Start muted               |
| `preload`  | Load audio before playing |

Example:

```html
<audio controls loop>
    <source src="music.mp3" type="audio/mpeg">
</audio>
```

---

# 11. Video (`<video>`)

Used to display videos.

## Syntax

```html
<video controls width="500">
    <source src="movie.mp4" type="video/mp4">
</video>
```

---

## Multiple Video Formats

```html
<video controls width="500">
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    Your browser does not support video.
</video>
```

---

# 12. Video Attributes

| Attribute  | Purpose                  |
| ---------- | ------------------------ |
| `controls` | Show controls            |
| `autoplay` | Auto play                |
| `loop`     | Repeat                   |
| `muted`    | Start muted              |
| `poster`   | Thumbnail before playing |
| `width`    | Video width              |
| `height`   | Video height             |

Example:

```html
<video controls width="600" poster="thumbnail.jpg">
    <source src="movie.mp4" type="video/mp4">
</video>
```

---

# 13. Embedding YouTube Videos

Use the embed code provided by YouTube.

Example:

```html
<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="YouTube video"
    allowfullscreen>
</iframe>
```

Replace `VIDEO_ID` with the video's ID.

---

# 14. `<iframe>`

Used to embed another webpage or external content.

Example:

```html
<iframe
    src="about.html"
    width="500"
    height="300">
</iframe>
```

Or embed a map:

```html
<iframe
    src="https://www.google.com/maps/embed?..."
    width="600"
    height="450">
</iframe>
```

---

# 15. Image Formats

| Format   | Best Use                                              |
| -------- | ----------------------------------------------------- |
| JPG/JPEG | Photographs                                           |
| PNG      | Transparent images                                    |
| GIF      | Simple animations                                     |
| SVG      | Logos, icons, vector graphics                         |
| WebP     | Modern format with good quality and smaller file size |

---

# 16. Audio Formats

| Format | Description                    |
| ------ | ------------------------------ |
| MP3    | Most common                    |
| OGG    | Open-source format             |
| WAV    | High-quality, larger file size |

---

# 17. Video Formats

| Format | Description           |
| ------ | --------------------- |
| MP4    | Most widely supported |
| WebM   | Modern web format     |
| OGV    | Open-source format    |

---

# 18. Accessibility Tips

Always:

* Add `alt` to images.
* Add captions or transcripts for videos and audio when appropriate.
* Avoid autoplay with sound.
* Use meaningful filenames (e.g., `company-logo.png` instead of `img1.png`).

---

# 19. Best Practices

* Optimize images to reduce page load time.
* Use responsive images (`max-width:100%; height:auto;`).
* Use the correct file format.
* Use `<figure>` and `<figcaption>` for images with captions.
* Provide fallback text inside `<audio>` and `<video>`.
* Use `controls` so users can play, pause, and adjust volume.

---

# Mini Project Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>Images and Media</title>
</head>
<body>

<h1>Images and Media Example</h1>

<h2>Image</h2>

<figure>
    <img src="images/flower.jpg"
         alt="Red flower"
         width="300">
    <figcaption>Beautiful Red Flower</figcaption>
</figure>

<h2>Audio</h2>

<audio controls>
    <source src="music/song.mp3" type="audio/mpeg">
    Your browser does not support audio.
</audio>

<h2>Video</h2>

<video controls width="500" poster="thumbnail.jpg">
    <source src="videos/movie.mp4" type="video/mp4">
    Your browser does not support video.
</video>

<h2>YouTube Video</h2>

<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="YouTube Video"
    allowfullscreen>
</iframe>

</body>
</html>
```

---

# Summary Table

| Tag                | Purpose                          |
| ------------------ | -------------------------------- |
| `<img>`            | Display an image                 |
| `src`              | Image, audio, or video file path |
| `alt`              | Alternative text for images      |
| `width` / `height` | Set dimensions                   |
| `<figure>`         | Group image and caption          |
| `<figcaption>`     | Caption for a figure             |
| `<audio>`          | Embed audio                      |
| `<source>`         | Specify media source             |
| `<video>`          | Embed video                      |
| `controls`         | Show media controls              |
| `autoplay`         | Play automatically               |
| `loop`             | Repeat media                     |
| `muted`            | Start muted                      |
| `poster`           | Video thumbnail                  |
| `<iframe>`         | Embed webpages, maps, or videos  |

---