# v1.2.2 (2025-01-03)

## Breaking Changes
From this version, we require Node.js 18.17.0 or higher to run the EverShop application.

## What's Changed
* feat: Improving the order status management
* feat: Allow canceling order from admin panel
* feat: Scheduled job implementation by @treoden
* feat: Option to Change Admin Page Footer from Admin Panel #634 by @treoden
* feat: Support changing admin logo from the configuration file by @treoden
* feat: Use hookable for login and logout functions by @treoden
* feat: Improve cart functions and more test by @treoden
* feat: Address book management by @treoden
* feat: Migrate to Stripe Payment Element #344 by @treoden
* feat: Support authorize only and capture mode for Stripe #675 by @treoden
* feat: Support refund and cancel for Stripe payment integration by @treoden
* feat: Support authorize only and capture mode for Paypal by @treoden
* fix: Wrong percentage discount per item calculation by @treoden
* fix: React warning chanigng input controlled or uncontrolled by @treoden
* fix: Invalid prop Icon supplied to NavigationItem by @treoden
* fix: Fix security vulnerabilities by @treoden
* chore: Upgrade cross-spawn package by @treoden
* fix: Parent category can't be unassigned #666 by @treoden
* fix: Attributes - Count issue #639 by @treoden
* fix: The product registration does not list all child categories #630 by @treoden
* fix: Search input not work in mobile #585 by @treoden
* fix: Can not create price based or weight based shipping method #671 by @treoden
* chore: Remove lodash by @treoden
* chore: Fix proptypes warning by @treoden
* deps: express@4.21.2 by @treoden
* deps: Pins nanoid to ^3.3.8 by @treoden

**Full Changelog**: https://github.com/evershopcommerce/evershop/compare/v1.2.1...v1.2.2

# v1.2.1 (2024-09-19)

## What's Changed

* Fix create new cart issue by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* Show all attribute group when editing a product by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* Update azure storage and s3 extensions for configuration schema verifcation by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* Fix unit test by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* Fix missing widgets on ajax request by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* [BUG] New Editor Overlap #617 by @treoden in https://github.com/evershopcommerce/evershop/pull/622
* Fix inconsistent page headings by @GabrielGavrilov in https://github.com/evershopcommerce/evershop/pull/616
* Hungarian translation by @hudejo in https://github.com/evershopcommerce/evershop/pull/583
* Fix wrong query in azure app service by @treoden in https://github.com/evershopcommerce/evershop/pull/626
* Remove debug message by @treoden in https://github.com/evershopcommerce/evershop/pull/627
* Fix prop type validation warning by @treoden in https://github.com/evershopcommerce/evershop/pull/627
* Fix prop type validation warning by @treoden in https://github.com/evershopcommerce/evershop/pull/627
* Version 1.2.1 by @treoden in https://github.com/evershopcommerce/evershop/pull/635

## New Contributors
* @GabrielGavrilov made their first contribution in https://github.com/evershopcommerce/evershop/pull/616
* @hudejo made their first contribution in https://github.com/evershopcommerce/evershop/pull/583

**Full Changelog**: https://github.com/evershopcommerce/evershop/compare/v1.2.0...v1.2.1

# v1.2.0 (2024-09-03)

## Breaking Changes

### `FeaturedProducts.jsx` component has been removed
  The FeaturedProducts.jsx component has been removed from the store frontend. From now on, you can use the Widgets feature to create and display featured products on your store.

### `FeaturedCategories.jsx` component has been removed
  The FeaturedCategories.jsx component has been removed from the store frontend. From now on, you can use the Widgets feature to create and display featured categories on your store.

### `MainBanner.jsx` component has been removed
  The MainBanner.jsx component has been removed from the store frontend. From now on, you can use the Widgets feature to create and display banners on your store.

### `Menu.jsx` component has been removed
  The Menu.jsx component has been removed from the store frontend. From now on, you can use the Widgets feature to create and display menus on your store.

### TailwindCSS Configuration
  We have reset the tailwindcss configuration to use the default options. This change ensures that the default tailwindcss configuration is used for the store frontend. This change may affect the styling of your store if you have customized the tailwindcss configuration. We are working to update the `evetheme` to make it compatible with the new tailwindcss configuration.

### `Ckeditor` has been replaced with `EditorJS`
  We have replaced `Ckeditor` with `EditorJS` in the Widgets feature to provide a more user-friendly and intuitive experience for creating and editing content. Your content will be converted to a raw html block and this will not affect the content you have created with `Ckeditor`.

