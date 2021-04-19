---
title: 如何取出和設定快速鍵
description: 本主題將示範如何取得或設定快速鍵控制項的按鍵組合。
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106993738"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>如何取出和設定快速鍵

本主題將示範如何取得或設定快速鍵控制項的按鍵組合。 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)訊息可讓應用程式設定快速鍵控制項的快速鍵組合。 應用程式會使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息來取得使用者所選擇之快速鍵的虛擬金鑰程式碼和修飾詞旗標。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


您可以使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息來取得虛擬金鑰程式碼和輔助按鍵，以描述使用者選擇的熱鍵。 使用 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) 訊息來設定快速鍵的值。

在下列 c + + 程式碼範例中，應用程式定義函式會使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息從熱鍵控制項取出按鍵組合，然後使用 [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) 訊息來設定全域熱鍵。 請注意，您無法為具有 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 視窗樣式的視窗設定全域快速鍵。



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
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

 

 