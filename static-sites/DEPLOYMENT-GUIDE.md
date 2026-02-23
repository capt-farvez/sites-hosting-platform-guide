# Static Sites Deployment Guide

A guide for deploying static HTML/CSS/JS sites on **Netlify** and **Vercel**.

---

## Prerequisites

- A GitHub account with your project pushed to a repository.
- Your project should have an `index.html` at the root level.
- Basic project structure (Recommended):
  ```
  project/
  ├── index.html
  ├── css/
  │   └── styles.css
  ├── js/
  │   └── script.js
  └── images/
  ```

---

## Netlify

### Method 1: Drag & Drop (Quick Deploy)

1. Go to [netlify.com](https://www.netlify.com) and sign up / log in.
2. From the dashboard, click **Add new site** > **Deploy manually**.
3. Drag and drop your project folder into the upload area.
4. Within seconds, your site will be live with a public URL (e.g., `https://random-name.netlify.app`).

### Method 2: Git-Based Continuous Deployment (Recommended)

1. Go to [netlify.com](https://www.netlify.com) and sign up / log in (preferably via GitHub).
2. Click **Add new site** > **Import an existing project**.
3. Select **GitHub** as your Git provider and authorize Netlify.
4. Choose the repository you want to deploy.
5. Configure build settings:
   - **Branch to deploy:** `main`
   - **Build command:** *(leave blank for plain HTML/CSS/JS)*
   - **Publish directory:** `/` or `.` *(root of the repo, or subfolder path if needed)*
     > **Example from this repo:** If you want to deploy only `project-1`, set the publish directory to `static-sites/project-1`.
6. Click **Deploy site**.


---

## Vercel

### Method: Import via Dashboard

1. Go to [vercel.com](https://vercel.com) and sign up / log in (preferably via GitHub).
2. Click **Add New** > **Project**.
3. Select your GitHub repository from the list.
4. Configure the project:
   - **Framework Preset:** Select **Other** (since it's plain HTML/CSS/JS).
   - **Output Directory:** Leave blank or set to `.`
5. Click **Deploy**.
6. Your site will be live within 10-30 seconds at a URL like `https://your-project.vercel.app`.

---
## References

- [Netlify - Deploying a Static Site](https://www.netlify.com/blog/2016/10/27/a-step-by-step-guide-deploying-a-static-site-or-single-page-app/)
- [Netlify Support - Deploy Static Site](https://answers.netlify.com/t/how-do-i-deploy-a-static-site-html-css-js/30499)
- [Vercel - Deployments Docs](https://vercel.com/docs/deployments)
- [GeeksforGeeks - Host HTML/CSS/JS on Vercel](https://www.geeksforgeeks.org/javascript/how-to-host-html-css-javascript-website-on-vercel/)
- [How to Deploy Static HTML to Vercel](https://stefankudla.com/posts/how-to-deploy-a-static-html-css-and-javascript-website-to-vercel)