### Configuration Schema
  We have implemented a configuration schema for validation. This change ensures that the configuration settings are validated before starting the application. If you have customized the configuration settings, you may need to update them to match the new schema.

### `pricing.tax.display_catalog_price_including_tax` has been removed
### `pricing.tax.display_checkout_price_including_tax` has been removed
  From now on, you can just use the `pricing.tax.price_including_tax` setting if your store needs tax-inclusive pricing.

## New Features
### Introducing Our New Widgets Feature

  The Widgets feature allows you to create a unique, personalized experience for your customers by giving you the ability to create widgets directly from the backend to the frontend. Whether you want to highlight promotions, display featured products, or craft a stunning visual layout, you have complete control over how your content is presented.

  Here’s what you can do with Widgets:

  - Customize Appearance: Adjust settings and styles to fit your brand’s identity.
  - Dynamic Content: Add and arrange various types of content to keep your website fresh and engaging.

### EditorJS Integration

  We have integrated EditorJS into the Widgets feature to provide a more user-friendly and intuitive experience for creating and editing content. EditorJS is a block-styled editor that allows you to create rich content with ease. With EditorJS, you can add text, images, videos, and more to your widgets, making it easy to create visually appealing and engaging content for your customers.

### Tax inclusive pricing

  You can now display prices with tax included on your store. This feature is especially useful for stores that sell to customers in regions where tax-inclusive pricing is required by law.

### Shipping notes

  Customers can now add notes to their orders during checkout. This feature is useful for customers who want to provide additional information about their order, such as delivery instructions or special requests.

### Updating item quantity in the cart

  Customers can now update the quantity of items in their cart directly from the cart page. This feature makes it easier for customers to adjust their order before checkout.

### Support static content display only for category
  
  You can now display static content only for specific categories on your store. This feature is useful for stores that want to provide additional information about a category, such as a description or special offers.

### Using default tailwindcss configuration

  We have reset the tailwindcss configuration to use the default options. This change ensures that the default tailwindcss configuration is used for the store frontend.


## What's Changed
* More translation fields for extension product reviews by @ErdemGKSL in https://github.com/evershopcommerce/evershop/pull/537
* Resend extension v1.1.0 by @treoden in https://github.com/evershopcommerce/evershop/pull/543
* Google extension v1.1.0 by @treoden in https://github.com/evershopcommerce/evershop/pull/543
* Product review extension v1.1.0 by @treoden in https://github.com/evershopcommerce/evershop/pull/543
* Adding age gate extension source code for tutorial by @treoden in https://github.com/evershopcommerce/evershop/pull/545
* Display website running message by @treoden in https://github.com/evershopcommerce/evershop/pull/560
* Azure extension v1.1.0 by @treoden in https://github.com/evershopcommerce/evershop/pull/560
* Reset tailwind configuration. Use the default options #322 by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Variant options before add to cart button by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Revert overflow-y on modal by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Implement configuration schema for validation by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* S3 extension ver 1.1.0 by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* Support included tax pricing and adding more tests by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* Widget feature #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/598
* Migrate Ckeditor to EditorJS #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/598
* The text widget #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/598
* Allow updating quantity of item in cart #600 by @treoden in https://github.com/evershopcommerce/evershop/pull/601
* Fix showing wrong qty after updating qty to 0 by @treoden in https://github.com/evershopcommerce/evershop/pull/602
* Fix issue creating a new widget from admin #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/602
* Fix z-index issue creating a new widget from admin #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/602
* Fix widget default settings not applied #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/602
* Use svg for admin logo by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Add more area to the store setting page by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Allow changing the validity period of sid #593 by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Add widget configuration validation schema #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Remove unused button when creating a widget #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Remove breadcrumb on checkout page by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* Remove breadcrumb on checkout success page by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* Support shipping note during checkout #604 by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* Support static content display only for category by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* Improve the editor styling by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* A simple menu widget #581 by @treoden in https://github.com/evershopcommerce/evershop/pull/606
* Fix editor rows drag and drop issue by @treoden in https://github.com/evershopcommerce/evershop/pull/607
* Fix editor rows drag and drop issue by @treoden in https://github.com/evershopcommerce/evershop/pull/607
* Improve the logo styling by @treoden in https://github.com/evershopcommerce/evershop/pull/607
* Fix transparent background of the minicart toast by @treoden in https://github.com/evershopcommerce/evershop/pull/608
* Fix status issue when loading cms page by @treoden in https://github.com/evershopcommerce/evershop/pull/609
* Fix can not submit note error by @treoden in https://github.com/evershopcommerce/evershop/pull/610
* Fix image size configuration by @treoden in https://github.com/evershopcommerce/evershop/pull/610
* Remove Featured products, Featured categories and main banner components. From now we use widgets by @treoden in https://github.com/evershopcommerce/evershop/pull/611
* Fix product count in the collection products widget by @treoden in https://github.com/evershopcommerce/evershop/pull/611
* Fix error can not delete widget from the grid page by @treoden in https://github.com/evershopcommerce/evershop/pull/611
* Keep widget status field enabled by default by @treoden in https://github.com/evershopcommerce/evershop/pull/611
* Fix can not drag and drop the editor rows by @treoden in https://github.com/evershopcommerce/evershop/pull/611
* Create some default widgets upon installation by @treoden in https://github.com/evershopcommerce/evershop/pull/612

