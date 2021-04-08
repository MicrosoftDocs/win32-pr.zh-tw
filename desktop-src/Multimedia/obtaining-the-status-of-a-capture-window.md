---
title: 取得捕獲視窗的狀態
description: 取得捕獲視窗的狀態
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus 宏
- CAPSTATUS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f848898247ad8ea2ddbb0dde7a13c08b6a7274
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933150"
---
# <a name="obtaining-the-status-of-a-capture-window"></a>取得捕獲視窗的狀態

下列範例會使用 [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos)函式，根據 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構中 [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus)宏所傳回的資訊，將捕捉視窗的大小設定為內送影片串流的整體維度。


```C++
CAPSTATUS CapStatus;

capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS)); 

SetWindowPos(hWndC, NULL, 0, 0, CapStatus.uiImageWidth, 
    CapStatus.uiImageHeight, SWP_NOZORDER | SWP_NOMOVE); 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 