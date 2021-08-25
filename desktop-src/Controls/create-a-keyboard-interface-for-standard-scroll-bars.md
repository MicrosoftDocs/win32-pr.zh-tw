---
title: 如何建立標準捲軸的鍵盤介面
description: 雖然捲軸控制項提供內建的鍵盤介面，但標準捲軸不是。
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698738"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>如何建立標準捲軸的鍵盤介面

雖然捲軸控制項提供內建的鍵盤介面，但標準捲軸不是。 若要執行標準捲軸的鍵盤介面，視窗程式必須處理 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息，並檢查 *wParam* 參數所指定的虛擬機器碼程式碼。 如果虛擬按鍵程式碼對應到箭號鍵，則視窗程式會將一組 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息傳送給自己，並將 *wParam* 參數的低序位字組設定為適當的捲軸要求碼。

例如，當使用者按下向上鍵時，視窗程式會收到 *wParam* 等於 VK UP 的 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)訊息 \_ 。 在回應中，視窗程式會將具有低序位單字 *wParam* 的一 [**\_ VSCROLL**](wm-vscroll.md)訊息傳送給自己，並將設定為 SB 的 \_ 要求碼。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>建立標準捲軸的鍵盤介面

下列程式碼範例示範如何包含標準捲軸的鍵盤介面。


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用捲軸](using-scroll-bars.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 