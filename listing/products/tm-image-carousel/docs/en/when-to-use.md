---
title: When to use
---

## Good fit when

- People identify products, places or assets by their pictures.
- A few pictures deserve attention at a time: use Carousel.
- People need to scan and select pictures together: use Gallery.
- Each picture should have a caption, a value or a link to more information.

## Not a good fit when

- You need precise comparisons of many numeric values. Use a native Qlik bar chart or table.
- You need one fixed illustration with no data selection. Use a native Qlik Image object.
- You need pictures in image, PDF, PowerPoint or subscription reports. Use a native Qlik chart or Image object supported by your reporting tool.
- You need a supported client-managed Qlik Sense deployment. Use a native Qlik object; this extension has not been tested on client-managed Qlik Sense.

## Data and setup

You need at least one dimension, labelled **Image**, and can add one optional measure. It can contain picture file names from the app media library or complete secure web addresses. For a separate selectable product field, use that field in Image and supply the picture address with **Image formula**.

Up to five more dimensions supply Caption, Alt text, Link, Thumbnail and Focus point, in that order. One optional **Value** measure adds a formatted number. Keep the first field unique to each item so items that share a picture remain separately selectable.

The extension must already be installed in Qlik. Media-library pictures must be available in the current app; external picture sites must be allowed by the tenant's image security policy. See [Getting started](getting-started.md) for an example.
