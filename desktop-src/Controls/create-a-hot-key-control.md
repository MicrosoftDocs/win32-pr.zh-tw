---
title: 如何建立快速鍵控制項
description: 本主題將示範如何建立快速鍵控制項。 您可以使用 CreateWindowEx 函式來建立快速鍵控制項，以指定快速鍵 \_ 類別視窗類別。
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842912"
---
# <a name="how-to-create-a-hot-key-control"></a>如何建立快速鍵控制項

本主題將示範如何建立快速鍵控制項。 您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立快速鍵控制項，以指定快速鍵 \_ 類別視窗類別。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


建立快速鍵控制項之前，請確定已載入通用控制項 DLL。

在下列 c + + 程式碼範例中，應用程式定義函式會呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來載入通用控制項 DLL。 然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定快速鍵 **\_ 類別** 視窗類別來建立快速鍵控制項。 它會使用 [**HKM \_ SETRULES**](hkm-setrules.md) 和 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) 訊息來初始化控制項，並將控制碼傳回給控制項。

此熱鍵控制項不允許使用者選擇以單一未修改的金鑰為依據的熱鍵，也不允許使用者只選擇 SHIFT 和 key。 這些規則可有效地防止使用者選擇在輸入文字時可能會不小心輸入的快速鍵。



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速鍵控制參考](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[關於快速鍵控制項](hot-key-controls.md)
</dt> <dt>

[使用快速鍵控制項](using-hot-key-controls.md)
</dt> </dl>

 

 