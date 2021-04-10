---
title: 判斷壓縮程式的輸出格式
description: 判斷壓縮程式的輸出格式
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，輸出格式
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，輸出格式
- ICCompressGetFormat 宏
- ICCompressQuery 宏
- ICCompressGetSize 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092727"
---
# <a name="determining-a-compressors-output-format"></a>判斷壓縮程式的輸出格式

下列範例會使用 [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size 宏來判斷指定壓縮格式之資料所需的緩衝區大小、使用 [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) 函數配置適當大小的緩衝區，並使用 **ICCompressGetFormat** 宏來抓取壓縮格式資訊。


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



下列範例會使用 [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) 宏來判斷壓縮壓縮是否可以處理輸入和輸出格式。


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



下列範例會使用 [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) 宏來決定緩衝區大小，並使用 [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc)配置該大小的緩衝區。


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 