---
title: 壓縮資料
description: 壓縮資料
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，壓縮資料
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，壓縮資料
- ICCompressBegin 宏
- ICCompress 函式
- ICCompressEnd 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f45c7b592b4b55e77b71390d7ffd79b23714242ea678d641d4a3f5b8118bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145001"
---
# <a name="compressing-data"></a>壓縮資料

下列範例會壓縮要用於 AVI 檔案的影像資料。 它會假設壓縮功能不支援 VIDCF \_ CRUNCH 或 VIDCF \_ 時態旗標，但它支援 VIDCF \_ 品質。 此範例會使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏、 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函數和 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏。


```C++
DWORD dwCkID; 
DWORD dwCompFlags; 
DWORD dwQuality; 
LONG  lNumFrames, lFrameNum; 
// Assume dwNumFrames is initialized to the total number of frames. 
// Assume dwQuality holds the proper quality value (0-10000). 
// Assume lpbiOut, lpOut, lpbiIn, and lpIn are initialized properly. 
 
// If OK to start, compress each frame. 
if (ICCompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for ( lFrameNum = 0; lFrameNum < lNumFrames; lFrameNum++)
    { 
        if (ICCompress(hIC, 0, lpbiOut, lpOut, lpbiIn, lpIn, 
            &dwCkID, &dwCompFlags, lFrameNum, 
            0, dwQuality, NULL, NULL) == ICERR_OK)
        { 
            // Write compressed data to the AVI file. 
             
            // Set lpIn to the next frame in the sequence. 
             
        } 
        else 
        { 
            // Handle compressor error. 
        } 
    } 
    ICCompressEnd(hIC);    // terminate compression 
} 
else 
{ 
    // Handle the error identifying the unsupported format. 
} 
 
```



 

 




