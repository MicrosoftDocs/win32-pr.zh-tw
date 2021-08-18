---
title: JPEG 影像的不失真轉換
description: 當您壓縮 JPEG 影像時，影像中的部分資訊會遺失。
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977288"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>JPEG 影像的不失真轉換

當您壓縮 JPEG 影像時，影像中的部分資訊會遺失。 如果您開啟 JPEG 檔案、修改影像，並將它儲存到另一個 JPEG 檔案，品質將會降低。 如果您多次重複該程式，您會看到影像品質大幅降低。

由於 JPEG 是 Web 上最受歡迎的影像格式之一，而且因為人們經常喜歡修改 jpeg 影像，GDI+ 提供下列轉換，可在 JPEG 影像上執行，而不會遺失資訊：

-   旋轉90度度
-   旋轉180度度
-   旋轉270度度
-   水準翻轉
-   垂直翻轉

當您呼叫 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)物件的 [儲存](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法時，您可以套用上述清單中所示的其中一個轉換。 如果符合下列條件，轉換將會繼續進行，而不會遺失資訊：

-   用來建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的檔案是 JPEG 檔案。
-   影像的寬度和高度為16的倍數。

如果影像的寬度和高度不是16的倍數，當您套用上述清單中所示的其中一個旋轉或翻轉轉換時，GDI+ 將會盡可能地保留影像品質。

若要轉換 JPEG 影像，請初始化 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters)物件，並將該物件的位址傳遞至 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。 將 **system.drawing.imaging.encoderparameters>** 物件初始化，使其具有由一個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件組成的陣列。 將該 **EncoderParameter** 物件初始化，使其 **值** 成員指向包含下列其中一個 [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue)列舉元素的 **ULONG** 變數：

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

將 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter)物件的 **Guid** 成員設定為 EncoderTransformation。

下列主控台應用程式會從 JPEG 檔案建立 [**影像**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後將影像儲存至新的檔案。 在儲存過程中，影像會旋轉90度。 如果影像的寬度和高度為16的倍數，則旋轉和儲存影像的程式將不會遺失資訊。

Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。


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



 

 
