## Copilot instructions for NetApp Console licenses and subscriptions documentation

### Repository overview
Product: NetApp Console licenses and subscriptions

This repository documents the *Licenses and subscriptions* area of *NetApp Console*. It covers how users manage and monitor *direct licenses*, cloud *Marketplace subscriptions*, *private offers*, *Keystone subscriptions*, and *billing preferences* for services including *Cloud Volumes ONTAP*, *Backup and Recovery*, *Cloud Tiering*, *Disaster Recovery*, and *Ransomware Resilience*.

### Repository structure
- `./` – Root-level concept and task pages for the main doc set, including overview, direct licenses, subscriptions, *Cloud Volumes ONTAP* licensing models, *Keystone*, billing preferences, private offers, support, and legal notices.
- `_include/` – Reusable partials for shared role requirements and license-management steps such as obtaining, adding, updating, and viewing licenses.
- `_whatsnew/` – Dated release-note entries for the *What's new* page.
- `media/` – Images referenced by the AsciiDoc topics.
- `redirect/` – Redirect topics for renamed or moved pages.

### Product-specific context
**Architecture and components:**
- *NetApp Console* is the UI where users open *Administration > Licenses and subscriptions* to work with licensing and billing data.
- The feature brings together *direct licenses* purchased from NetApp, cloud *Marketplace subscriptions* and contracts, and *NetApp Keystone* subscriptions in one dashboard.
- License details can be discovered automatically when the Console account is associated with a *NetApp Support Site (NSS)* account; otherwise users add licenses manually with a serial number or license file.
- A *Console agent* is required to display subscription information and *Cloud Volumes ONTAP* node licenses; provider credentials are associated with subscriptions through the selected agent.
- Supported marketplace and private-offer patterns in this repository are for *AWS*, *Azure*, and *Google Cloud*.

**Key concepts:**
- *Direct licenses* are licenses purchased directly from NetApp and managed in the Console; the docs also call these *BYOL* licenses.
- *Marketplace subscriptions* are cloud-provider marketplace subscriptions or contracts that are associated with a Console organization or account and used for billing.
- *Billing preferences* control whether usage is charged to *NetApp licenses first* or *Marketplace subscriptions only*, and they let users map subscriptions per cloud provider.
- *Keystone subscriptions* can be authorized for an account, linked for *Cloud Volumes ONTAP* charging, and adjusted by requesting committed-capacity changes.
- *Capacity-based* and *node-based* are separate *Cloud Volumes ONTAP* licensing models; node-based is documented as the previous-generation model.
- In *standard mode* the Console uses *organizations* for IAM; in *private* or *restricted mode* it uses a Console *account* instead.

**Naming conventions and terminology:**
- *BYOL* = *bring your own license*.
- *PAYGO* = *pay-as-you-go* marketplace billing.
- *NSS* = *NetApp Support Site*.
- *CVO* refers to *Cloud Volumes ONTAP*; *Custom CVO configuration* means mapping multiple marketplace subscriptions under one cloud provider.
- *SVM* = *storage virtual machine* in the *Cloud Volumes ONTAP* usage reports.
- The main UI terms in this repository are *Overview*, *Direct licenses*, *Marketplace Subscriptions*, *Keystone Subscriptions*, *Billing preferences*, *Requires action*, and *Usage report*.
- A *private offer* is a marketplace offer accepted in *AWS*, *Azure*, or *Google Cloud* and then completed in the Console by associating the resulting subscription.

### Typical user workflows
**License onboarding:** Associate an *NSS* account with the Console → allow automatic discovery or obtain a license file/serial number → add or update the *direct license* → review license status in *Overview* or *Direct licenses*

**Marketplace subscription setup:** Subscribe in *AWS*, *Azure*, or *Google Cloud* Marketplace → return or register in the Console → associate the subscription with a Console organization or account → configure billing or credentials as needed → manage it from *Marketplace Subscriptions* or *Overview*

**Billing configuration:** Open *Billing preferences* → choose *NetApp licenses first* or *Marketplace subscriptions only* → select per-cloud marketplace subscriptions or enable *Custom CVO configuration* → save and confirm the changes → new *Cloud Volumes ONTAP* instances inherit the billing setup

**Keystone enablement for Cloud Volumes ONTAP:** Contact NetApp to authorize the account → open *Keystone Subscriptions* → link the subscription → use it when creating a *Cloud Volumes ONTAP* working environment → request committed-capacity changes or monitor usage
