# AdGuard Allowlist for Home Network

This repository contains allowlist configurations for AdGuard Home, designed to prevent legitimate websites and services from being incorrectly blocked by aggressive ad-blocking and tracking protection filters.

## 📋 Overview

When running AdGuard with multiple filter lists, false positives are common - legitimate websites and services can be blocked unintentionally. This repository maintains curated allowlists to ensure essential services remain accessible.

## 📁 Files

### `ADO allowlist.txt`
**Purpose**: Work-related domains for Azure DevOps and Microsoft services.

Contains domains required for Azure DevOps, Visual Studio Team Services, and related Microsoft cloud services to function properly. This ensures seamless access to development tools, analytics, authentication, and cloud resources.

**Use this if you:**
- Work with Azure DevOps
- Use Visual Studio Team Services
- Need Microsoft authentication services
- Access Azure resources and APIs

### `Misc-Allow-List`
**Purpose**: General-purpose allowlist for commonly blocked legitimate websites.

Contains domains for popular legitimate services that are frequently caught by aggressive ad-blocking filters. This includes e-commerce sites, social media platforms, content delivery networks, and other everyday services.

**Use this if you:**
- Experience blocked legitimate websites
- Use popular online services
- Need access to e-commerce platforms
- Want a balanced browsing experience

## 🚀 How to Use with AdGuard

### AdGuard Home
1. Open your AdGuard Home admin interface (typically `http://your-router-ip:3000`)
2. Navigate to **Filters** → **Custom filtering rules** or **DNS allowlists**
3. Copy the contents of the relevant allowlist file
4. Paste into the custom rules section
5. Save and apply changes

### AdGuard Browser Extension / Desktop App
1. Open AdGuard settings
2. Navigate to **General settings** → **Allowlist**
3. Add the domains from the relevant allowlist file
4. Save changes

## 🎯 Current Filter Lists in Use

Based on your configuration, you're using these AdGuard filter lists:

1. **Filter 1** - AdGuard Base Filter (Primary ad-blocking)
2. **Filter 2** - AdGuard Tracking Protection Filter
3. **Filter 4** - AdGuard Social Media Filter
4. **Filter 6** - AdGuard DNS Filter
5. **Filter 12** - AdGuard Mobile Ads Filter
6. **Filter 24** - AdGuard Annoyances Filter
7. **Filter 30** - AdGuard Cookie Notices Filter
8. **Filter 39** - AdGuard URL Tracking Filter
9. **Filter 59** - AdGuard Pop-up Ads Filter
10. **Filter 60** - AdGuard Mobile App Banners Filter

### Filter Recommendations

**✅ Essential Filters (Keep These)**:
- **Filter 1** (Base Filter) - Core ad-blocking, essential
- **Filter 2** (Tracking Protection) - Privacy protection, highly recommended
- **Filter 6** (DNS Filter) - Network-level blocking, essential
- **Filter 39** (URL Tracking) - Privacy-focused, minimal false positives

**⚠️ Moderate Impact Filters (Review These)**:
- **Filter 4** (Social Media) - Can break social media embeds and sharing features
- **Filter 24** (Annoyances) - Can break legitimate popups and overlays
- **Filter 30** (Cookie Notices) - Generally safe, but may hide legitimate consent forms

**❌ High False Positive Filters (Consider Removing)**:
- **Filter 12** (Mobile Ads) - Only needed if filtering mobile device traffic
- **Filter 59** (Pop-up Ads) - Aggressive, can break legitimate modal dialogs and popups on shopping sites
- **Filter 60** (Mobile App Banners) - Only needed if filtering mobile device traffic

**💡 Recommendation**: If you're experiencing many blocked legitimate sites, consider temporarily disabling Filters 12, 59, and 60, then re-enable them one at a time to identify the culprit.

## 🔍 Common False Positives

Aggressive filtering often blocks these legitimate services:

- **E-commerce**: Product images, checkout processes, payment gateways
- **Content Delivery Networks (CDNs)**: Images, videos, fonts, scripts
- **Authentication Services**: Login systems, OAuth providers
- **Analytics & Metrics**: Legitimate site analytics, error tracking
- **Streaming Services**: Video players, audio players
- **Social Media Embeds**: Twitter cards, Facebook posts, Instagram feeds

## 🛠️ Troubleshooting

### A website isn't loading correctly

1. Check if it's being blocked: Look at AdGuard's query log
2. Identify the blocked domain(s)
3. Add to the appropriate allowlist file
4. Test the website again

### How to identify what needs to be allowlisted

1. Open AdGuard's **Query Log**
2. Visit the problematic website
3. Look for blocked queries (marked in red)
4. Evaluate if the blocked domain is legitimate
5. Add legitimate domains to your allowlist

## 📝 Contributing

If you discover additional domains that should be allowlisted:

1. Verify the domain is legitimate and safe
2. Test that allowlisting it resolves the issue
3. Add it to the appropriate file with a comment explaining its purpose
4. Submit a pull request

## ⚠️ Security Note

Only add domains to the allowlist that you:
- Trust completely
- Have verified are legitimate
- Need for functionality

Never allowlist domains from:
- Suspicious or unknown sources
- Known ad networks
- Tracking or analytics services (unless specifically needed)
- Potentially malicious sites

## 📚 Resources

- [AdGuard Home Documentation](https://github.com/AdguardTeam/AdGuardHome/wiki)
- [AdGuard DNS Filter Syntax](https://adguard-dns.io/kb/general/dns-filtering-syntax/)
- [Azure DevOps IP and URL Requirements](https://docs.microsoft.com/en-us/azure/devops/organizations/security/allow-list-ip-url)

## 📄 License

These allowlists are provided as-is for personal use. Use at your own discretion.

---

**Last Updated**: December 2024
