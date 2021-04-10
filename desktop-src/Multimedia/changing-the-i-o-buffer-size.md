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
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023483"
---
# <a name="changing-the-io-buffer-size"></a><span data-ttu-id="0eca6-111">變更 i/o 緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="0eca6-111">Changing the I/O Buffer Size</span></span>

<span data-ttu-id="0eca6-112">下列範例會針對未緩衝的 i/o 開啟名為 SAMPLE.TXT 的檔案，然後使用 [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) 函式以內部16k 緩衝區啟用緩衝處理的 i/o。</span><span class="sxs-lookup"><span data-stu-id="0eca6-112">The following example opens a file named SAMPLE.TXT for unbuffered I/O, and then enables buffered I/O with an internal 16K buffer using the [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) function.</span></span>


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



 

 