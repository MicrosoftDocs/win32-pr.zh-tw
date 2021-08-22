---
title: 變更 i/o 緩衝區大小
description: 變更 i/o 緩衝區大小
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- 多媒體檔案 i/o，變更緩衝區大小
- 檔案 i/o，變更緩衝區大小
- 輸入和輸出 (i/o) ，變更緩衝區大小
- I/o (輸入和輸出) ，變更緩衝區大小
- 變更 i/o 緩衝區大小
- 未緩衝 i/o
- 緩衝的 i/o
- mmioSetBuffer 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 826fabfb7e51b80bf406721b3d5e7b094f83c1c3fe2061f7edea0810a41dc639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145081"
---
# <a name="changing-the-io-buffer-size"></a>變更 i/o 緩衝區大小

下列範例會針對未緩衝的 i/o 開啟名為 SAMPLE.TXT 的檔案，然後使用 [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) 函式以內部16k 緩衝區啟用緩衝處理的 i/o。


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 