---
title: 如何顯示按鈕的工具提示
description: 當您指定 TBSTYLE \_ 工具提示樣式時，工具列會建立和管理工具提示控制項。 工具提示控制項是隱藏的，只有在使用者將指標移到工具列按鈕上方，並將其保留大約一秒時才會出現。
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319998"
---
# <a name="how-to-display-tooltips-for-buttons"></a>如何顯示按鈕的工具提示

當您指定 [**TBSTYLE \_ 工具提示**](toolbar-control-and-button-styles.md) 樣式時，工具列會建立和管理工具提示控制項。 工具提示控制項是隱藏的，只有在使用者將指標移到工具列按鈕上方，並將其保留大約一秒時才會出現。

您的應用程式可以下列任何一種方式，將文字提供給工具提示控制項：

-   將工具提示文字設定為每個按鈕之 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的 **iString** 成員。 您也必須傳送 [**TB 的 \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) 訊息，並將文字資料列的最大值設為0，讓文字不會顯示為按鈕標籤，而不會顯示為工具提示。
-   使用 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式建立工具列，然後設定 [**TBSTYLE \_ EX \_ MIXEDBUTTONS**](toolbar-extended-styles.md) 延伸樣式。 標籤只會針對具有 [**BTNS \_ SHOWTEXT**](toolbar-control-and-button-styles.md) 樣式的按鈕顯示。 針對沒有此樣式的按鈕，會顯示包含按鈕文字的工具提示。
-   回應 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知碼。
-   回應 [TBN \_ GETINFOTIP](tbn-getinfotip.md) 通知碼。

需要直接將訊息傳送至工具提示控制項的應用程式，可以使用 [**TB \_ GETTOOLTIPS**](tb-gettooltips.md) 訊息來取得控制項的控制碼。 應用程式可以使用 [**TB \_ SETTOOLTIPS**](tb-settooltips.md) 訊息來取代工具列的工具提示控制項與另一個工具提示控制項。

提供工具提示文字最有彈性的方式，就是以 [**WM \_ 通知**](wm-notify.md)訊息的形式，回應工具列控制項傳送給其父系的 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)或 [TBN \_ GETINFOTIP](tbn-getinfotip.md)通知程式碼。 針對 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)， *lParam* 參數包含 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構的指標 (也定義為 **LPTOOLTIPTEXT**) ，以指定需要解說文字之按鈕的命令識別碼。 此識別碼位於 **NMTTDISPINFO idFrom** 成員中。 應用程式可以將解說文字複製到結構中、指定包含解說文字之字串的位址，或指定字串資源的實例控制碼和資源識別碼。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="display-a-tooltip-for-a-button"></a>顯示按鈕的工具提示

下列範例程式碼會藉由提供資源識別碼的文字來處理 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 工具提示通知程式碼。


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具列控制項](using-toolbar-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




