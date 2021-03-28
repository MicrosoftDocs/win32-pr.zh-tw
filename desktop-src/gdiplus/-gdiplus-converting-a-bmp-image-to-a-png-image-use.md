---
description: 若要將影像儲存至磁片檔案，請呼叫 Image 類別的 Save 方法。
ms.assetid: a95fa3ea-2013-45d5-bdec-61eddcefc2fa
title: 將 BMP 影像轉換為 PNG 影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d165809bb4cfa7f37685b8b130e2b895b35c0ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991370"
---
# <a name="converting-a-bmp-image-to-a-png-image"></a><span data-ttu-id="64b7e-103">將 BMP 影像轉換為 PNG 影像</span><span class="sxs-lookup"><span data-stu-id="64b7e-103">Converting a BMP Image to a PNG Image</span></span>

<span data-ttu-id="64b7e-104">若要將影像儲存至磁片檔案，請呼叫 [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters))方法。</span><span class="sxs-lookup"><span data-stu-id="64b7e-104">To save an image to a disk file, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="64b7e-105">下列主控台應用程式會從磁片檔案載入 BMP 影像、將影像轉換為 PNG 格式，然後將轉換後的影像儲存至新的磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="64b7e-105">The following console application loads a BMP image from a disk file, converts the image to the PNG format, and saves the converted image to a new disk file.</span></span> <span data-ttu-id="64b7e-106">Main 函式依賴 helper 函式 GetEncoderClsid，其顯示于抓取 [編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)。</span><span class="sxs-lookup"><span data-stu-id="64b7e-106">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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

   CLSID   encoderClsid;
   Status  stat;
   Image*   image = new Image(L"Bird.bmp");

   // Get the CLSID of the PNG encoder.
   GetEncoderClsid(L"image/png", &encoderClsid);

   stat = image->Save(L"Bird.png", &encoderClsid, NULL);

   if(stat == Ok)
      printf("Bird.png was saved successfully\n");
   else
      printf("Failure: stat = %d\n", stat); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 



