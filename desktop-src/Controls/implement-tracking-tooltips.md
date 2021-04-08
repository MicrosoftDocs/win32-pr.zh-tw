---
title: 如何執行追蹤工具提示
description: 追蹤工具提示會保持可見，直到應用程式明確關閉為止，並且可以動態地變更螢幕上的位置。 版本4.70 和更新版本的通用控制項都支援它們。
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021018"
---
# <a name="how-to-implement-tracking-tooltips"></a>如何執行追蹤工具提示

追蹤工具提示會保持可見，直到應用程式明確關閉為止，並且可以動態地變更螢幕上的位置。 [版本 4.70](common-control-versions.md)和更新版本的通用控制項都支援它們。

若要建立追蹤工具提示，請在傳送 \_ [**TTM \_ ADDTOOL**](ttm-addtool.md)訊息時，在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中包含 TTF TRACK 旗標。

您的應用程式必須以手動方式啟動 (顯示) ，並藉由傳送 [**TTM \_ TRACKACTI加值稅E**](ttm-trackactivate.md) 訊息來停用 (隱藏) 追蹤工具提示。 當追蹤工具提示為使用中時，您的應用程式必須將 [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) 訊息傳送至工具提示控制項，以指定工具提示的位置。 由於應用程式會處理工作（例如定位工具提示），因此追蹤工具提示不會使用 **TTF 子 \_ 類別** 旗標或 [**TTM \_ RELAYEVENT**](ttm-relayevent.md) 訊息。

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)訊息會讓工具提示控制項使用兩個放置樣式的其中一個來顯示視窗：

-   根據預設，工具提示會顯示在控制項所選擇的位置中，對應工具的旁邊。 選擇的位置是相對於您使用此訊息所提供的座標。
-   如果您在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的成員中包含 **TTF \_ 絕對值**，則會在訊息中指定的圖元位置顯示工具提示。 在此情況下，控制項不會嘗試從您提供的座標變更工具提示視窗的位置。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="implement-in-place-tooltips"></a>執行工具提示 In-Place

範例中所使用之 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **UFlags** 成員包含 **TTF \_ 絕對** 旗標。 如果沒有這個旗標，工具提示控制項會選擇要顯示工具提示的位置，而其相對於對話方塊的位置可能會隨著滑鼠指標移動而突然變更。

> [!Note]  
> `g_toolItem` 是全域 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構。

 

下列範例示範如何建立追蹤工具提示控制項。 此範例會將主視窗的整個工作區指定為工具。


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a>視窗程式執行

當滑鼠指標位於工作區時，工具提示會在作用中，並顯示游標座標，如下圖所示。

![對話方塊的螢幕擷取畫面;工具提示會顯示滑鼠指標的 x 和 y 座標](images/tt-tracking.png)

下列範例程式碼來自對話方塊的視窗程式，此對話方塊會顯示在上述範例中建立的追蹤工具提示。 全域布林值變數 *g \_ TrackingMouse* 是用來判斷是否需要重新啟用工具提示和重設滑鼠追蹤，如此當滑鼠指標離開對話方塊的工作區時，就會通知應用程式。


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 




