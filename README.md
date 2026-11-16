# Oldham Neighbourhood Contacts

A single-file web app (`index.html`) that reads the partner contacts Google Sheet and shows each person on a map of Oldham's five districts (North, West, Central, East, South) and their wards.

## Publish on GitHub Pages
1. Create a GitHub repository and upload `index.html`.
2. Go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then click **Save**.
3. Your site will be at `https://<your-username>.github.io/<repo-name>/`.

You don't need any API keys. The map uses Leaflet and OpenStreetMap, and the ward boundaries (ONS, December 2024) are built into the file.

## Keeping data up to date
- Edit the Google Sheet. The site shows the changes the next time someone loads the page or presses **Refresh data**.
- The sheet must stay shared as **Anyone with the link → Viewer**.
- Keep the column headings: Name, Org, Team, Job Title, District/Ward, Email.
- In **District/Ward**, enter a district name (`North`, `Central`, `East`, `South`, `West`), more than one separated by `/` (for example, `West / North`), or `ALL`. You can add ward names after the district, for example `South/Failsworth, Hollinwood`.
- Services come only from the **Service** column. Separate several services with `/` (for example, `Adult Services / Mental Health`). The person will appear under each of them.
- The app groups people by the **Organisation** column. Each contact card shows every column in the sheet, so a new column (such as Phone) appears on the cards automatically.
- To use a different tab, set `SHEET_GID` near the top of the script.

## Privacy note
Anyone with the site link can see the names and email addresses on it. Make sure everyone listed is happy for their details to be public.
