# Simple Comment Rules Page (Dark Theme)

This is a simple Node.js (Express) application designed to serve a beautiful, dark-themed "Community Comment Guidelines" page. It is optimized for easy deployment on Vercel.

## Project Structure

- `server.js`: The minimal Express server that serves the static files from the `public` directory.
- `public/index.html`: The main HTML file containing the structure and content of the comment rules.
- `public/styles.css`: The CSS file that provides the dark theme, modern layout, and responsive design.
- `package.json`: Defines project dependencies (Express) and the `start` script.
- `vercel.json`: Configuration file for Vercel to correctly identify and deploy the Node.js server.

## Local Development

1.  **Install Dependencies:**
    \`\`\`bash
    npm install
    \`\`\`
2.  **Run the Server:**
    \`\`\`bash
    npm start
    \`\`\`
    The application will be available at `http://localhost:3000`.

## Deployment on Vercel

This project is configured to be deployed directly to Vercel.

1.  **Push to Git:**
    Commit all files (`server.js`, `public/`, `package.json`, `vercel.json`) and push them to a new repository on GitHub, GitLab, or Bitbucket.

2.  **Import Project:**
    - Go to the [Vercel Dashboard](https://vercel.com/dashboard).
    - Click **"Add New..."** and then **"Project"**.
    - Select your Git repository.

3.  **Configure Deployment:**
    - Vercel will automatically detect that this is a Node.js project and use the `@vercel/node` builder, thanks to the `vercel.json` file.
    - **Root Directory:** Ensure this is set to the root of your repository (where `package.json` is located).
    - **Build Command:** Vercel will use the default `npm run build` (which is not needed here) or `npm install`.
    - **Start Command:** Vercel will use the `start` script defined in `package.json` (`node server.js`).

4.  **Deploy:**
    - Click **"Deploy"**. Vercel will handle the rest, and your site will be live!

The `vercel.json` file ensures that Vercel knows to use the Node.js runtime and route all traffic to your `server.js` file, which then serves the static HTML/CSS.
