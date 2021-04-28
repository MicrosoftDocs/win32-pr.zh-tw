---
title: 撰寫視窗程式
description: 撰寫視窗程式
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105716"
---
# <a name="writing-the-window-procedure"></a>撰寫視窗程式

[**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)函式會呼叫訊息目標視窗的視窗程式。 視窗程式具有下列簽章。

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

有四個參數：

- *hwnd* 是視窗的控制碼。
- *uMsg* 是訊息代碼;例如， [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息表示視窗已調整大小。
- *wParam* 和 *lParam* 包含與訊息相關的其他資料。 確切的意義取決於訊息碼。

**LRESULT** 是您的程式傳回給 Windows 的整數值。 它包含您的程式對特定訊息的回應。 此值的意義取決於訊息碼。 **回呼** 是函數的呼叫慣例。

一般的視窗程式只是在訊息程式碼上切換的大型 switch 語句。 針對您想要處理的每個訊息新增案例。

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

訊息的額外資料會包含在 *lParam* 和 *wParam* 參數中。 這兩個參數都是整數值，也就是指標寬度的大小 (32 位或64位) 。 各項的意義取決於 (*uMsg*) 的訊息碼。 針對每個訊息，您必須查閱 MSDN 上的訊息程式碼，並將參數轉換成正確的資料類型。 資料通常是數值或結構的指標。 某些訊息沒有任何資料。

例如， [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息的檔指出：

- *wParam* 是一個旗標，指出視窗是否最小化、最大化或調整大小。
- *lParam* 包含視窗的新寬度和高度，做為將16位值壓縮成 1 32 或64位數位。 您必須執行一些位移位以取得這些值。 幸運的是，標頭檔 WinDef 包含可進行此作業的 helper 宏。

一般的視窗程式會處理數十個訊息，因此它可能會變得很長。 讓您的程式碼更模組化的其中一種方式，是將處理每個訊息的邏輯放在個別的函式中。 在視窗程式中，將 *wParam* 和 *lParam* 參數轉換成正確的資料類型，並將這些值傳遞至函式。 例如，若要處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息，視窗程式如下所示：

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))和 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))宏會從 *lParam* 取得16位的寬度和高度值。  (您可以在 MSDN 檔中查看每個訊息代碼的這幾種詳細資料。 ) 視窗程式會將寬度和高度解壓縮，然後將這些值傳遞至函式 `OnSize` 。

## <a name="default-message-handling"></a>預設訊息處理

如果您未處理視窗程式中的特定訊息，請將訊息參數直接傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 此函式會執行訊息的預設動作，這會因訊息類型而異。

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>避免視窗程式中的瓶頸

當您的視窗程式執行時，它會封鎖在相同執行緒上建立之 windows 的任何其他訊息。 因此，請避免在您的視窗程式內進行冗長的處理。 例如，假設您的程式開啟了 TCP 連線，並無限期等待伺服器回應。 如果您在視窗程式中這麼做，則在要求完成之前，您的 UI 將不會回應。 在這段時間內，視窗無法處理滑鼠或鍵盤輸入、重新繪製或甚至關閉。

相反地，您應該使用 Windows 內建的多工工具之一，將工作移至另一個執行緒：

- 建立新的執行緒。
- 使用執行緒集區。
- 使用非同步 i/o 呼叫。
- 使用非同步程序呼叫。

## <a name="next"></a>下一個

[繪製視窗](painting-the-window.md)
