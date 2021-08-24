---
title: 建立捕獲視窗
description: 建立捕獲視窗
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- capCreateCaptureWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d44e7701900d090a8d73b226039d468e2da817e9c0f9746fc10eaa13578d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144771"
---
# <a name="creating-a-capture-window"></a>建立捕獲視窗

下列範例會使用 [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) 函式來建立捕獲視窗。


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




