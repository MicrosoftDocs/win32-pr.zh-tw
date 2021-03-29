---
description: GDI + 提供 GetImageEncoders 函式，讓您可以判斷電腦上可用的影像編碼器。
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: 列出已安裝的編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310e9d366cdacde019373724f2b9feb3b94aef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972868"
---
# <a name="listing-installed-encoders"></a><span data-ttu-id="56a0f-103">列出已安裝的編碼器</span><span class="sxs-lookup"><span data-stu-id="56a0f-103">Listing Installed Encoders</span></span>

<span data-ttu-id="56a0f-104">GDI + 提供 [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) 函式，讓您可以判斷電腦上可用的影像編碼器。</span><span class="sxs-lookup"><span data-stu-id="56a0f-104">GDI+ provides the [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) function so that you can determine which image encoders are available on your computer.</span></span> <span data-ttu-id="56a0f-105">**GetImageEncoders** 會傳回 [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="56a0f-105">**GetImageEncoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="56a0f-106">在呼叫 **GetImageEncoders** 之前，您必須配置夠大的緩衝區來接收該陣列。</span><span class="sxs-lookup"><span data-stu-id="56a0f-106">Before you call **GetImageEncoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="56a0f-107">您可以呼叫 [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) 來判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="56a0f-107">You can call [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="56a0f-108">下列主控台應用程式會列出可用的映射編碼器：</span><span class="sxs-lookup"><span data-stu-id="56a0f-108">The following console application lists the available image encoders:</span></span>


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



<span data-ttu-id="56a0f-109">當您執行上述的主控台應用程式時，輸出會如下所示：</span><span class="sxs-lookup"><span data-stu-id="56a0f-109">When you run the preceding console application, the output will be similar to the following:</span></span>


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