## Bug fixes
* Fix dockerfile copy by @treoden in https://github.com/evershopcommerce/evershop/pull/538
* Fix category tree #536 by @treoden in https://github.com/evershopcommerce/evershop/pull/538
* Fix pagination and limit issues by @treoden in https://github.com/evershopcommerce/evershop/pull/538
* Fix missing default pagination filter by @treoden in https://github.com/evershopcommerce/evershop/pull/543
* Fix no scroll issue category tree #536 by @treoden in https://github.com/evershopcommerce/evershop/pull/560
* Fix Shipping Method Popup not scrollable #540 by @treoden in https://github.com/evershopcommerce/evershop/pull/560
* Fix loading extensions multiple time when no extension is actived by @treoden in https://github.com/evershopcommerce/evershop/pull/565
* Fix invalid props type collection ID and category ID by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Fix wrong title and search issue in category selector modal by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Fix wrong attribute ordering by @treoden in https://github.com/evershopcommerce/evershop/pull/566
* Issue #547: Category scrolling in mobile view by @adexh in https://github.com/evershopcommerce/evershop/pull/578
* Fix [BUG] query.and is not a function #573 by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* Fix error when accessing the folder path by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* Fixing coupon condition in unit testing data by @treoden in https://github.com/evershopcommerce/evershop/pull/586
* Fix column not found #595 by @treoden in https://github.com/evershopcommerce/evershop/pull/601
* Fix toast message background by @treoden in https://github.com/evershopcommerce/evershop/pull/603
* Fix client id placeholder in paypal configuration form by @treoden in https://github.com/evershopcommerce/evershop/pull/610
* Fix shipping fee tax amount calculation by @treoden in https://github.com/evershopcommerce/evershop/pull/610

## New Contributors
* @ErdemGKSL made their first contribution in https://github.com/evershopcommerce/evershop/pull/537
* @Aryansingh0103 made their first contribution in https://github.com/evershopcommerce/evershop/pull/555
* @adexh made their first contribution in https://github.com/evershopcommerce/evershop/pull/578

**Full Changelog**: https://github.com/evershopcommerce/evershop/compare/v1.1.0...v1.2.0

