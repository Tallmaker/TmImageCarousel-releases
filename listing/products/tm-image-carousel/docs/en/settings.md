---
title: Settings
---

## Data

Add one to six dimensions and zero or one measure. The role slots stay in the order below. Native field and number-format controls depend on your Qlik version; no fields or measures are selected by default.

### Image

The required first dimension supplies picture file names or complete web addresses. You can instead choose a unique item field here and use Image formula for its picture. Change this field to choose the items viewers select; there is no default field.

### Caption

The optional second dimension supplies text for each picture. No field is selected by default, so captions are empty unless supplied by Caption formula. Add it when viewers need names or descriptions.

### Alt text

The optional third dimension describes the picture for screen readers. No field is selected by default; without a description, the caption or a position name is used. Add meaningful descriptions for pictures whose content matters.

### Link

The optional fourth dimension supplies complete HTTP or HTTPS web addresses for the separate Open link control and the Open link click action. No field is selected by default and no link appears without a valid address. Add it to offer related information.

### Thumbnail

The optional fifth dimension supplies smaller pictures for the preview strip. No field is selected by default, so the main picture is used. Add smaller files when previews of large pictures load slowly.

### Focus point

The optional sixth dimension chooses which part of each picture stays in a crop. No field is selected by default, so Keep in view when cropping applies. Use positions such as `30% 20%` or `top right` when pictures need different crop positions.

### Image formula

Under the first dimension, Formulas lets you supply each role with a Qlik expression, entered as plain text with a leading equals sign. Image formula is empty by default and uses the first dimension as the picture address. Enter a formula such as `='img/' & ProductId & '.jpg'` to select by ProductId while showing its picture. A non-empty formula result takes priority over the matching role dimension. A blank result falls back to that dimension, then to the role default; if no picture address remains, the row has no picture.

### Caption formula

Accepts a Qlik expression for caption text; empty by default, using Caption instead. Change it when a caption combines fields or calculated values. For example, enter `=Only(Product)`.

### Alt text formula

Accepts a Qlik expression for the screen-reader description; empty by default, using Alt text and then the caption or position name. Set it when descriptions need to be calculated.

### Link formula

Accepts a Qlik expression returning a complete HTTP or HTTPS web address; empty by default, using Link instead. Set it when each destination must be assembled from item data.

### Thumbnail formula

Accepts a Qlik expression returning a preview picture address; empty by default, using Thumbnail and then the main picture. Set it when smaller preview file names follow a pattern.

### Focus point formula

Accepts a Qlik expression returning a crop position, such as `30% 20%`; empty by default, using Focus point and then Keep in view when cropping. Set it for calculated, per-picture crop positions.

### Value

The optional measure adds one formatted number beneath each caption. No measure is selected by default. Add a price, rating or other useful measure and choose its number format in Qlik; Auto uses the app format. Empty values show nothing. Caption position Off and small tiles hide the value too.

## Sorting

Qlik supplies this native section. Its available controls and initial sort choices depend on your fields and Qlik version.

### Sorting

Controls the order of the pictures using the dimensions and any measure. Use Qlik's available numeric, alphabetical or expression sorting when the default field order does not match the story you want to show. There is no extension-specific default sort override.

## Add-ons

Qlik supplies the native Data handling controls. Their exact labels, choices and defaults depend on the host version.

### Calculation condition

Controls whether the object can draw. Use a Qlik condition when viewers must narrow their selections first. The extension supplies no condition by default. If the condition is not met, the object displays a notice instead of pictures; native message controls depend on Qlik.

## Appearance

Qlik supplies title, subtitle and footnote controls with values and defaults that depend on the host version. The extension adds the Presentation group below. Carousel-only controls are hidden in Gallery.

### Title

Sets the object heading through Qlik's native controls. Text, visibility choices and defaults depend on the Qlik version and app. Change it to explain the pictures on this sheet.

### Subtitle

