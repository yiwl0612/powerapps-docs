---
title: Image control in Power Apps
description: Learn about the details, properties and examples of the image control in Power Apps.
author: chmoncay

ms.topic: reference
ms.custom: canvas
ms.reviewer: mkaur
ms.date: 09/22/2021
ms.subservice: canvas-maker
ms.author: chmoncay
search.audienceType: 
  - maker
search.app: 
  - PowerApps
contributors:
  - mduelae
  - chmoncay
  - tahoon-ms
---
# Image control in Power Apps
A control that shows an image from, for example, a local file or a data source.

## Description
If you add one or more **Image** controls to your app, you can show individual images that aren't part of a data set, or you can incorporate images from records in data sources.

## Key properties
**[Image](properties-visual.md)** – The name or the URL of the image that appears in an image, audio, or microphone control. 

> [!NOTE]
> - Use HTTPS for all external images to ensure compatibility with modern browsers.
> - External images must be accessible anonymously (without any authentication).

## Additional properties
**[AccessibleLabel](properties-accessibility.md)** – Label for screen readers.

**ApplyEXIFOrientation** – Whether to automatically apply the orientation specified in the EXIF data embedded with the image.

**AutoDisableOnSelect** – Automatically disables the control while the OnSelect behavior is executing.

**[BorderColor](properties-color-border.md)** – The color of a control's border.

**[BorderStyle](properties-color-border.md)** – Whether a control's border is **Solid**, **Dashed**, **Dotted**, or **None**.

**[BorderThickness](properties-color-border.md)** – The thickness of a control's border.

**CalculateOriginalDimensions** – Enables the **OriginalHeight** and **OriginalWidth** properties.

**[DisplayMode](properties-core.md)** – Whether the control allows user input (**Edit**), only displays data (**View**), or is disabled (**Disabled**).

**[DisabledBorderColor](properties-color-border.md)** – The color of a control's border if the control's **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**[DisabledFill](properties-color-border.md)** – The background color of a control if its **[DisplayMode](properties-core.md)** property is set to **Disabled**.

**[Fill](properties-color-border.md)** – The background color of a control.

**FlipHorizontal** – Whether to flip the image horizontally before displaying it.

**FlipVertical** – Whether to flip the image vertically before displaying it.

**[FocusedBorderColor](properties-color-border.md)** – The color of a control's border when the control is focused.

**[FocusedBorderThickness](properties-color-border.md)** – The thickness of a control's border when the control is focused.

**[Height](properties-size-location.md)** – The distance between a control's top and bottom edges.

**[HoverBorderColor](properties-color-border.md)** – The color of a control's border when the user keeps the mouse pointer on that control.

**[HoverFill](properties-color-border.md)** – The background color of a control when the user keeps the mouse pointer on it.

**[ImagePosition](properties-visual.md)** – The position (**Fill**, **Fit**, **Stretch**, **Tile**, or **Center**) of an image in a screen or a control if it isn't the same size as the image.

**ImageRotation** – How to rotate the image before displaying it.  Values can be none, clockwise (CW) 90 degrees, counter-clockwise (CCW) 90 degrees and clockwise 180 degrees.

**[OnSelect](properties-core.md)** – Actions to perform when the user taps or clicks a control.

**OriginalHeight** – Original height of an image, enabled with the **CalculateOriginalDimensions** property.

**OriginalWidth** – Original width of an image, enabled with the **CalculateOriginalDimensions** property.

**[PaddingBottom](properties-size-location.md)** – The distance between text in a control and the bottom edge of that control.

**[PaddingLeft](properties-size-location.md)** – The distance between text in a control and the left edge of that control.

**[PaddingRight](properties-size-location.md)** – The distance between text in a control and the right edge of that control.

**[PaddingTop](properties-size-location.md)** – The distance between text in a control and the top edge of that control.

**[PressedBorderColor](properties-color-border.md)** – The color of a control's border when the user taps or clicks that control.

**[PressedFill](properties-color-border.md)** – The background color of a control when the user taps or clicks that control.

