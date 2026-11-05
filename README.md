# Md Tuhuruzzaman — Professional Portfolio

A static website: no build step. Open `index.html` to preview it, upload the folder to any static host (Netlify, Vercel, GitHub Pages, cPanel).

## Folder
```
index.html
assets/
  Md_Tuhuruzzaman_Resume.pdf   <- your CV (already included)
  profile.jpg              <- your photo (already included)
```

## 1. Make the Resume buttons work (required)
1. Export your CV as a PDF and name it `Md_Tuhuruzzaman_Resume.pdf`.
2. Put it in the `assets/` folder next to `index.html`.
3. Upload the whole folder. **View Resume** opens `assets/Md_Tuhuruzzaman_Resume.pdf` in a new tab in the browser's PDF viewer; **Download Resume** downloads it under the same name.

To use a different file name or location, change `CONFIG.resume` near the top of the script in `index.html`.

## 2. Edit mode (owner only)
Open `index.html?edit` (or the "Owner edit mode" link in the footer). You can:
- Click any dashed text and type to change it (metrics, reporting periods, responsibilities, project fields, achievements…).
- Upload / replace / remove images in every image area and use **Position / crop** to frame them.
- **Contact & links:** enter your email, LinkedIn, phone (all taken from your CV) and an optional form endpoint.
- **Upload CV PDF:** previews the resume buttons with your file in your own browser.

Edit-mode changes are stored in *your* browser only, so visitors will not see them until you publish them:

- **Text, contact details, crops:** click **Export edits (JSON)**, then paste the file's contents over `const PUBLISHED = {...}` near the top of the script in `index.html`, and re-upload.
- **Images:** save each image into `assets/`, then add it to `PUBLISHED.images`, e.g. `{ "hero": "assets/profile.jpg", "p1-a": "assets/ezjobs-campaign.png" }`. Each image area shows its slot id (like `hero`, `p1-a`) in edit mode.
- **CV:** the PDF in `assets/` as in step 1.

Items beginning with "Add …" are placeholders. They are hidden from visitors until you replace them with real details.

## Tool logos
Brand logos (from the open-source Simple Icons set) are included in `assets/logos/` for Meta, Google Ads, LinkedIn, Google Analytics, Canva, ChatGPT (OpenAI), Gemini, WhatsApp and Telegram. CapCut and IMO have no logo in that set, so they show a neutral icon. To show a tool's official logo, download it from that brand's own press or brand page, save it in `assets/` (for example `assets/canva.png`) and add it to `PUBLISHED.images`, like `'tool-5':'assets/canva.png'`. In edit mode every tool has a Logo button to preview an upload first, and its id (`tool-0` … `tool-11`) follows the tool order.

## 3. Contact form
- With a form endpoint (for example a free Formspree form URL) set in Contact & links, the form posts there.
- Without one, but with your email set, submitting opens the visitor's email app with the message addressed to you.
- With neither, the form tells the visitor it is not connected yet. Nothing is faked.

## 4. Social preview image
Add `assets/og-image.jpg`, then uncomment the `og:image` lines in the `<head>` and replace `YOUR-DOMAIN` with your site address.

## Content taken from your CV
Name, email, phone, LinkedIn, job titles and dates, responsibilities, skills, industries and education come from the CV. Figures use the CV's Transsion section plus the periods you gave: app downloads and CPI cover about the last 6 months, and views, impressions, reach, campaigns managed and followers about 8–9 months (organic and paid combined where noted).

Still blank (hidden from visitors until you fill them in): company descriptions, project roles and durations, graduation years, professional goals, certifications, extra achievements and testimonials. The Top Performer Award (2025) is shown with your trophy photo (`assets/top-performer-award.jpg`).

Your home street address and your referees' phone numbers are in the CV PDF, so anyone who opens View Resume will see them. They are not shown on the web pages themselves.
