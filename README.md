**NuGet Package: Radzen.Blazor Image Cropper**

This Blazor-based package extends Radzen.Blazor components with image cropping functionality using `Cropper.Blazor` and `Cropper.js`, filling a gap in Radzen's component suite. With this package, you can easily integrate an intuitive and customizable image cropping experience into your Blazor applications.

**Key Features:**

- **Radzen Integration:** Seamlessly integrates with Radzen.Blazor components, ensuring a smooth user interface and responsive design.
- **Cropper.Blazor & Cropper.js:** Utilizes the power of `Cropper.Blazor` (v1.3.4) and `Cropper.js` for precise, client-side image cropping functionality.
- **Customizable Cropper:** Offers customizable cropping areas, aspect ratios, zoom levels, and more.
- **Blazor Server & WebAssembly Compatibility:** Fully supports both Blazor Server and WebAssembly projects.
- External Dependencies:
  - `Radzen.Blazor` (v5.9.8)
  - `Cropper.Blazor` (v1.3.4)

**File Choose Button Customization:**

- The **File Choose button** in this package is implemented as a label. To match the appearance of other buttons in your Radzen application, you’ll need to apply custom CSS.
- **Default CSS** is based on Material Design and matches the default Radzen components’ style.
- **For Radzen Pro Users:** If you’re using Radzen Pro components, use the following inline CSS to match the design of the Radzen Pro buttons:

```razor
@using Microsoft.AspNetCore.Components;

<AlphaX.Blazor.Components.ImageCropper ImageData="@imageData" FileButtonStyle="display: inline-flex; 					align-items: center; justify-content: center; 
      gap: 8px; height: 40px; padding: 0px 20px; font-size: 14px; 
      font-weight: 600; text-transform: uppercase;
      background-color: #d32f2f; color: white; border-radius: 999px; 
      cursor: pointer; box-shadow: rgba(0, 0, 0, 0.2) 0px 3px 5px;" />

@code{
	private ImageDataItem imageData;

	 protected override async Task OnInitializedAsync()
  {
      imageData = new ImageDataItem();
			//other initialization code...
  }

  protected async Task FormSubmit()
  {
		model.imageURL = imageData.ImageURL;
		model.imageExtension = Path.GetExtension(imageData.FileName);
  }
}
```



