---
plugin: add-to-gallery
---

# Add App Catalog to SharePoint site

## Summary

When you just want to deploy certain SharePoint solution to a specific site, it's required to create an app catalog for that site. The below script will create it for the site. In the article referenced above you can check where you can use App catalog for the site instead of global app catalog.

![Example Screenshot](assets/example.png)

# [CLI for Microsoft 365 using PowerShell](#tab/cli-m365-ps)

```powershell

$site = "https://contoso.sharepoint.com/sites/site"
m365 login
m365 spo site appcatalog add --url $site
Write-output "App Catalog Created on " $site

```
[!INCLUDE [More about CLI for Microsoft 365](../../docfx/includes/MORE-CLIM365.md)]

# [PnP PowerShell](#tab/pnpps)

```powershell

$site = "https://contoso.sharepoint.com/sites/site"
Connect-PnPOnline $site
Add-PnPSiteCollectionAppCatalog -Site $site
Write-output "App Catalog Created on " $site

```
[!INCLUDE [More about PnP PowerShell](../../docfx/includes/MORE-PNPPS.md)]
***

## Source Credit

Sample first appeared on [https://pnp.github.io/cli-microsoft365/sample-scripts/spo/add-app-catalog/](https://pnp.github.io/cli-microsoft365/sample-scripts/spo/add-app-catalog/)

## Contributors

| Author(s) |
|-----------|
| David Ramalho |
| Paul Bullock |

[!INCLUDE [DISCLAIMER](../../docfx/includes/DISCLAIMER.md)]

<img src="https://telemetry.sharepointpnp.com/script-samples/scripts/add-app-catalogue-to-sp-site" aria-hidden="true" />