# Skylene Links

Link page for **Skylene**, heavy melodic music from Honolulu, Hawaii.
One page with the band's video, streaming links, merch, socials and shows.
Plain HTML and CSS, no build step, hosted on GitHub Pages.

## What's on the page

- YouTube video: "Without Regard"
- Stream "Within My Vicinity"
- Spotify
- Apple Music
- Merch Store (Bandcamp)
- Instagram
- Facebook
- Bandsintown

Every button links straight to the destination, with no redirect or tracking service in between.

## Files

```
index.html         page content and links
style.css          layout, background and mobile styles
media/             background artwork and favicon
link-icons/        icons shown on each link button
```

## Editing

**Change or add a link:** in `index.html`, copy one of the `<li>` blocks inside
`<ul class="profile-links">`, then change the `href`, the icon file and the label.
Keep `target="_blank" rel="noopener noreferrer"` so it opens in a new tab.

**Add an icon:** drop a white PNG or SVG into `link-icons/`. Icons display at 40×40px.

**Change the video:** in `index.html`, replace the ID at the end of the
`youtube.com/embed/...` address with the new video's ID (the part after `watch?v=`
in a normal YouTube link). Keep the `referrerpolicy` attribute, or YouTube shows Error 153.

**Change the background:** replace `media/Background CD 3000.jpg`, or update the
file name in both places it appears in `style.css` (`.page::before` and `.profile-image`).

## Preview locally

Opening `index.html` straight from Finder works for the layout, but the YouTube video
won't play that way. To preview it properly, run this from the project folder:

```
python3 -m http.server
```

Then open http://localhost:8000.

## Publishing

The site is published with GitHub Pages. Changes go live a minute or two after they're
merged into `main`. Work happens on the `dev` branch and is merged into `main` once reviewed.
