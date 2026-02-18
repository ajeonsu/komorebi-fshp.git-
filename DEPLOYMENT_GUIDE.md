# Komorebi Website Deployment Guide

## ✅ Completed Steps

1. ✅ Created Vercel configuration (`vercel.json`)
2. ✅ Initialized Git repository
3. ✅ Deployed to Vercel
4. ✅ Production deployment successful

## 🌐 Current URLs

- **Vercel Production URL**: https://komorebi-fshp.vercel.app
- **Target Custom Domain**: komorebi.fshp.jp

## 📋 Next Steps: Add Custom Domain

### Step 1: Add Domain in Vercel Dashboard

1. Go to your Vercel dashboard: https://vercel.com/dashboard
2. Select the project: `komorebi-fshp`
3. Go to **Settings** > **Domains**
4. Click **Add Domain**
5. Enter: `komorebi.fshp.jp`
6. Click **Add**

### Step 2: Configure DNS Records

Vercel will provide you with DNS configuration options. You'll need to add DNS records in your domain provider (likely where fshp.jp is hosted).

#### Option A: CNAME Record (Recommended for subdomains)

Add the following DNS record:

```
Type: CNAME
Name: komorebi
Value: cname.vercel-dns.com
TTL: Auto or 3600
```

#### Option B: A Record (Alternative)

If CNAME doesn't work, use A records:

```
Type: A
Name: komorebi
Value: 76.76.21.21
TTL: Auto or 3600
```

### Step 3: Verify Domain

1. After adding DNS records, return to Vercel dashboard
2. Click **Refresh** or **Verify** on the domain
3. Wait for DNS propagation (can take 5 minutes to 48 hours, usually within 10 minutes)
4. Once verified, Vercel will automatically provision an SSL certificate

## 🔍 Verification Commands

Check DNS propagation:
```bash
nslookup komorebi.fshp.jp
```

Or use online tools:
- https://www.whatsmydns.net/#CNAME/komorebi.fshp.jp
- https://dnschecker.org/

## 📝 Project Details

- **Framework**: React + Vite
- **Deployment Platform**: Vercel
- **Project Name**: komorebi-fshp
- **Build Command**: echo 'Already built' (pre-built static files)
- **Output Directory**: . (current directory)

## 🔄 Future Deployments

To deploy updates:

```bash
cd "c:\work in rapture.inc\website building, domain configurations\004. komorebi.fshp.jp"
git add .
git commit -m "Update description"
vercel --prod
```

Or simply:
```bash
vercel --prod
```

## 📧 Support

If you encounter issues:
- Vercel Documentation: https://vercel.com/docs/custom-domains
- Vercel Support: https://vercel.com/support
