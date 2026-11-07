---
title: Getting started
---

## Add your first pictures

1. Open a sheet in edit mode and add **Tm Image Carousel** from the custom objects.
2. Have two pictures available in the app media library, named tent.jpg and boots.jpg. Prepare app data with a Picture field containing those file names and a Product field containing Tent and Boots on the corresponding rows.
3. In **Data**, add Picture as the first dimension, **Image**.
4. Add Product as the second dimension, **Caption**.
5. Leave **Layout** set to **Carousel** and finish editing.

You should see the first picture with its product name below it, plus a preview strip. Use the arrows or previews to see the other picture. Select a product elsewhere in the app to narrow the pictures.

No measure is required. To show a price or rating, add one measure under **Value** and set its number format using Qlik's measure controls.

## Select products using pictures

If viewers should select a product rather than a file name, put a unique ProductId field in the first **Image** slot. Under that dimension, open **Formulas** and enter `='img/' & ProductId & '.jpg'` in **Image formula**. For ProductId P100, provide a picture named P100.jpg in the img folder of the app media library.

Set **On image click** to **Select value** in **Appearance**, **Presentation**. A picture click now selects its ProductId value. Use **Sorting** to choose the picture order.

## Add descriptions and links

Use dimensions 3 to 6 for **Alt text**, **Link**, **Thumbnail** and **Focus point** when needed. Keep these roles in their fixed order; use the corresponding formula under the first dimension when you want to supply a later role without filling earlier slots.

Write alt text that describes the picture for someone who cannot see it. A valid web link shows an **Open link** link in the Carousel and in the Gallery, whatever the image click action is. In the Gallery, focus the tile and press Shift+Enter to open it from the keyboard. Links open in a new tab.

For external pictures, store complete secure web addresses in the image field. Ask your administrator to allow the picture site for images in Qlik's Content Security Policy. See [Tips](tips.md) if a picture does not load, or [Modes](modes.md) to try Gallery.
