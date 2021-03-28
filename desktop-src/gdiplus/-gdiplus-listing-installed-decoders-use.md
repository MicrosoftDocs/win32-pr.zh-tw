---
description: Windows GDI + 提供 GetImageDecoders 函式，讓您可以判斷電腦上可用的映射解碼器。
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: 列出已安裝的解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a20a4e8ac88fa884483ebeaf6592b8085fde807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972869"
---
# <a name="listing-installed-decoders"></a>列出已安裝的解碼器

Windows GDI + 提供 [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) 函式，讓您可以判斷電腦上可用的映射解碼器。 **GetImageDecoders** 會傳回 [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) 物件的陣列。 在呼叫 **GetImageDecoders** 之前，您必須配置夠大的緩衝區來接收該陣列。 您可以呼叫 [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) 來判斷所需的緩衝區大小。

下列主控台應用程式會列出可用的映射解碼器：


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

   UINT  num;        // number of image decoders
   UINT  size;       // size, in bytes, of the image decoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many decoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageDecodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageDecoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageDecoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageDecoders(num, size, pImageCodecInfo);

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
image/x-emf
image/x-wmf
image/tiff
image/png
image/x-icon
```



 

 
