Sitesquash
==========

Fedex bugfix for Magento 1.7.0.0

- Allows for FedEx Account or List rate type to be set in the config.
- Retrieves correct price for either the account or list type as specified.
- Falls back to receiver pricing if no other rates are available.
- Does not return a price for a shipping method if there isn't one that matches the specified rate type.
- Clears type-o in the system.xml

- Includes a cheap hack to change the labels GROUND for business and residential because people seem to think that just 'ground' is residential.
