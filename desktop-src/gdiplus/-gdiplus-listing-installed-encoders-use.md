---
description: GDI+ 提供 GetImageEncoders 函式，讓您可以判斷電腦上可用的影像編碼器。
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: 列出已安裝的編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072b18d226d2ad09bc79cb1d1599ea5c0c62fa695a7aae2ff5969e27031e37b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066879"
---
# <a name="listing-installed-encoders"></a>列出已安裝的編碼器

GDI+ 提供 [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders)函式，讓您可以判斷電腦上可用的影像編碼器。 **GetImageEncoders** 會傳回 [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) 物件的陣列。 在呼叫 **GetImageEncoders** 之前，您必須配置夠大的緩衝區來接收該陣列。 您可以呼叫 [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) 來判斷所需的緩衝區大小。

下列主控台應用程式會列出可用的映射編碼器：


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image encoders
   UINT  size;       // size, in bytes, of the image encoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



當您執行上述的主控台應用程式時，輸出會如下所示：


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
