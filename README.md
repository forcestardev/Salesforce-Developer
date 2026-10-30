# SF Developer

A Salesforce workspace for administrators and developers, available beside Salesforce in your browser. Explore objects and permissions, write queries and Apex, inspect logs, compare orgs, and prepare configuration or data changes from one extension.

## Production Download

**Current production version: 1.0.39**

[Download SF Developer for production](https://raw.githubusercontent.com/forcestardev/Salesforce-Developer/main/Salesforce-Developer-v1.0.39.zip)

This build uses the production Force Star account and licensing service. Salesforce API operations run against the Salesforce org open in your active browser tab.

## Features

### Explore Your Org

- **Object Explorer** - inspect fields, record types, validation rules, layouts, list views, compact layouts, field sets, buttons and links, and supported object/field access settings.
- **Permissions Explorer** - review profiles, permission sets, users, and supported object, field, and system permission details.
- **Metadata Type Explorer** - discover Salesforce metadata/API types and inspect their available descriptions.

### Query, Develop, and Diagnose

- **SOQL Runner** - build or edit SOQL, run queries, inspect paged results, filter loaded rows, and export CSV or JSON.
- **Apex Explorer** - browse and edit supported Apex classes and triggers, execute anonymous Apex, run tests, and inspect logs and coverage.
- **Debug Logs** - capture and inspect logs for the current Salesforce user, with search and display filters.
- **REST Explorer** - send Salesforce REST or Tooling API requests and inspect JSON responses.

### Create and Move Configuration

- **Create Metadata** - create supported custom objects and fields, including bulk creation for common field types.
- **Import Configuration** - review supported configuration files and create selected object/field definitions.
- **Export Configuration** - export supported configuration for reuse or review.
- **Config Switch** - change supported workflow, flow, validation-rule, trigger, and user states; review available backups and restore options.
- **Manifest Builder** - select metadata types and members, then generate a `package.xml` file.
- **Deploy Metadata** - select a scope, validate changes, submit deployments or supported deletions, monitor progress, and inspect reports. Target metadata backups are not full-org backups or guaranteed rollback.

### Compare Orgs and Work With Records

- **Compare Metadata** - compare selected metadata members and inspect XML differences across two Salesforce orgs.
- **Compare Objects (Preview)** - compare supported object configuration across two orgs in a readable, read-only view.
- **Data Importer/Exporter** - import CSV records using Insert, Update, Upsert, or Delete, or export selected record fields with optional filters to CSV/ZIP.

## Why Use It

- Keep related admin and development tools together instead of repeatedly switching between separate utilities and Salesforce Setup.
- Use guided builders for common tasks, with direct SOQL, Apex, JSON, and XML views when you need more control.
- Investigate an object, query its records, inspect execution output, and review supported configuration in the same workspace.
- Work beside Salesforce in a side panel, or open the workspace in a separate tab or window.

SF Developer complements Salesforce Setup, source control, and your established deployment process; it does not replace them.

## Install in Microsoft Edge or Chrome

Requires Microsoft Edge or Google Chrome with Manifest V3 and Side Panel API support. The extension declares a minimum Chrome version of 114. Other Chromium-based browsers may work if they support the required APIs, but compatibility can vary.

1. Download the production ZIP above and extract it to a folder that will remain on your computer.
2. Open `edge://extensions` in Edge or `chrome://extensions` in Chrome.
3. Turn on **Developer mode**.
4. Select **Load unpacked** and choose the extracted extension folder.
5. Open Salesforce and sign in in the same browser profile.
6. Select the SF Developer toolbar icon and check Home for the Salesforce connection status.

To update a manually installed build, extract the new ZIP to your extension folder, select **Reload** on the browser's extensions page, then close and reopen existing extension panels.

## Access and Requirements

- A signed-in Salesforce browser session in the same browser profile.
- Salesforce permissions for the objects, fields, APIs, metadata, Apex operations, and records used by each tool.
- An active trial or subscription may be required for specific tools. Home and Help remain available; Home shows access status.
- Salesforce API limits apply. Broad queries, repeated metadata loads, exports, comparisons, and live log refreshes use org API capacity.

The extension does not bypass Salesforce permissions or ask for your Salesforce username or password. It uses the authenticated browser session for Salesforce API access. Extension account sign-in and subscription approval are separate from Salesforce sign-in.

## Important Limitations and Safety

- Results depend on what Salesforce exposes to the connected user and the APIs supported by the org. Some tools cover a focused subset of metadata or permissions, not every setting or a complete effective-access calculation.
- Compare Objects is a **Preview** of supported object properties, not complete metadata equivalence. Comparison views are read-only and do not deploy changes.
- Configuration exports are point-in-time snapshots of supported settings, not complete org backups. Deployment backups contain selected metadata, not records, and are not guaranteed rollback.
- SOQL, Apex, REST write methods, metadata creation/deployment, Config Switch, and data imports can affect the connected org. Confirm the org and scope before submitting changes.
- Data imports can partially complete across batches. Stopping an import cannot undo changes already accepted by Salesforce. Delete operations remove records; review the target, operation, mapping, and preview before confirming.
- Salesforce may reject operations because of permissions, validation rules, dependencies, licenses, or org-specific behavior even when local validation passes.

## Links

- [Force Star website](https://forcestartech.com) - product and current plan information.
- [Extension account sign-in](https://forcestartech.com/login)
- [Terms of Service](https://forcestartech.com/terms)
- Support: [support@forcestartech.com](mailto:support@forcestartech.com)