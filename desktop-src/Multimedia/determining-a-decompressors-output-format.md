---
title: 判斷解壓縮程式的輸出格式
description: 判斷解壓縮程式的輸出格式
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，輸出格式
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，輸出格式
- ICDecompressGetFormatSize 宏
- ICDecompressQuery 宏
- ICDecompressGetPalette 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092698"
---
# <a name="determining-a-decompressors-output-format"></a><span data-ttu-id="142ae-108">判斷解壓縮程式的輸出格式</span><span class="sxs-lookup"><span data-stu-id="142ae-108">Determining a Decompressor's Output Format</span></span>

<span data-ttu-id="142ae-109">下列範例會使用 [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) 宏來決定資料指定解壓縮格式所需的緩衝區大小、使用 [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) 函數配置適當大小的緩衝區，並使用 [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) 宏來抓取解壓縮格式資訊。</span><span class="sxs-lookup"><span data-stu-id="142ae-109">The following example determines the buffer size needed for the data specifying the decompression format using the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the decompression format information using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="142ae-110">下列範例會顯示應用程式如何使用 [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) 宏來判斷解壓縮程式是否可以處理輸入和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="142ae-110">The following example shows how an application can use the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a decompressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



<span data-ttu-id="142ae-111">下列程式碼片段顯示如何使用 [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) 宏取得調色板資訊。</span><span class="sxs-lookup"><span data-stu-id="142ae-111">The following code fragment shows how to get the palette information using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 