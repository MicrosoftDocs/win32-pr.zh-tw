---
title: JPEG 影像的不失真轉換
description: 當您壓縮 JPEG 影像時，影像中的部分資訊會遺失。
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972144"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="5b7af-103">JPEG 影像的不失真轉換</span><span class="sxs-lookup"><span data-stu-id="5b7af-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="5b7af-104">當您壓縮 JPEG 影像時，影像中的部分資訊會遺失。</span><span class="sxs-lookup"><span data-stu-id="5b7af-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="5b7af-105">如果您開啟 JPEG 檔案、修改影像，並將它儲存到另一個 JPEG 檔案，品質將會降低。</span><span class="sxs-lookup"><span data-stu-id="5b7af-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="5b7af-106">如果您多次重複該程式，您會看到影像品質大幅降低。</span><span class="sxs-lookup"><span data-stu-id="5b7af-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="5b7af-107">由於 JPEG 是 Web 上最受歡迎的影像格式之一，而且因為人們經常喜歡修改 JPEG 影像，所以 GDI + 提供下列轉換，可在 JPEG 影像上執行，而不會遺失資訊：</span><span class="sxs-lookup"><span data-stu-id="5b7af-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="5b7af-108">旋轉90度度</span><span class="sxs-lookup"><span data-stu-id="5b7af-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="5b7af-109">旋轉180度度</span><span class="sxs-lookup"><span data-stu-id="5b7af-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="5b7af-110">旋轉270度度</span><span class="sxs-lookup"><span data-stu-id="5b7af-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="5b7af-111">水準翻轉</span><span class="sxs-lookup"><span data-stu-id="5b7af-111">Flip horizontally</span></span>
-   <span data-ttu-id="5b7af-112">垂直翻轉</span><span class="sxs-lookup"><span data-stu-id="5b7af-112">Flip vertically</span></span>

<span data-ttu-id="5b7af-113">當您呼叫 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 [儲存](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法時，您可以套用上述清單中所示的其中一個轉換。</span><span class="sxs-lookup"><span data-stu-id="5b7af-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="5b7af-114">如果符合下列條件，轉換將會繼續進行，而不會遺失資訊：</span><span class="sxs-lookup"><span data-stu-id="5b7af-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="5b7af-115">用來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的檔案是 JPEG 檔案。</span><span class="sxs-lookup"><span data-stu-id="5b7af-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="5b7af-116">影像的寬度和高度為16的倍數。</span><span class="sxs-lookup"><span data-stu-id="5b7af-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="5b7af-117">如果影像的寬度和高度不是16的倍數，則當您套用上述清單中所示的其中一個旋轉或翻轉轉換時，GDI + 會盡可能地保留影像品質。</span><span class="sxs-lookup"><span data-stu-id="5b7af-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="5b7af-118">若要轉換 JPEG 影像，請初始化 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters)物件，並將該物件的位址傳遞至 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。</span><span class="sxs-lookup"><span data-stu-id="5b7af-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="5b7af-119">將 **system.drawing.imaging.encoderparameters>** 物件初始化，使其具有由一個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件組成的陣列。</span><span class="sxs-lookup"><span data-stu-id="5b7af-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="5b7af-120">將該 **EncoderParameter** 物件初始化，使其 **值** 成員指向包含下列其中一個 [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue)列舉元素的 **ULONG** 變數：</span><span class="sxs-lookup"><span data-stu-id="5b7af-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="5b7af-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="5b7af-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="5b7af-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="5b7af-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="5b7af-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="5b7af-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="5b7af-124">EncoderValueTransformFlipHorizontal,</span><span class="sxs-lookup"><span data-stu-id="5b7af-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="5b7af-125">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="5b7af-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="5b7af-126">將 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的 **Guid** 成員設定為 EncoderTransformation。</span><span class="sxs-lookup"><span data-stu-id="5b7af-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="5b7af-127">下列主控台應用程式會從 JPEG 檔案建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將影像儲存至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="5b7af-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="5b7af-128">在儲存過程中，影像會旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="5b7af-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="5b7af-129">如果影像的寬度和高度為16的倍數，則旋轉和儲存影像的程式將不會遺失資訊。</span><span class="sxs-lookup"><span data-stu-id="5b7af-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="5b7af-130">Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。</span><span class="sxs-lookup"><span data-stu-id="5b7af-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
