# Personal website: Jiayi (Joyce) Zhang

A plain static website (no build step, no frameworks). It replaces the old AcademicPages/Jekyll site at https://jz2655.github.io.

```
index.html                  the whole site (About, Research, Publication, Teaching, CV)
images/profile.jpg          headshot (4:5 crop of your original photo)
images/…                    the two figures
files/CV_Jiayi_Zhang.pdf    CV shown on the CV page
publications/, teaching/,   tiny redirect pages so old links such as
cv/, talks/, portfolio/…    jz2655.github.io/publications/ still land on the right page
```

## Put it on GitHub (replacing the old site)

Your current site lives in the repository `JZ2655/jz2655.github.io` (default branch `master`). The safest way to replace it is to keep the old one as a backup under a new name and start a clean repository.

1. **Back up the old site.** Open the old repository on github.com, go to **Settings > General**, change **Repository name** to `academicpages-old`, and click **Rename**. Then open **Settings > Pages** in that repository and unpublish it (optional, so the backup isn't a second live site).
2. **Create the new repository.** Click **New repository**. Name it exactly `jz2655.github.io`, set it to **Public**, leave "Add a README" unchecked, and click **Create repository**.
3. **Upload the site.** Unzip this folder. On the new repository page click **uploading an existing file**, then drag in everything *inside* the unzipped folder: `index.html`, `README.md`, and the folders `images`, `files`, `publications`, `teaching`, `cv`, `talks`, `portfolio`, `year-archive`, `markdown`. Write a message such as "New website" and click **Commit changes**.
4. **Turn on Pages.** Go to **Settings > Pages**. Under **Build and deployment** choose **Deploy from a branch**, pick branch `main` and folder `/ (root)`, and click **Save**.
5. After 1 to 2 minutes, open https://jz2655.github.io. Click through all five tabs, the icons, and the CV download once.

## Updating the site later

Everything is edited in the browser on github.com: open the file, click the pencil icon, change it, then **Commit changes**. The live site updates in about a minute.

| To change… | Do this |
|---|---|
| **Add a publication** | Open `index.html`, search for `ADD A PAPER`, copy any `<li>…</li>` under the right heading (journal or conference), paste it at the **top** of that list, and edit the text. The numbers ([C.46], and so on) are added automatically. Wrap the authors you want in bold as `<strong>Zhang, J.</strong>`. For an award badge, add `<span class="award">Best Paper Nomination</span>` at the end of the line. |
| **Update citation numbers** | Search for `748` in `index.html` and edit the four numbers and the date under "Source: Google Scholar". |
| **Add a news item** | Search for `Recent Highlights` and add an `<li>` at the top of the list. |
| **Add a project or course** | Search for `<!-- TEACHING -->` or `<!-- RESEARCH -->` and copy an existing item. |
| **New CV** | In the repository open `files`, click **Add file > Upload files**, and upload the new PDF with the same name, `CV_Jiayi_Zhang.pdf`. |
| **New photo** | Upload a new `images/profile.jpg` the same way (about 720 x 900 px works well). |

Tip: keep a copy of what you change in a text editor first if you're making several edits, then paste once. If something looks wrong after a commit, open the file's **History** and revert it.

## Notes

- Each page can be linked directly: `https://jz2655.github.io/#research`, `#publication`, `#teaching`, `#cv`.
- The CV page embeds the PDF. Some phone browsers only show the first page, so a **Download CV (PDF)** link is above it.
- The site follows the visitor's dark or light mode setting.
- A custom domain can be added later in **Settings > Pages > Custom domain**.
