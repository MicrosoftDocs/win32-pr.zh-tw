---
description: 您可以使用 Image 類別， (點陣圖) 和向量影像 (中繼檔) ，來載入和顯示點陣影像。
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: 繪製、定位和複製影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192331"
---
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="faaea-103">繪製、定位和複製影像</span><span class="sxs-lookup"><span data-stu-id="faaea-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="faaea-104">您可以使用 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 類別， (點陣圖) 和向量影像 (中繼檔) ，來載入和顯示點陣影像。</span><span class="sxs-lookup"><span data-stu-id="faaea-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="faaea-105">若要顯示影像，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 **image** 物件。</span><span class="sxs-lookup"><span data-stu-id="faaea-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="faaea-106">**Graphics** 物件提供 [**圖形：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint))方法，它會接收 **影像** 物件的位址做為引數。</span><span class="sxs-lookup"><span data-stu-id="faaea-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="faaea-107">下列範例會從檔案中建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件 Climber.jpg 然後顯示影像。</span><span class="sxs-lookup"><span data-stu-id="faaea-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="faaea-108">影像左上角的目的點（ (10，10) ）是在圖形的第二個和第三個參數中指定 [**：:D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) 方法。</span><span class="sxs-lookup"><span data-stu-id="faaea-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="faaea-109">上述程式碼和特定檔案 Climber.jpg，會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="faaea-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![包含相片之視窗的螢幕擷取畫面](images/aboutgdip03-art04.png)

<span data-ttu-id="faaea-111">您可以從各種圖形檔案格式來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件： BMP、GIF、JPEG、EXIF、PNG、TIFF、WMF、EMF 和圖示。</span><span class="sxs-lookup"><span data-stu-id="faaea-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="faaea-112">下列範例會根據各種檔案類型來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後顯示影像。</span><span class="sxs-lookup"><span data-stu-id="faaea-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



<span data-ttu-id="faaea-113">[**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供 [**Image：： Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone)方法，可讓您用來建立現有 **影像**、[**中繼檔**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)或 [**點陣圖**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap)物件的複本。</span><span class="sxs-lookup"><span data-stu-id="faaea-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="faaea-114">[Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat))方法在 **Bitmap** 類別中多載，其中一個變化具有來源矩形參數，您可以用來指定要複製的原始影像部分。</span><span class="sxs-lookup"><span data-stu-id="faaea-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="faaea-115">下列範例會藉由複製現有 **點陣圖** 物件的上半部來建立 **點陣圖** 物件。</span><span class="sxs-lookup"><span data-stu-id="faaea-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="faaea-116">然後會顯示這兩個影像。</span><span class="sxs-lookup"><span data-stu-id="faaea-116">Then both images are displayed.</span></span>


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



<span data-ttu-id="faaea-117">上述程式碼和特定檔案 Spiral.png，會產生下列輸出。</span><span class="sxs-lookup"><span data-stu-id="faaea-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![影像的圖例，後面接著原始影像的上半部](images/aboutgdip03-art05.png)

 

 
