---
title: 處理 MM_WOM_DONE 訊息
description: 處理 MM \_ WOM \_ 完成訊息
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- 波形音訊，訊息
- 輔助音訊，訊息
- 波形音訊，MM_WOM_DONE 訊息
- 輔助音訊，MM_WOM_DONE 訊息
- MM_WOM_DONE 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462212"
---
# <a name="processing-the-mm_wom_done-message"></a><span data-ttu-id="7cce8-108">處理 MM \_ WOM \_ 完成訊息</span><span class="sxs-lookup"><span data-stu-id="7cce8-108">Processing the MM\_WOM\_DONE Message</span></span>

<span data-ttu-id="7cce8-109">下列範例顯示如何處理 [**MM \_ WOM \_ 完成**](mm-wom-done.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7cce8-109">The following example shows how to process the [**MM\_WOM\_DONE**](mm-wom-done.md) message.</span></span> <span data-ttu-id="7cce8-110">此範例假設應用程式不會播放多個資料區塊，因此它可以在播放單一資料區塊之後關閉輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="7cce8-110">This example assumes the application does not play multiple data blocks, so it can close the output device after playing a single data block.</span></span>


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




