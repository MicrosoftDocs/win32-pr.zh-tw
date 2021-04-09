---
title: 關閉視窗
description: 當使用者關閉視窗時，該動作就會觸發一連串的視窗訊息。
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842304"
---
# <a name="closing-the-window"></a>關閉視窗

當使用者關閉視窗時，該動作就會觸發一連串的視窗訊息。

使用者可以按一下 [ **關閉** ] 按鈕，或使用鍵盤快速鍵（例如 ALT + F4）關閉應用程式視窗。 其中任何一項動作都會導致視窗收到 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close) 訊息。 **WM \_ 關閉** 訊息讓您有機會在關閉視窗之前提示使用者。 如果您真的想要關閉視窗，請呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函數。 否則，只會從 **WM \_ 關閉** 訊息傳回零，而且作業系統會忽略該訊息，而不會損毀視窗。

以下是程式可能處理 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)的範例。

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

在此範例中， [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) 函式會顯示模式對話方塊，其中包含 **[確定** ] 和 [ **取消** ] 按鈕。 如果使用者按一下 **[確定]**，程式就會呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow)。 否則，如果使用者按一下 [ **取消**]，則會略過對 **DestroyWindow** 的呼叫，且視窗會保持開啟狀態。 在任一種情況下，都會傳回零以表示您已處理訊息。

如果您想要關閉視窗而不提示使用者，您可以直接呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) ，而不需要呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)。 不過，在此情況下有一個快捷方式。 回想一下， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會執行任何視窗訊息的預設動作。 在 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)的情況下， **DefWindowProc** 會自動呼叫 **DestroyWindow**。 這表示，如果您在 **switch** 語句中忽略 **WM \_ 關閉** 訊息，則預設會終結視窗。

當視窗即將終結時，它會收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息。 這則訊息會在視窗從螢幕中移除之後傳送，但在銷毀之前 (特別是在) 之前終結任何子視窗之前。

在主應用程式視窗中，您通常會藉由呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)來回應 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)。

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

在 [ [視窗訊息]](window-messages.md) 區段中， [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) 會在訊息佇列上放置一個 [**WM \_**](/windows/desktop/winmsg/wm-quit) 結束訊息，造成訊息迴圈結束。

以下流程圖顯示處理 [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close) 和 [**WM \_ 摧毀**](/windows/desktop/winmsg/wm-destroy) 訊息的一般方式：

![顯示如何處理 wm \- 關閉和 wm 損 \- 毀訊息的流程圖](images/wmclose01.png)

## <a name="next"></a>下一個

[管理應用程式狀態](managing-application-state-.md)