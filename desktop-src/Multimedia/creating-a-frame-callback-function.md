---
title: 建立框架回呼函數
description: 建立框架回呼函數
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- capSetCallbackOnFrame 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b2a921bfae235c50387c41865c44bb69b5c05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300523"
---
# <a name="creating-a-frame-callback-function"></a>建立框架回呼函數

下列範例是簡單的畫面回呼函數。 使用 [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) 宏註冊此回呼。


```
TCHAR gachBuffer[100];  // Global buffer.
DWORD gdwFrameNum = 0;

// FrameCallbackProc: frame callback function. 
// hWnd:              capture window handle. 
// lpVHdr:            pointer to structure containing captured 
//                        frame information. 
// 
LRESULT PASCAL FrameCallbackProc(HWND hWnd, LPVIDEOHDR lpVHdr) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    _stprintf_s(gachBuffer, TEXT("Preview frame# %ld "), gdwFrameNum++); 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE ; 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




