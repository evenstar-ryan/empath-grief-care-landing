# Setup Instructions

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `empath-grief-care` (or your preferred name)
3. Description: "Empath Health Grief Care Support Groups Website"
4. Set to **Public** or **Private** (your choice)
5. **DO NOT** initialize with README, .gitignore, or license (we already have these)
6. Click "Create repository"

## Step 2: Push Code to GitHub

Run these commands in your terminal from the `empath-grief-care` folder:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Empath Grief Care Support Groups website"

# Add your GitHub repository as remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/empath-grief-care.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Connect to Cloudflare Pages

1. Log into your Cloudflare Dashboard: https://dash.cloudflare.com
2. Go to **Workers & Pages** in the left sidebar
3. Click **Create Application**
4. Select the **Pages** tab
5. Click **Connect to Git**
6. Click **Connect GitHub** (if not already connected)
7. Select your `empath-grief-care` repository
8. Configure the build settings:
   - **Project name:** empath-grief-care (or your preferred name)
   - **Production branch:** main
   - **Build command:** (leave empty - this is a static HTML site)
   - **Build output directory:** / (just the root)
9. Click **Save and Deploy**

Cloudflare will now build and deploy your site. The first deploy takes about 1-2 minutes.

## Step 4: Get Your Site URL

After deployment completes:
1. You'll see your site URL (something like `empath-grief-care.pages.dev`)
2. Click on the URL to view your live site
3. You can add a custom domain later if needed

## Step 5: Automatic Deployments

From now on, whenever you push changes to the `main` branch:
1. Cloudflare Pages will automatically detect the changes
2. It will rebuild and redeploy your site
3. Changes typically go live within 1-2 minutes

## Making Updates

To update the site content:

```bash
# Make your edits to index.html
# Then:
git add index.html
git commit -m "Update: [describe your changes]"
git push
```

Cloudflare Pages will automatically deploy the changes.

## Custom Domain (Optional)

If you want to use a custom domain:
1. In Cloudflare Pages project settings
2. Go to **Custom domains**
3. Click **Set up a custom domain**
4. Follow the DNS configuration steps

## Troubleshooting

**If git push fails with authentication error:**
- You may need to set up a Personal Access Token
- Go to GitHub Settings > Developer settings > Personal access tokens
- Generate a new token with 'repo' scope
- Use the token as your password when pushing

**If Cloudflare Pages shows a 404:**
- Make sure `index.html` is in the root directory of your repo
- Check that the build output directory is set to `/`

## Handing Off to Empath Health

When ready to transfer:
1. Give them the GitHub repository URL
2. You can transfer ownership of the repo to their GitHub organization
3. They can reconnect the Cloudflare Pages project to their own Cloudflare account
4. Or simply provide them with the built files and deployment instructions