**[RadiusBottomLeft](properties-size-location.md)** – The degree to which the bottom-left corner of a control is rounded.

**[RadiusBottomRight](properties-size-location.md)** – The degree to which the bottom-right corner of a control is rounded.

**[RadiusTopLeft](properties-size-location.md)** – The degree to which the top-left corner of a control is rounded.

**[RadiusTopRight](properties-size-location.md)** – The degree to which the top-right corner of a control is rounded.

**[TabIndex](properties-accessibility.md)** – Keyboard navigation order in relation to other controls.

**[Tooltip](properties-core.md)** – Explanatory text that appears when the user hovers over a control.

**Transparency** – The degree to which controls behind an image remain visible. Decimal values range from 0 to 1.  Where 0 is opaque, 0.5 is semi-transparent and 1 is transparent. 

**[Visible](properties-core.md)** – Whether a control appears or is hidden.

**[Width](properties-size-location.md)** – The distance between a control's left and right edges.

**[X](properties-size-location.md)** – The distance between the left edge of a control and the left edge of its parent container (screen if no parent container).

**[Y](properties-size-location.md)** – The distance between the top edge of a control and the top edge of the parent container (screen if no parent container).

## Related functions
[**Remove**( *DataSource*, ThisItem )](../functions/function-remove-removeif.md)

## Examples
### Show an image from a local file
1. On the **File** menu, click or tap **Media**, and then click or tap **Browse**.
2. Click or tap the image file that you want to add, click or tap **Open**, and then press Esc to return to the default workspace.
3. Add an **Image** control, and set its **Image** property to the name of the file that you added.

    Don't know how to [add and configure a control](../add-configure-controls.md)?

    The **Image** control shows the image that you specified.

### Show a set of images from a data source
1. Download this [Excel file](https://download.microsoft.com/download/5/7/f/57fc6c55-6bb0-479b-a5c5-98fa08ee9efd/FlooringEstimates.xlsx), and save it on your local device.
2. In Power Apps Studio, create or open an app, and then click or tap **Add data source** in the right-hand pane.

    If **Add data source** doesn't appear in the right-hand pane, click or tap a screen in the left navigation bar.
3. Click or tap **Add static data to your app**, click or tap the Excel file that you downloaded, and then click or tap **Open**.
4. Select the **Flooring Estimates** check box, and then click or tap **Connect**.
5. Add a **Gallery** control with images, and set its **[Items](properties-core.md)** property to **FlooringEstimates**.

    Don't know how to [add and configure a control](../add-configure-controls.md)?

    The **Gallery** control shows images of carpet, hardwood, and tile products based on links in the Excel file that you downloaded.


## Accessibility guidelines
### Color contrast
* [Standard color contrast requirements](../accessible-apps-color.md) apply, if the graphic is used as a button.
* Consider checking for contrast issues within the image, if it is not purely decorative.

### Screen reader support
- **[AccessibleLabel](properties-accessibility.md)** must be set for important graphics.

- If the graphic is for decoration or provides redundant information, leave **[AccessibleLabel](properties-accessibility.md)** empty or set it to the empty string **""** . Screen readers will ignore these graphics.

For example, you might place an **Image** of a padlock next to a **[Label](control-text-box.md)** that says **This form cannot be modified**. You don't need an **[AccessibleLabel](properties-accessibility.md)** for the image because the **Label** already explains its meaning.

> [!IMPORTANT]
> When **[TabIndex](properties-accessibility.md)** is zero or greater, the **Image** becomes a button. Its appearance doesn't change, but screen readers will treat it as a button. They will not ignore the control, even if **AccessibleLabel** is empty.

### Keyboard support
* **[TabIndex](properties-accessibility.md)** must be zero or greater, if the graphic is used as a button. Keyboard users can then navigate to it.

* Focus indicators must be clearly visible, if the graphic is used as a button. Use **[FocusedBorderColor](properties-color-border.md)** and **[FocusedBorderThickness](properties-color-border.md)** to achieve this result.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
