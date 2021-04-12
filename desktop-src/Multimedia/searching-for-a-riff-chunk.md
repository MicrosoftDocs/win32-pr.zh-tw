---
title: 搜尋 RIFF 區塊
description: 搜尋 RIFF 區塊
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- 多媒體檔案 i/o，搜尋 RIFF 區塊
- 檔案 i/o，搜尋 RIFF 區塊
- 輸入和輸出 (i/o) ，搜尋 RIFF 區塊
- I/o (輸入和輸出) ，搜尋 RIFF 區塊
- 搜尋 RIFF 區塊
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375324"
---
# <a name="searching-for-a-riff-chunk"></a><span data-ttu-id="9a63c-112">搜尋 RIFF 區塊</span><span class="sxs-lookup"><span data-stu-id="9a63c-112">Searching for a RIFF Chunk</span></span>

<span data-ttu-id="9a63c-113">下列範例會使用 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) 函式來搜尋格式為 "WAVE" 的 "RIFF" 區塊，以確認剛開啟的檔案是波形音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="9a63c-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for a "RIFF" chunk with a form type of "WAVE" to verify that the file that has just been opened is a waveform-audio file.</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 