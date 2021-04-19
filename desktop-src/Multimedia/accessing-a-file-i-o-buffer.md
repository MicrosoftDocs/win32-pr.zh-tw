---
title: 存取檔案 i/o 緩衝區
description: 存取檔案 i/o 緩衝區
ms.assetid: b829d8ef-8e0b-4c30-b8cf-e9feccc63bbf
keywords:
- 多媒體檔案 i/o，存取緩衝區
- 檔案 i/o，存取緩衝區
- 輸入和輸出 (i/o) ，存取緩衝區
- I/o (輸入和輸出) ，存取緩衝區
- 存取 i/o 緩衝區
- 緩衝的 i/o
- mmioSetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c89b2376f1bae68d55c76d7731b6ee78f6bf7d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106988024"
---
# <a name="accessing-a-file-io-buffer"></a><span data-ttu-id="594b6-110">存取檔案 i/o 緩衝區</span><span class="sxs-lookup"><span data-stu-id="594b6-110">Accessing a File I/O Buffer</span></span>

<span data-ttu-id="594b6-111">下列範例會直接存取 i/o 緩衝區以讀取波形音訊檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="594b6-111">The following example accesses an I/O buffer directly to read data from a waveform-audio file.</span></span>


```C++
HMMIO    hmmio; 
MMIOINFO mmioinfo; 
DWORD    dwDataSize; 
DWORD    dwCount; 
HPSTR    hptr; 

// Get information about the file I/O buffer. 
if (mmioGetInfo(hmmio, &mmioinfo, 0)) 
{ 
    Error("Failed to get I/O buffer info."); 
    . 
    . 
    . 
    mmioClose(hmmio, 0); 
    return; 
} 
 
// Read the entire file by directly reading the file I/O buffer. 
// When the end of the I/O buffer is reached, advance the buffer. 

for (dwCount = dwDataSize, hptr = lpData; dwCount  0; dwCount--) 
{ 
    // Check to see if the I/O buffer must be advanced. 
    if (mmioinfo.pchNext == mmioinfo.pchEndRead) 
    { 
        if(mmioAdvance(hmmio, &mmioinfo, MMIO_READ)) 
        { 
            Error("Failed to advance buffer."); 
            . 
            . 
            . 
            mmioClose(hmmio, 0); 
            return; 
        } 
    } 
 
    // Get a character from the buffer. 
    *hptr++ = *mmioinfo.pchNext++; 
} 
 
// End direct buffer access and close the file. 
mmioSetInfo(hmmio, &mmioinfo, 0); 
mmioClose(hmmio, 0); 

```



<span data-ttu-id="594b6-112">當您完成存取檔案 i/o 緩衝區時，請呼叫 [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)函式，並傳遞 [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)函式所填滿的 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構位址。</span><span class="sxs-lookup"><span data-stu-id="594b6-112">When you finish accessing a file I/O buffer, call the [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) function, passing an address of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure filled by the [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) function.</span></span> <span data-ttu-id="594b6-113">如果您已寫入緩衝區，請 \_ 在 **MMIOINFO** 結構的 **DWFLAGS** 成員中設定 MMIO DIRTY 旗標，然後再呼叫 **mmioSetInfo**。</span><span class="sxs-lookup"><span data-stu-id="594b6-113">If you wrote to the buffer, set the MMIO\_DIRTY flag in the **dwFlags** member of the **MMIOINFO** structure before calling **mmioSetInfo**.</span></span> <span data-ttu-id="594b6-114">否則，將不會將緩衝區排清到磁片。</span><span class="sxs-lookup"><span data-stu-id="594b6-114">Otherwise, the buffer will not be flushed to disk.</span></span>

 

 