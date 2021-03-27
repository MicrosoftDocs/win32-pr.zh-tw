---
description: 若要在儲存 JPEG 影像時指定壓縮等級，請初始化 System.drawing.imaging.encoderparameters> 物件，並將該物件的位址傳遞至 Image 類別的 Save 方法。
ms.assetid: b8365c00-2223-4aff-9fb2-422976af4c31
title: 設定 JPEG 壓縮等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d2e82dfb21e121609d5e09e5c31e2242ec652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690331"
---
# <a name="setting-jpeg-compression-level"></a><span data-ttu-id="29bde-103">設定 JPEG 壓縮等級</span><span class="sxs-lookup"><span data-stu-id="29bde-103">Setting JPEG Compression Level</span></span>

<span data-ttu-id="29bde-104">若要在儲存 JPEG 影像時指定壓縮等級，請初始化 [**system.drawing.imaging.encoderparameters>**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters)物件，並將該物件的位址傳遞至 [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。</span><span class="sxs-lookup"><span data-stu-id="29bde-104">To specify the compression level when you save a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="29bde-105">將 **system.drawing.imaging.encoderparameters>** 物件初始化，使其具有由一個 [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) 物件組成的陣列。</span><span class="sxs-lookup"><span data-stu-id="29bde-105">Initialize the **EncoderParameters** object so that it has an array consisting of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="29bde-106">將一個 **EncoderParameter** 物件初始化，讓其 **值** 成員指向從0到100的 **ULONG** 值。</span><span class="sxs-lookup"><span data-stu-id="29bde-106">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** value from 0 through 100.</span></span> <span data-ttu-id="29bde-107">將 **EncoderParameter** 物件的 **Guid** 成員設定為 EncoderQuality。</span><span class="sxs-lookup"><span data-stu-id="29bde-107">Set the **Guid** member of the **EncoderParameter** object to EncoderQuality.</span></span>

<span data-ttu-id="29bde-108">下列主控台應用程式會儲存三個 JPEG 影像，每個影像各有不同的品質等級。</span><span class="sxs-lookup"><span data-stu-id="29bde-108">The following console application saves three JPEG images, each with a different quality level.</span></span> <span data-ttu-id="29bde-109">品質層級 0 對應到最大壓縮，而品質層級 100 對應到最小壓縮。</span><span class="sxs-lookup"><span data-stu-id="29bde-109">A quality level of 0 corresponds to the greatest compression, and a quality level of 100 corresponds to the least compression.</span></span>

<span data-ttu-id="29bde-110">Main 函式依賴 helper 函式 GetEncoderClsid，它會顯示在抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)中：</span><span class="sxs-lookup"><span data-stu-id="29bde-110">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md):</span></span>


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
   ULONG             quality;
   Status            stat;

   // Get an image from the disk.
   Image* image = new Image(L"Shapes.bmp");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will let this value vary from 0 to 100.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderQuality;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Save the image as a JPEG with quality level 0.
   quality = 0;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes001.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes001.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes001.jpg");

   // Save the image as a JPEG with quality level 50.
   quality = 50;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes050.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes050.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes050.jpg");

      // Save the image as a JPEG with quality level 100.
   quality = 100;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes100.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes100.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes100.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
