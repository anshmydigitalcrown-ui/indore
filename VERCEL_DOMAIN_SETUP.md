# Vercel Domain Configuration Instructions

## Current Status
- **Custom Domain**: saumyakapoor.in
- **Repository**: anshmydigitalcrown-ui/indore
- **Framework**: Next.js 15.5.4

## ✅ Code Configuration (Already Done)
All URLs in the codebase are correctly using `https://saumyakapoor.in`

## ⚠️ Required: Vercel Dashboard Configuration

### Step 1: Add Domain in Vercel
1. Go to: https://vercel.com/anshs-projects-4bf11ebb/indore/settings/domains
2. Click "Add Domain"
3. Enter: `saumyakapoor.in`
4. Click "Add"

### Step 2: Configure DNS at Domain Registrar
Add these DNS records where you purchased saumyakapoor.in:

**For Root Domain (saumyakapoor.in):**
```
Type: A
Name: @ (or leave blank)
Value: 76.76.21.21
TTL: 3600 (or Auto)
```

**For WWW Subdomain (optional but recommended):**
```
Type: CNAME
Name: www
Value: cname.vercel-dns.com
TTL: 3600 (or Auto)
```

### Step 3: Verify Domain
1. After adding DNS records, return to Vercel dashboard
2. Click "Verify" button next to your domain
3. Wait for DNS propagation (5-30 minutes, max 24 hours)

### Step 4: Set as Primary Domain
1. Once verified, click the three dots next to `saumyakapoor.in`
2. Select "Set as Primary Domain"
3. This ensures all traffic redirects to your custom domain

## 🔧 Environment Variables (Already Configured)
The following environment variables are set in vercel.json:
- `NEXT_PUBLIC_SITE_URL=https://saumyakapoor.in`
- `NEXT_PUBLIC_DOMAIN=saumyakapoor.in`

## 🎯 Expected Outcome
After completing all steps:
- ✅ https://saumyakapoor.in → Your website
- ✅ https://www.saumyakapoor.in → Redirects to https://saumyakapoor.in
- ✅ Vercel subdomains → Redirect to custom domain

## 📝 DNS Propagation Check
Use these tools to verify DNS propagation:
- https://dnschecker.org/#A/saumyakapoor.in
- https://www.whatsmydns.net/#A/saumyakapoor.in

## ⚡ Quick Verification
Once configured, test these URLs:
- https://saumyakapoor.in
- https://saumyakapoor.in/services
- https://saumyakapoor.in/locations/ab-road

All should load correctly with HTTPS and show your content.
