---
title: 使用 mmioOpen 開啟檔案
description: 使用 mmioOpen 開啟檔案
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- 多媒體檔案 i/o，開啟檔案
- 檔案 i/o，開啟檔案
- 輸入和輸出 (i/o) ，開啟檔案
- I/o (輸入和輸出) ，開啟檔案
- 多媒體檔案 i/o，mmioOpen 函式
- file i/o，mmioOpen 函式
- 輸入和輸出 (i/o) ，mmioOpen 函式
- I/o (輸入和輸出) ，mmioOpen 函式
- mmioOpen 函式
- 開啟 i/o 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463121"
---
# <a name="opening-a-file-with-mmioopen"></a><span data-ttu-id="2f25c-113">使用 mmioOpen 開啟檔案</span><span class="sxs-lookup"><span data-stu-id="2f25c-113">Opening a File with mmioOpen</span></span>

<span data-ttu-id="2f25c-114">若要開啟基本 i/o 作業的檔案，請將 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的 *lpmmioinfo* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f25c-114">To open a file for basic I/O operations, set the *lpmmioinfo* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to **NULL**.</span></span> <span data-ttu-id="2f25c-115">下列範例會開啟名為 "C： \\ SAMPLES \\SAMPLE1.TXT" 的檔案進行讀取，並檢查錯誤的傳回值。</span><span class="sxs-lookup"><span data-stu-id="2f25c-115">The following example opens a file named "C:\\SAMPLES\\SAMPLE1.TXT" for reading, and checks the return value for error.</span></span>


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



<span data-ttu-id="2f25c-116">使用 **mmioOpen** 的 *dwFlags* 參數來指定用來開啟檔案的旗標。</span><span class="sxs-lookup"><span data-stu-id="2f25c-116">Use the *dwFlags* parameter of **mmioOpen** to specify flags for opening a file.</span></span>

 

 