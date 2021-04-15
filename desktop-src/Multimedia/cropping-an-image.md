---
title: 裁剪影像
description: 裁剪影像
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- MCIWndGetSource 宏
- MCIWndPutSource 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462181"
---
# <a name="cropping-an-image"></a>裁剪影像

下列範例會建立 MCIWnd 視窗並載入 AVI 檔。 此視窗會在功能表中包含裁剪命令，該命令會從框架的四個邊裁剪一季的高度或寬度。 此範例會使用 [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) 宏來抓取來源矩形的目前 (初始) 維度。 修改後的來源矩形會是原始高度和寬度的一半，並在原始框架中置中。 [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)宏的呼叫會重新定義來源矩形的座標。


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