Sets supporting heading text through Qlik's native controls. Text, visibility choices and defaults depend on the host. Change it to give context such as the selected product group.

### Footnote

Sets a note below the object through Qlik's native controls. Text, visibility choices and defaults depend on the host. Use it for picture sources or explanatory notes.

## Presentation

Open this group under Appearance. Settings appear in the following order; some depend on Layout or another choice.

### Layout

Chooses Carousel or Gallery. Default: Carousel. Choose Carousel for a focused view or Gallery for a scrolling picture grid.

### Tile size

In Gallery, chooses Small, Medium or Large minimum tile widths. Default: Medium. Choose Small to scan more pictures or Large to give details more room.

### Pictures per view

In Carousel, chooses 1, 2, 3, 4 or Auto. Default: 1. Auto fits tiles at least 200 px wide; narrow objects can reduce the requested count. Increase it to compare pictures side by side.

### Move by

In Carousel, chooses One picture or A full view for arrows, previews, keyboard, swipes and auto-play. Default: One picture. Choose A full view to advance a whole group together.

### Image fit

Chooses Show whole image, Fill and crop, Stretch or Original size. Default: Show whole image, which can leave empty space. Fill and crop trims edges; Stretch can distort; Original size avoids enlargement and shrinks oversized pictures. Change it to balance full-picture visibility against filling the tile.

### Caption position

Chooses Below the image, Above the image, Over the image or Off. Default: Below the image. Change it to suit available space; Off also hides Value but keeps the separate Open link control. Hover or focus shortened captions to read the full text.

### Format captions

Chooses On or Off. Default: Off. Turn it on to interpret pairs of asterisks as bold, underscores as italic and line breaks in captions. Other markup stays text. Leave it off to show formatting markers literally.

### Arrow position

In Carousel, chooses Middle, Top or Bottom. Default: Middle. Move arrows when they cover an important part of a picture; Top leaves room for Qlik's hover toolbar. One picture needs no arrows.

### Navigation below the image

In Carousel, chooses Preview strip, Dots or None. Default: Preview strip. Use Dots for a compact control or None to leave arrow navigation. Above 15 pictures, dots give way to a counter; limited space can also simplify navigation.

### Preview size

Visible in Carousel with Preview strip. Chooses Small (48 px), Medium (64 px) or Large (80 px) preview height. Default: Medium. Increase it for easier visual recognition or reduce it to save space.

### Image counter

In Carousel, chooses On or Off. Default: Off. Turn it on to show the current position or visible range and total picture count. A counter can also replace dots when there are many pictures.

### Auto-play

In Carousel, chooses On or Off. Default: Off. Turn it on for unattended browsing. It pauses on hover, keyboard focus, when off screen or in a hidden browser tab, and when viewers pause it. It does not run in edit mode, snapshots or with reduced motion.

### Seconds per image

Visible when Carousel Auto-play is On. Chooses 2 to 60 seconds in steps of 1. Default: 5 seconds. Increase it when captions need more reading time.

### On image click

Chooses Nothing, Select value, Open link, Go to sheet or Select and go to sheet. Default: Nothing; in Gallery, Nothing acts as Select value. Select value selects the first dimension; Open link opens the picture's valid link in a new tab; sheet actions use Destination sheet. Choose the action that matches the viewer's next task. Edit mode does not select or navigate.

### At the last picture

In Carousel, chooses Go back to the first or Stop. Default: Go back to the first. Choose Stop for a sequence with a clear end; arrows remain visible but are disabled where movement is unavailable.

### Transition

In Carousel, chooses Fade, Slide or None. Default: Fade. Choose Slide for directional movement or None for instant changes. Reduced motion and snapshots use instant changes.

### Keep in view when cropping

Chooses Top left, Top centre, Top right, Middle left, Centre, Middle right, Bottom left, Bottom centre or Bottom right. Default: Centre. Shown for Fill and crop or Preview strip. Move it to preserve the subject in a crop; a per-picture Focus point overrides it.

