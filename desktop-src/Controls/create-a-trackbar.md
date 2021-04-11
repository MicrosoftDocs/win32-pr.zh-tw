---
title: 如何建立跟蹤條
description: 建立程式時，會初始化其範圍及其選取範圍。 此時也會設定頁面大小。
ms.assetid: FA110B4A-D3D7-49D8-A3DC-368099F6DA1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9468ff044b94837f54d04cda4a9105f15410692
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021024"
---
# <a name="how-to-create-a-trackbar"></a>如何建立跟蹤條

建立程式時，會初始化其範圍及其選取範圍。 此時也會設定頁面大小。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-trackbar"></a>建立跟蹤條

下列範例示範如何建立具有 [**tb \_ AUTOTICKS**](trackbar-control-styles.md) 和 [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式的顯示。


```
// CreateTrackbar - creates and initializes a trackbar. 
// 
// Global variable
//     g_hinst - instance handle
//
HWND WINAPI CreateTrackbar( 
    HWND hwndDlg,  // handle of dialog box (parent window) 
    UINT iMin,     // minimum value in trackbar range 
    UINT iMax,     // maximum value in trackbar range 
    UINT iSelMin,  // minimum value in trackbar selection 
    UINT iSelMax)  // maximum value in trackbar selection 
{ 

    InitCommonControls(); // loads common control's DLL 

    hwndTrack = CreateWindowEx( 
        0,                               // no extended styles 
        TRACKBAR_CLASS,                  // class name 
        "Trackbar Control",              // title (caption) 
        WS_CHILD | 
        WS_VISIBLE | 
        TBS_AUTOTICKS | 
        TBS_ENABLESELRANGE,              // style 
        10, 10,                          // position 
        200, 30,                         // size 
        hwndDlg,                         // parent window 
        ID_TRACKBAR,                     // control identifier 
        g_hinst,                         // instance 
        NULL                             // no WM_CREATE parameter 
        ); 

    SendMessage(hwndTrack, TBM_SETRANGE, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) MAKELONG(iMin, iMax));  // min. & max. positions
        
    SendMessage(hwndTrack, TBM_SETPAGESIZE, 
        0, (LPARAM) 4);                  // new page size 

    SendMessage(hwndTrack, TBM_SETSEL, 
        (WPARAM) FALSE,                  // redraw flag 
        (LPARAM) MAKELONG(iSelMin, iSelMax)); 
        
    SendMessage(hwndTrack, TBM_SETPOS, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) iSelMin); 

    SetFocus(hwndTrack); 

    return hwndTrack; 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 [使用] 控制項](using-trackbar-controls.md)
</dt> </dl>

 

 




