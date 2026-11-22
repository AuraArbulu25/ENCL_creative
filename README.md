#  personal page for job application - just for fun

A one-page static site. All the text, figures and map cities live in `content/site.json`, which can be edit in Pages CMS. `index.html` reads that file when the page loads, so there is no build step.

## Files

- `index.html`: layout, styles and the map. 
- `content/site.json`: all the content.
- `.pages.yml`: tells Pages CMS which fields to show.

## Put it online

1. Create a new GitHub repository (for example ) and upload these files, keeping the `content` folder and the `.pages.yml` file (it starts with a dot, so make sure it is uploaded).
2. In Vercel: **Add New → Project**, import the repository, set the framework preset to **Other**, leave the build command empty, and deploy.
3. In Pages CMS (app.pagescms.org): sign in with GitHub, open the repository, and edit **Page content**. Each save is a commit, and Vercel redeploys automatically within a minute.

## Adding the video

Upload the video to YouTube (Unlisted is fine) or Vimeo, then paste the normal link into **Video → YouTube or Vimeo link**. The page turns it into an embed. Leave the field empty to show the placeholder.

## Adding a city to the map

In **Map cities**, add an item with the name, longitude and latitude (west and south are negative numbers). If labels overlap, turn off **Show name on the map** or change the label position or offset. Every city is also listed under the map.

## Preview locally

Opening `index.html` directly from your disk will not load the content (browsers block that). Run `python3 -m http.server` in the folder and open http://localhost:8000.