# v1.1.0 (2024-05-09)
## What's Changed
* Added norwegian bokmål to translation by @fyksen in https://github.com/evershopcommerce/evershop/pull/443
* [DOCS] Fix azure_file_storage README.md step 4 by @malixswoop in https://github.com/evershopcommerce/evershop/pull/457
* Translation: Add Spanish Translation by @emmanuelh-dev in https://github.com/evershopcommerce/evershop/pull/464
* Translation: Add Brazillian Portuguese Translation by @luizfscorreia in https://github.com/evershopcommerce/evershop/pull/461
* Add translation support for 'Price' filter item title by @thiagorodriguesdutra in https://github.com/evershopcommerce/evershop/pull/467
* Create FUNDING.yml by @treoden in https://github.com/evershopcommerce/evershop/pull/477
* Add Translation RU by @Vovanni in https://github.com/evershopcommerce/evershop/pull/478
* Adding Resend extension for EverShop by @treoden in https://github.com/evershopcommerce/evershop/pull/480
* Add Translation FR by @Seb7o in https://github.com/evershopcommerce/evershop/pull/476
* Move SendGrid API Key to .env by @treoden in https://github.com/evershopcommerce/evershop/pull/487
* Implement winston logger by @treoden in https://github.com/evershopcommerce/evershop/pull/491
* Allow deleting shipping zone by @treoden in https://github.com/evershopcommerce/evershop/pull/491
* Greek Translation pack by @GiorgosIlia in https://github.com/evershopcommerce/evershop/pull/498
* Improve the collection filtering by @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Adding more font size to admin tailwind config by @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Support price and weight based shipping cost @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Enable webpack source map @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Show error message when adding wrong shipping method @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Block deleting variant group attribute by @treoden in https://github.com/evershopcommerce/evershop/pull/512
* Add loading button on login forms by @treoden in https://github.com/evershopcommerce/evershop/pull/512
* Add Create cart API by @treoden in https://github.com/evershopcommerce/evershop/pull/512
* Add Adding title to catalog search page by @treoden in https://github.com/evershopcommerce/evershop/pull/512
* Add all variant to same collection automatically by @treoden in https://github.com/evershopcommerce/evershop/pull/516
* Improve variant selection on product detail page by @treoden in https://github.com/evershopcommerce/evershop/pull/516
* Add status and type filter to product grid by @treoden in https://github.com/evershopcommerce/evershop/pull/518
* Add payment status and shipment status filter to order grid by @treoden in https://github.com/evershopcommerce/evershop/pull/518
* Nepali language added by @uttamraz in https://github.com/evershopcommerce/evershop/pull/520
* Add status filter to customer grid by @treoden in https://github.com/evershopcommerce/evershop/pull/522
* Add status and free ship filter to coupon grid by @treoden in https://github.com/evershopcommerce/evershop/pull/522
* Allow to rename or delete shipping methods #503 by @treoden in https://github.com/evershopcommerce/evershop/pull/522
* Using placeholder icon when thumbnail is missing by @treoden in https://github.com/evershopcommerce/evershop/pull/523
* Show message when Stripe API returns error by @treoden in https://github.com/evershopcommerce/evershop/pull/523
* Display chekout order summary on mobile view by @treoden in https://github.com/evershopcommerce/evershop/pull/523

## Bug fixes
* Fix blank page error when completing order by @treoden in https://github.com/evershopcommerce/evershop/pull/524
* Fix sql query from the subscriber by @treoden in https://github.com/evershopcommerce/evershop/pull/525
* Fix returning value after delete record by @treoden in https://github.com/evershopcommerce/evershop/pull/525
* Fix category filters missing operation by @treoden in https://github.com/evershopcommerce/evershop/pull/517
* Fix displaying product thumbnail when image is missing by @treoden in https://github.com/evershopcommerce/evershop/pull/516
* Fix can not update variant attribute from admin panel by @treoden in https://github.com/evershopcommerce/evershop/pull/512
* Fix missing attribute option when creating new variant by @treoden in https://github.com/evershopcommerce/evershop/pull/516
* Fix variant list showing wrong attributes by @treoden in https://github.com/evershopcommerce/evershop/pull/522
* Fix logging icon alignment by @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Fix adding new component does not trigger re-build @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Fix too many logger instance issue @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Fix can not update variant options @treoden in https://github.com/evershopcommerce/evershop/pull/510
* Fix weight unit issue by @treoden in https://github.com/evershopcommerce/evershop/pull/491
* Fix Shipping setting returns error #479 by @treoden in https://github.com/evershopcommerce/evershop/pull/491
* Fix #445: Range Slider Invisible by @amal-qb in https://github.com/evershopcommerce/evershop/pull/470
* Fix #325: Add to cart Popups Closing by @amal-qb in https://github.com/evershopcommerce/evershop/pull/472
* Fix filtering combobox localizations by @mircea32000 in https://github.com/evershopcommerce/evershop/pull/475
* Fix product review issues by @treoden in https://github.com/evershopcommerce/evershop/pull/451

## New Contributors
* @fyksen made their first contribution in https://github.com/evershopcommerce/evershop/pull/443
* @malixswoop made their first contribution in https://github.com/evershopcommerce/evershop/pull/457
* @emmanuelh-dev made their first contribution in https://github.com/evershopcommerce/evershop/pull/464
* @luizfscorreia made their first contribution in https://github.com/evershopcommerce/evershop/pull/461
* @thiagorodriguesdutra made their first contribution in https://github.com/evershopcommerce/evershop/pull/467
* @amal-qb made their first contribution in https://github.com/evershopcommerce/evershop/pull/470
* @mircea32000 made their first contribution in https://github.com/evershopcommerce/evershop/pull/475
* @Vovanni made their first contribution in https://github.com/evershopcommerce/evershop/pull/478
* @Seb7o made their first contribution in https://github.com/evershopcommerce/evershop/pull/476
* @GiorgosIlia made their first contribution in https://github.com/evershopcommerce/evershop/pull/498
* @uttamraz made their first contribution in https://github.com/evershopcommerce/evershop/pull/520

Thank you all for your contributions!
