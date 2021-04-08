---
title: 解壓縮資料
description: 解壓縮資料
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，解壓縮資料
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，解壓縮資料
- ICDecompressBegin 宏
- ICDecompress 函式
- ICDecompressEnd 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b44ea375bb1f2b5c41a361ca7f31387439b610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673403"
---
# <a name="decompressing-data"></a><span data-ttu-id="902e2-108">解壓縮資料</span><span class="sxs-lookup"><span data-stu-id="902e2-108">Decompressing Data</span></span>

<span data-ttu-id="902e2-109">下列範例顯示應用程式如何使用 [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) 宏初始化解壓縮程式、使用 [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) 函式解壓縮框架順序，以及使用 [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) 宏來終止解壓縮。</span><span class="sxs-lookup"><span data-stu-id="902e2-109">The following example shows how an application can initialize a decompressor using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro, decompress a frame sequence using the [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) function, and terminate decompression using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




