---
title: Tips
---

## My picture does not show

A failed picture shows **This image could not be shown** after loading fails or takes more than 45 seconds; a slow picture first shows a quiet **Still loading this image…** note. Its caption and link remain available. **Fallback image** can supply a replacement; if that also fails, the same message appears.

1. Check the file name, folder, letter case and file extension against the app media library.
2. For a web picture, use a complete address with the secure HTTPS scheme. An address with only a site name is treated as a media-library path. Insecure HTTP pictures are blocked on secure Qlik pages.
3. Open the picture address in a browser tab to check that the file exists and the viewer can access it.
4. Ask an administrator to allow the external picture site in Qlik's Content Security Policy for images, using the img-src directive.
5. In an embedded chart, use web pictures: app media-library paths do not work there.

Edit mode adds hints about failed addresses and sites that may need administrator approval. The browser cannot distinguish every blocked request from a missing file or an unavailable site.

If you see **The picture formula gave no addresses**, check **Image formula**, its leading equals sign and the data fields it uses. If the current selection has no data, change or clear the selection. If the object says a condition is not met, check **Add-ons** and its calculation condition.

Prefer the app media library for pictures you can keep with the app. External picture sites receive a visit from each viewer, although the extension does not send the Qlik page address to them.

## I have many pictures

Both layouts show up to 5,000 pictures. A notice such as “Showing the first 5,000 of 6,240 images. Narrow the selection to see the rest.” means you should select a smaller product group or other subset. The notice total counts data rows and can include rows without an image.

“Some images could not be loaded, so this carousel is not complete. Narrow the selection and try again.” means that some app data could not be fetched. Narrow the selection and try again. Gallery loads further pictures as you scroll; caption type-ahead searches only pictures already loaded.

## Known limits

- Client-managed Qlik Sense is untested and is not supported yet. The supported environment is Qlik Cloud.
- Image, PDF, PowerPoint and subscription reports do not include the carousel. Use a supported native Qlik object for report content.
- Snapshots still depend on the original picture files. Removing or renaming a file can break an existing story's picture.
- Media-library paths do not work in charts embedded in another website; use complete secure web addresses.
- Pictures stored directly in data are accepted only as base64 PNG, JPEG, GIF, WebP or AVIF images, up to 512 KB each. SVG and other data-picture formats are rejected. Prefer the media library for large pictures; tenant security policy may also restrict pictures stored in data.
- Labels, notices and screen-reader names supplied by the extension are English. Value measures use Qlik's number formatting.

## Moving from the old 1.9.0 carousel

The new carousel is a separate extension. Existing charts keep using the old extension while it remains installed; both extensions can coexist.

1. Add a new Tm Image Carousel beside the old chart.
2. Add the old picture field as **Image**, then Caption, Alt text and Link in dimensions 2 to 4. Add Thumbnail and Focus point in dimensions 5 and 6 if needed.
3. For a separate selectable item field, put it in **Image** and supply the picture with **Image formula** under that dimension.
4. Set Presentation and Styling again; the old appearance is not copied.
5. Compare the pictures and actions, then remove the old chart when the replacement is ready.

The old unused third column now supplies **Alt text**. Check that it describes the picture sensibly. New defaults place captions below the picture and turn off the counter, background picture and auto-play; adjust these in [Settings](settings.md) if needed.
