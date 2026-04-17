# ECE Department Portal

A complete student portal for the Electrical and Computer Engineering department.

## Pages
- `index.html` — Home page with hero, quick navigation, notice preview, upcoming events
- `notices.html` — Main notices (important / CR notices)
- `notices-secondary.html` — General/non-urgent notices
- `semesters.html` — Semester-wise materials (1-1 to 4-2)
- `routine.html` — Calendar with class, exam, lab, viva scheduling
- `students.html` — Directory of all students

## How to Host on GitHub Pages (Step by Step)

### 1. Create a GitHub Account
Go to https://github.com and sign up (free).

### 2. Create a New Repository
- Click the "+" button → "New repository"
- Name it exactly: `yourusername.github.io`
  (Replace `yourusername` with your actual GitHub username)
- Set it to **Public**
- Click "Create repository"

### 3. Upload Your Files
- Click "uploading an existing file" on the repo page
- Drag and drop ALL the HTML files from this folder
- Click "Commit changes"

### 4. Enable GitHub Pages
- Go to your repository Settings
- Scroll to "Pages" in the left sidebar
- Under "Source", select `main` branch and `/ (root)` folder
- Click Save

### 5. Your site is live!
Visit: `https://yourusername.github.io`
(Takes 1-2 minutes to go live after enabling)

## How to Update Content

### Adding Notices
- Open `notices.html` in the browser
- Click "Add New Notice (CR Only)"
- Fill in the form and click Post

### Adding Students
- Open `students.html`
- Click "+ Add Student"
- Fill in name, roll, semester, contact info

### Adding Semester Materials
- Open `semesters.html`
- Select a semester from the left sidebar
- Click a subject to expand it
- Click "Edit links" to add Google Drive links for each type of material

### Adding Calendar Events
- Open `routine.html`
- Use the "Add Event" panel on the right
- Select type: Class, CT/Exam, Lab, or Viva

## Important Notes

### Data Storage
All data (notices, events, students) is stored in `localStorage` (browser storage).
This means:
- Data is stored PER BROWSER — each student's browser has their own copy
- The CR should share notice content directly in the HTML file for permanent storage
- For permanent shared data, consider using Google Sheets as a backend in the future

### For Permanent Shared Data
To have data visible to all 60 students, edit the default data directly in each HTML file:
- In `notices.html`: Edit the `defaultNotices` array in the `<script>` tag
- In `students.html`: Edit the `defaults` array in the `<script>` tag
- In `semesters.html`: Edit the `defaultData` object in the `<script>` tag

### Adding More Material Types
In `semesters.html`, find the line:
```js
const MATS=['Materials','CT Questions','Final Questions','Board Viva Questions','Quiz Questions'];
```
Add more types to this array, then also add an icon to `MAT_ICONS`.

## File Structure
```
ece-portal/
├── index.html              (Home)
├── notices.html            (Main notices)
├── notices-secondary.html  (General notices)
├── semesters.html          (Academic materials)
├── routine.html            (Calendar)
├── students.html           (Student directory)
└── README.md               (This file)
```
