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
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037858"
---
# <a name="processing-the-mm_wom_done-message"></a>處理 MM \_ WOM \_ 完成訊息

下列範例顯示如何處理 [**MM \_ WOM \_ 完成**](mm-wom-done.md) 訊息。 此範例假設應用程式不會播放多個資料區塊，因此它可以在播放單一資料區塊之後關閉輸出裝置。


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



 

 




