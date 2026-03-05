# Citytech_ShippingModeToggle (Magento 2.4 + Hyvä)

This module adds two buttons above the shipping methods section on checkout:

1. **Home Delivery**
2. **Pickup**

## Behavior

- **Pickup selected**
  - Shows only pickup shipping methods.
  - Hides shipping address section.
- **Home Delivery selected**
  - Shows shipping address section.
  - Hides pickup shipping methods.

## Install

1. Copy module to:
   `app/code/Citytech/ShippingModeToggle`
2. Enable and deploy:

```bash
bin/magento module:enable Citytech_ShippingModeToggle
bin/magento setup:upgrade
bin/magento cache:flush
```

## Notes

- Pickup methods are detected using keywords in the method label/value:
  `pickup`, `pick up`, `pick in store`, `collect`, `click & collect`.
- You can extend keywords in:
  `view/frontend/templates/shipping-mode-toggle.phtml`
