---
title: 如何處理 ComboBoxEx 通知
description: 本主題將示範如何處理 ComboBoxEx 通知訊息。
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575488"
---
# <a name="how-to-process-comboboxex-notifications"></a>如何處理 ComboBoxEx 通知

本主題將示範如何處理 ComboBoxEx 通知訊息。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


ComboBoxEx 控制項藉由傳送 [**WM \_ 通知**](wm-notify.md) 訊息，來通知其父視窗的事件。 它也會將它從它所包含的下拉式方塊接收的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 通知訊息，傳遞給要處理的父視窗。 因此，您的應用程式必須準備好處理從 ComboBoxEx 子下拉式方塊控制項轉送的 ComboBoxEx 和 **wm \_ 命令** 訊息中的 **wm \_ 通知** 訊息。

本節中的範例會呼叫對應的應用程式定義函數來處理這些訊息，以處理來自 ComboBoxEx 控制項的 [**wm \_ 通知**](wm-notify.md) 和 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。

## <a name="complete-example"></a>完整範例


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 ComboBoxEx 控制項](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx 控制項參考](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[使用 ComboBoxEx 控制項](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 