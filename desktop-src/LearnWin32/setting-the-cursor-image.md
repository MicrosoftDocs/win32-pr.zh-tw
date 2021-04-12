---
title: 設定游標影像
description: 設定游標影像
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463033"
---
# <a name="setting-the-cursor-image"></a>設定游標影像

*游標* 是顯示滑鼠或其他指標裝置位置的小型影像。 許多應用程式會變更游標影像，以將意見反應提供給使用者。 雖然並非必要，但它會在您的應用程式中增加很棒的波蘭文。

Windows 提供一組標準的資料指標映射，稱為 *系統資料指標*。 其中包括箭號、手形、I-橫樑、沙漏 (現在是旋轉圓形) 和其他。 本節說明如何使用系統資料指標。 如需更先進的工作，例如建立自訂資料指標，請參閱資料 [指標](/windows/desktop/menurc/cursors)。

您可以藉由設定 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)或 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hCursor** 成員，將資料指標與視窗類別產生關聯。 否則，預設資料指標就是箭號。 當滑鼠移至視窗上方時，除非有另一個視窗已捕捉到滑鼠) ，否則視窗會收到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息 (。 此時會發生下列其中一個事件：

-   應用程式會設定資料指標，而視窗程式會傳回 **TRUE**。
-   應用程式不會執行任何動作，並且會將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

若要設定資料指標，程式會執行下列動作：

1.  呼叫 [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) 將資料指標載入記憶體中。 此函數會傳回資料指標的控制碼。
2.  呼叫 [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) 並傳入資料指標控制碼。

否則，若應用程式將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，則 **DefWindowProc** 函式會使用下列演算法來設定資料指標映射：

1.  如果視窗有父代，請將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息轉寄給父系以進行處理。
2.  否則，如果視窗具有類別游標，請將資料指標設定為類別資料指標。
3.  如果沒有類別資料指標，請將資料指標設為箭號游標。

[**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora)函數可以從資源或其中一個系統資料指標載入自訂資料指標。 下列範例會示範如何將資料指標設定為系統手游標。


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



如果您變更游標，則在下一個滑鼠移動時，游標影像會重設，除非您攔截到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息，並再次設定資料指標。 下列程式碼顯示如何處理 **WM \_ SETCURSOR**。


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



此程式碼會先檢查 *lParam* 的較低16位。 如果 `LOWORD(lParam)` 等於 **HTCLIENT**，表示游標是在視窗的工作區上。 否則，游標會在非工作區上。 一般而言，您應該只設定工作區的資料指標，並讓 Windows 設定非工作區的游標。

## <a name="next"></a>下一個

[使用者輸入：擴充的範例](user-input--extended-example.md)

 

 