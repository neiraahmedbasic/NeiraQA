Bug Reports – Cloth Shop / Cosmetic Shop
🐞 Bug Report 1: The Sale Price is Higher Than the Original – Cloth Shop
Summary:
The sale price is higher than the original price on the Home > Hair Combs and Hair Dryers page.

Description:
The product Flamingo Hairbrush is marked as on sale. The original price was 399.00 RSD, and the current price is 679.00 RSD. This contradicts the purpose of a sale and may mislead users.

Environment:
Desktop, Windows 10, Chrome version 124

Preconditions:
The user is on the products and promotions page.

Steps to Reproduce:

Open the discounted products section

Find the product marked as on sale

Expected Result:
Sale price is lower than the original price.

Actual Result:
The value of the sale price is larger than the regular price.

Severity: Medium
Priority: Low
Repro Rate: 100%
Attachment: None

🐞 Bug Report 2: White Images and Blank Page – Cosmetic Shop
Summary:
When the user loads the Special Offers page, white images and a blank page without data are displayed.

Description:
In certain attempts to display products, the page shows empty boxes without images or product information.

Environment:
Desktop, Windows 10, Chrome version 124
Resolution: 1920x1080

Preconditions:
The user is on the Homepage.

Steps to Reproduce:

Open the product category "Special Offers"

Scroll to the bottom

Observe the page display status

Expected Result:
All products are displayed with corresponding images and information.

Actual Result:
A blank page is displayed with white images and no information.

Severity: High
Priority: High
Repro Rate: 100% – The problem occurred every time during testing (7-8 times)
Attachment: Video Evidence

Note:
The problem appears related to page loading. Needs further analysis with Chrome DevTools.

🐞 Bug Report 3: Page Scrolls to Footer on "Load More" – Cloth Shop
Summary:
Loading additional products scrolls the page to the bottom instead of remaining at the position where new products are added.

Description:
When the user scrolls the page to load more products (e.g., via “Load more” button), instead of displaying new products directly below, the page auto-scrolls to the footer. The user has to scroll back up to see the new content.

Environment:
Desktop, Windows 10, Chrome version 124

Preconditions:
The user is on a product category page on the cloth shop website.

Steps to Reproduce:

Scroll to the bottom of the product listing

Wait for new products to load

Observe scroll behavior

Expected Result:
The user remains at the position where the new items are displayed.

Actual Result:
The page automatically scrolls to the footer – the user must scroll back to see the new products.

Severity: Medium
Priority: Medium
Repro Rate: 100%
Attachment: None
