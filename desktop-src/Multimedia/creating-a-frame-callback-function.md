---
title: 建立框架回呼函數
description: 建立框架回呼函數
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- capSetCallbackOnFrame 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac102baf62cbfabc79a9a38eb81127a0c6ea36b6ad694139f882bbae0e1bce1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497928"
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

 

 




