# Auto Pause/Play Video on Tab Visibility

This JavaScript snippet automatically pauses an HTML `<video>` element when the browser tab becomes inactive and resumes playback when the tab becomes active again.

## Features

- Detects when the browser tab visibility changes.
- Automatically pauses the video when the user switches to another tab.
- Resumes video playback when the user returns to the tab.

## How It Works

The script listens for the `visibilitychange` event and checks the `document.hidden` property:
- If the document is hidden, the video is paused.
- If the document is visible again, the video resumes playing.

## Usage

1. Include a `<video>` tag in your HTML.
2. Link or embed the JavaScript in your HTML file:

```html
<script src="1ea64292-51f3-4926-b909-3abe6bb97f8d.js"></script>
```

Or, if inline:

```html
<script>
  document.addEventListener("visibilitychange", () => {
    const video = document.querySelector("video");
    if (!video) return;

    if (document.hidden) {
      video.pause();
    } else {
      video.play();
    }
  });
</script>
```

## Example

```html
<video controls autoplay>
  <source src="your-video.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

## Compatibility

- Modern browsers that support the Page Visibility API.

