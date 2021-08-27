---
title: 取得捕獲視窗的狀態
description: 取得捕獲視窗的狀態
ms.assetid: 5095dbd2-7cd4-48b6-bbb4-1f0bddfcfd06
keywords:
- capGetStatus 宏
- CAPSTATUS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8effedac3950f0f57aaa6e57ccd5a93fe3044982c3d6ec6d6bb69b56024a1255
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038368"
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

 

 