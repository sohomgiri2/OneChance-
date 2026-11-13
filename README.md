# My Special Website — v2.0.0

A mobile-first friendship experience and developer portfolio created for Soham Giri.

## 1. Folder structure

```text
My-Special-Website/
├── index.html
├── README.md
└── assets/
    ├── photos/
    ├── voice/
    ├── music/
    ├── projects/
    └── icons/
```

The application is intentionally contained in `index.html`. The asset folders are ready for your own media.

## 2. Open locally

Open `index.html` in a browser. For the most reliable testing, use a local static server or publish with GitHub Pages.

## 3. Add photos

1. Put your images in `assets/photos/`.
2. Open `index.html` and find `const SITE_CONFIG`.
3. Add entries to `photos`, for example:

```js
photos: [
  { src: "assets/photos/photo1.jpg", caption: "A favourite day", alt: "Friends outdoors" },
  { src: "assets/photos/photo2.jpg", caption: "A little memory" }
],
```

The gallery is manifest-based; adding a file alone does not automatically add it to the gallery. Missing images show a graceful placeholder.

## 4. Add voice recordings

Copy your recordings to `assets/voice/`, then register them:

```js
voiceNotes: [
  { title: "A little hello", src: "assets/voice/voice1.mp3" },
  { title: "A memory", src: "assets/voice/voice2.mp3" }
],
```

Only one voice recording plays at a time. Playback never starts automatically.

## 5. Add music

Copy your own MP3 files to `assets/music/` and add:

```js
songs: [
  { title: "Song one", src: "assets/music/song1.mp3" },
  { title: "Song two", src: "assets/music/song2.mp3" }
],
```

Use only music you own or have permission to use. The player includes play/pause, next/previous, shuffle, repeat, native progress and volume controls. There is no autoplay.

## 6. Add previous websites to the portfolio

1. Put project screenshots in `assets/projects/`, e.g. `project1.jpg`.
2. Add real project details to `projects` in `SITE_CONFIG`:

```js
projects: [
  {
    title: "My Previous Website",
    description: "A website created by me.",
    image: "assets/projects/project1.jpg",
    liveUrl: "https://your-real-website.example",
    githubUrl: "",
    technologies: ["HTML", "CSS", "JavaScript"],
    category: "Website"
  }
],
```

Leave `liveUrl` or `githubUrl` as an empty string if you do not want that button displayed. Do not add placeholder or invented projects.

## 7. Edit developer information

Find the `SITE_CONFIG.developer` object near the beginning of the script. The visible developer card currently displays:

- Soham Giri
- Independent Web Developer · Creative Developer
- Instagram: `@ITchat_SG_063`

The Instagram link is set to `https://www.instagram.com/ITchat_SG_063/`.

## 8. Change version and changelog

Update `version` and add a changelog entry:

```js
version: "2.0.1",
changelog: [
  { version: "2.0.1", date: "2026-11-20", description: "Describe what changed." },
  { version: "2.0.0", date: "2026-11-13", description: "Initial release." }
],
```

This is a manual changelog. The site does not claim to detect GitHub commits automatically.

## 9. Publish with GitHub Pages (Android-friendly workflow)

1. Sign in to GitHub in your browser or app and create a new **public** repository, for example `My-Special-Website`.
2. Upload `index.html` and `README.md` to the repository root.
3. Upload the `assets` folders and your media files, keeping the exact folder names and paths.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then save.
7. Wait for GitHub Pages to publish. Open the URL shown in the Pages settings.

For large media files, upload from a desktop browser if the mobile interface is difficult. Keep filenames and capitalization exactly the same; GitHub Pages paths are case-sensitive.

## 10. Troubleshooting

- **A photo/audio file does not appear:** Confirm it is listed in the relevant configuration array and the path matches the uploaded filename exactly.
- **A project has no Live button:** This is intentional when `liveUrl` is blank.
- **Audio will not play:** Check that the file is a supported audio format and uploaded to the correct folder. Start playback with a tap; browsers block autoplay.
- **A photo shows a placeholder:** Check its path and filename. The gallery uses a manifest, not automatic folder scanning.
- **GitHub Pages shows 404:** Confirm `index.html` is in the repository root and Pages is configured for `main` → `/(root)`.
- **Changes do not appear:** Refresh the page, wait for Pages deployment, and check the repository's latest commit.
- **No projects yet:** Add actual projects to `SITE_CONFIG.projects`; the portfolio will show a helpful empty state until then.

## 11. Notes

- All visible interface copy is in English.
- Three themes are included: Pink Princess, Dreamy Purple and Soft Nature.
- The entry page transitions into the main experience without a page reload.
- Reduced-motion preferences are respected.
- This project has not been represented as browser-tested on every device. Test your own media and deployment after uploading.
