# OneTap Cards

NFC digital business cards. Each client gets a folder in this repo.  
Tapping the card opens `onetapcards.co/their-name`.

---

## Adding a New Client

### 1. Copy the template folder
Duplicate `_template/` and rename it to the client's name — **lowercase, hyphens, no spaces.**

```
_template/        →   julian-schwartz/
```

### 2. Drop in their files
```
julian-schwartz/
├── index.html
└── assets/
    ├── photo.jpg     ← their headshot (square crop works best)
    └── resume.pdf    ← their resume
```

### 3. Edit the CLIENT block in `index.html`
Open `julian-schwartz/index.html` and update only this section at the top of the `<script>` tag:

```js
const CLIENT = {
  name:        "Julian Schwartz",
  tagline:     "Based in Tampa, Florida — Marketing Student at The University of Tampa",
  photo:       "assets/photo.jpg",
  resumeUrl:   "assets/resume.pdf",
  linkedinUrl: "https://linkedin.com/in/julianschwartz",

  contact: {
    firstName: "Julian",
    lastName:  "Schwartz",
    phone:     "+18135551234",
    email:     "julian@email.com",
    title:     "Marketing Student",
    company:   "University of Tampa",
    website:   ""
  }
};
```

### 4. Commit and push
```bash
git add julian-schwartz/
git commit -m "Add client: Julian Schwartz"
git push
```

### 5. Program the NFC card
Set the NFC card URL to: `https://onetapcards.co/julian-schwartz`

That's it — the page is live within ~30 seconds of pushing.

---

## Client List

| Client | URL | Date Added |
|--------|-----|------------|
| — | — | — |

---

## File Structure

```
_template/              ← master template — never edit directly
julian-schwartz/        ← one folder per client
  ├── index.html
  └── assets/
      ├── photo.jpg
      └── resume.pdf
CNAME                   ← points GitHub Pages to onetapcards.co
index.html              ← fallback landing page
```
