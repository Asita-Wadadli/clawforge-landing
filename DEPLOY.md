# Deploy ClawForge Landing Page to Vercel

## Quick Deploy Steps

### Option 1: Deploy via Vercel CLI (Recommended)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```
   - This will open a browser to authenticate
   - Or use: `vercel login --github` if you have GitHub connected

3. **Deploy the landing page**:
   ```bash
   cd ~/.openclaw/marketing/clawforge-landing
   vercel --prod
   ```

4. **Get your live URL**:
   - Vercel will provide a URL like: `https://clawforge-landing.vercel.app`
   - Or you can add a custom domain later

### Option 2: Deploy via Vercel Web Interface

1. **Go to https://vercel.com**
2. **Sign up / Log in** (use GitHub, GitLab, or email)
3. **Click "Add New Project"**
4. **Import Git Repository** or **Upload files**
5. **Select the folder**: `~/.openclaw/marketing/clawforge-landing`
6. **Deploy**

### Option 3: Deploy via GitHub + Vercel (Best for updates)

1. **Create a GitHub repository**:
   - Go to https://github.com/new
   - Name: `clawforge-landing`
   - Make it public or private

2. **Push the code**:
   ```bash
   cd ~/.openclaw/marketing/clawforge-landing
   git remote add origin https://github.com/YOUR_USERNAME/clawforge-landing.git
   git branch -M main
   git push -u origin main
   ```

3. **Connect to Vercel**:
   - Go to https://vercel.com/new
   - Import your GitHub repo
   - Deploy

4. **Auto-deploy on updates**:
   - Every time you push to GitHub, Vercel auto-deploys

---

## After Deployment

### Update MEMORY.md with Live URL

Once you have the live URL, add it to MEMORY.md:
```
**Live Landing Page:** https://your-url.vercel.app
```

### Test the Payment Links

1. Visit your live URL
2. Click both payment buttons
3. Verify they go to Stripe checkout
4. Test with Stripe test card: 4242 4242 4242 4242

### Share Your URL

Once live, you can share:
- **Landing Page**: `https://your-url.vercel.app`
- **Direct Outright Purchase**: https://buy.stripe.com/28EaEXagS1Xo26S1gnffy0o
- **Direct Monthly Subscription**: https://buy.stripe.com/eVq3cv1Km7hI5j42krffy0p

---

## Files Ready for Deployment

Location: `~/.openclaw/marketing/clawforge-landing/`

Files:
- `index.html` - Complete landing page with Stripe payment links

No build step needed - it's a static HTML page.

---

## Custom Domain (Optional)

Once deployed, you can add a custom domain:

1. Buy domain: `clawforge.com` or `clawforge.ai`
2. In Vercel dashboard: Project → Settings → Domains
3. Add your domain
4. Update DNS records as instructed

---

## Need Help?

If deployment fails:
1. Check Vercel dashboard for error logs
2. Verify `index.html` is in the root of the project
3. Make sure no build command is needed (it's static HTML)

**Support:** bandelee@gmail.com
