---
title: 如何處理資訊提示通知訊息
description: Trackbars 會傳送一個 WM \_ HSCROLL 或 wm VSCROLL 訊息給父系，以通知其使用者動作的父視窗 \_ 。
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540318"
---
# <a name="how-to-process-trackbar-notification-messages"></a>如何處理資訊提示通知訊息

Trackbars 會傳送一個 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息給父系，以通知其使用者動作的父視窗。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="process-trackbar-notification-messages"></a>處理資訊提示通知訊息

下列程式碼範例是一種函式，會在執行程式碼段的父視窗收到 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息時呼叫。 此範例中的「 [**\_ ENABLESELRANGE**](trackbar-control-styles.md) 」樣式為「tb」。 滑杆的位置會與選取範圍進行比較，並在必要時，將滑杆移至選取範圍的開始或結束位置。


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>備註

包含 [**tb \_ 垂直**](trackbar-control-styles.md) 樣式的 [顯示] 的對話方塊，可以在接收到 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息時使用這個函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 [使用] 控制項](using-trackbar-controls.md)
</dt> </dl>

 

 




