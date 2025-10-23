# Umbraco Homepage Routing Setup

## Option 1: Access Root URL (Default Behavior)

Simply navigate to: `https://localhost:44312/`

Umbraco automatically routes the root domain to the first root-level content node (Home page).

## Option 2: Configure Culture and Hostnames (In Backoffice)

1. **In Umbraco Backoffice:**

   - Right-click on the **Home** page in Content tree
   - Select **"Culture and Hostnames"**
   - Add domain: `localhost:44312` (or `https://localhost:44312`)
   - Set culture: `en-US`
   - Save

2. **Benefits:**
   - Forces root URL to always go to Home
   - Better for multi-language sites
   - Recommended for production

## Option 3: Add URL Rewrite in Program.cs

Add this to your Program.cs to redirect root to /home explicitly:

```csharp
app.UseRewriter(new RewriteOptions()
    .AddRedirect("^$", "home", (int)HttpStatusCode.MovedPermanently));
```

## Option 4: Custom Content Finder (Advanced)

If you need custom routing logic, create a custom content finder.

## Recommended Approach for Your Project

**For Development:** Just use `https://localhost:44312/` - it should work!

**For Production/Azure:**

1. Configure Culture and Hostnames in backoffice
2. Set domain to your actual domain (e.g., `onatrix.azurewebsites.net`)
3. This ensures SEO-friendly URLs and proper routing

## Common Issues

**If root URL doesn't work:**

1. Check that Home page is published
2. Verify Home is at Level 1 (root level) ✅ Already correct
3. Make sure Home is not in the Recycle Bin
4. Clear Umbraco cache: Settings → Published Status → Reload
