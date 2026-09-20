# QuantWM — anonymous project page

A standalone static website with 24 supplied videos: four models, two examples per model, and BF16 / QVG / QuantWM comparisons. No build step or external dependencies.

## Preview

Run `python3 -m http.server 8000` in this directory and open http://localhost:8000.

## GitHub Pages

1. Create a repository under an anonymous GitHub account or organization.
2. Upload the contents of this directory to the repository root (including `assets` and `.nojekyll`).
3. In repository Settings → Pages, select Deploy from a branch, `main`, and `/ (root)`.
4. Open the Pages URL shown by GitHub after deployment.

The website contains no author, affiliation, email, analytics, or personal links. Use an anonymous repository owner and commit identity as those are public independently of the website.

## Video files

`assets/{model}-{example}-{method}.mp4`; methods are `bf16`, `qvg`, and `quantwm`. The supplied video stream is copied without re-encoding; audio and source metadata are omitted. JPEG thumbnails are previews only and do not replace video frames. The three videos in each example have matching durations and dimensions. Replace matching files to update comparisons.

Playback is synchronized per row with a common seek position and speed, plus periodic drift correction; independent browser video decoders do not provide frame-lock guarantees. Only one row plays at a time. Changing models or hiding the tab pauses playback.