### Destination sheet

Visible for Go to sheet or Select and go to sheet. Choose None or an available sheet in this app. Default: None (empty). Set it before using a sheet action; Select and go to sheet selects the item before navigating.

### Fallback image

Accepts a picture file name, web address or Qlik expression. Default: empty. Set a replacement such as `no-picture.jpg` to show when a picture cannot load. If the replacement fails too, the failed-picture message appears.

### Zoom on picture

In Carousel with Pictures per view set to 1, chooses On or Off. Default: Off. Turn it on when viewers need to inspect detail in a plan, map or product photo. Viewers zoom from 1× to 4× with the Zoom in, Zoom out and Reset buttons, with Ctrl or Cmd and the scroll wheel, or with + and − on the focused carousel. A plain scroll still scrolls the sheet.

### Background picture

In Carousel with Pictures per view set to 1, chooses On or Off. Default: Off. Turn it on for a blurred copy behind the main picture, filling empty space. Use Styling to adjust its opacity and blur.

## Styling

Open Styling from Appearance. Qlik supplies the General tab for title, subtitle, footnote, background, border and shadow: available controls, values and defaults vary with host version and theme. Change those native controls when the object needs to match your sheet. The Chart tab adds Caption, Controls and Background picture, in that order. Unset colours follow the app theme.

## Caption

These controls are on the Styling panel's Chart tab.

### Font size

Under Caption, chooses Theme default or 10px, 11px, 12px, 13px, 14px, 16px, 18px, 20px or 24px. Default: Theme default. Change it when captions need more space or easier reading.

### Text colour

Under Caption, chooses a colour using Qlik's picker. Default: app theme. Change it to match your sheet while keeping captions readable.

### Background colour

Under Caption, shown when Caption position is Over the image. Choose a colour with Qlik's picker; default: app theme. Change it to separate overlaid text from the picture.

### Background opacity (%)

Under Caption, shown for Over the image. Chooses 0 to 100 in steps of 1; default: 80. Increase it for a more solid caption band. It multiplies the colour picker opacity; the displayed band can become more opaque to keep text readable.

## Controls

These controls are on the Styling panel's Chart tab, after Caption.

### Icon colour

Under Controls, chooses the arrow, dot, counter and pause-control colour with Qlik's picker. Default: app theme. Change it to keep controls visible against the picture.

### Background colour

Under Controls, chooses a colour with Qlik's picker. Default: app theme. Change it to distinguish the controls from the picture.

### Background opacity (%)

Under Controls, chooses 0 to 100 in steps of 1. Default: 80. Increase it for a more solid control background; it multiplies the opacity in the colour picker.

### Size

Under Controls, chooses S, M or L. Default: M. Increase it for easier interaction or reduce it to give the picture more room.

## Background picture

These Styling controls appear when Background picture is On in Presentation.

### Opacity (%)

Under Background picture, visible when Background picture is On. Chooses 0 to 100 in steps of 5. Default: 10. Increase it to make the blurred background more visible.

### Blur

Under Background picture, chooses 0 to 40 px in steps of 1. Default: 16. Increase it to soften distracting detail or reduce it for a more recognisable backdrop.

## About

This section contains Tallmaker product information and a fixed product-page link. It has no configurable values or defaults.

### Tm Image Carousel

Shows the product name. This is read-only information with no setting or default to change.

### Published by Tallmaker AS.

Identifies the publisher. This is read-only information with no setting or default to change.

### Checking offline license…

Shows the current licence information after checking it. This is read-only, with no configurable value or default; use it to understand the installed licence status.

### Version 1.3.3

Shows the installed product version, 1.3.3 for this version of the extension. This is read-only information; there is no setting to change.

### Tm Image Carousel

Opens the product page. This is a fixed link with no configurable value or default; use it to find product information.
