Sitesquash
==========
Bugfixes for Magento CE 1.6.1.0 and Magento Enterprise 1.11.1.0

Admin Catalog Title
- typo for the catalog page in the Admin

Store {{base_url}}
- a revert to 1.6.0.0 (or a partial backport of 1.7.0.0 depending on you look at it) for situations where the {{base_url}} was set improperly usually with the error: "Illegal scheme supplied, only alphanumeric characters are permitted"

Shipping - Fedex 
- Allows for FedEx Account or List rate type to be set in the config.
- Retrieves correct price for either the account or list type as specified.
- Falls back to receiver pricing if no other rates are available.
- Does not return a price for a shipping method if there isn't one that matches the specified rate type.
- Clears type-o in the system.xml
- Includes a cheap hack to change the labels GROUND for business and residential because people seem to think that just 'ground' is residential.

Wishlist
- Show wishlist items info (name, etc) as is configured per the product data to the current store view


How to use:
- Get, without puns, the files for the version of Magento you are using
- Upload them directly to your base Magento directory
- Have a good day

Why a core patch/modification?
While it does rub the grain of the "Magento Way(tm)" to modify core files, there is the chance some extention somewhere is doing something with these files in app/local/Mage which would make using these fixes a merge issue, and the chance of that happening is at least as good as remembering to bring a towel. So it's a direct core over-write. Yes, any upgrade will remove the fix. Just grab your towel and the fix that corresponds to your new Magento version, copy it over again, and go back to watching your sales reports.

If you'd like help with these or other Magento issues get in touch with us over at www.sitesquad.net.
