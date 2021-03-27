---
Description: '\_當系統或其他應用程式提出要求來繪製應用程式視窗的一部分時，就會傳送 WM 油漆訊息。'
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: 'WM_PAINT 訊息 (Winuser .h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974849"
---
# <a name="wm_paint-message"></a>WM \_ 油漆訊息

當系統或其他應用程式提出要求來繪製應用程式視窗的一部分時，就會傳送 **WM \_ 油漆** 訊息。 當呼叫 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)或 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)函式時，或是當應用程式使用 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函數取得 **WM \_ 油漆** 訊息 [**時，就**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)會傳送此訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回零。

## <a name="example"></a>範例

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) 取得的範例。

## <a name="remarks"></a>備註

**WM \_ 油漆** 訊息是由系統產生，不應由應用程式傳送。 若要強制視窗繪製到特定的裝置內容，請使用 [**wm \_ 列印**](wm-print.md) 或 [**wm \_ PRINTCLIENT**](wm-printclient.md) 訊息。 請注意，這需要目標視窗支援 **WM \_ PRINTCLIENT** 訊息。 最常見的控制項支援 **WM \_ PRINTCLIENT** 訊息。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會驗證更新區域。 如果必須繪製視窗框架，此函式也可以將 [**wm \_ NCPAINT**](wm-ncpaint.md) 訊息傳送至視窗程式，如果必須清除視窗背景，則傳送 [**wm \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息。

當應用程式的訊息佇列中沒有其他訊息時，系統會傳送此訊息。 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) 決定傳送訊息的位置; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 會決定要分派的訊息。 當應用程式訊息佇列中沒有其他訊息時， **GetMessage** 會傳回 **WM \_ 油漆** 訊息，而 **DispatchMessage** 會將訊息傳送至適當的視窗程式。

當呼叫 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) 並設定 RDW INTERNALPAINT 旗標之後，視窗可能會接收內部繪製訊息 \_ 。 在此情況下，視窗可能沒有更新區域。 應用程式可能會呼叫 [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) 函式來判斷視窗是否有更新區域。 如果 **GetUpdateRect** 傳回零，則應用程式不需要呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函數。

應用程式必須藉由查看每個 **wm \_ 油漆** 訊息的內部資料結構來檢查是否有任何必要的內部繪製，因為 **wm \_ 油漆** 訊息可能是因為非 Null 的更新區域和使用 RDW INTERNALPAINT 旗標集的 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) 呼叫所造成 \_ 。

系統只會傳送內部的 **WM \_ 油漆** 訊息一次。 從 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)傳回內部的 **wm \_ 油漆** 訊息，或透過 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)將其傳送至視窗之後，系統不會在視窗失效之前張貼或傳送進一步的 **wm \_ 油漆** 訊息，或直到使用 RDW INTERNALPAINT 旗標設定再次呼叫 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)為止 \_ 。

針對某些常見的控制項，預設的 **WM \_ 油漆** 訊息處理會檢查 *wParam* 參數。 如果 *wParam* 不是 Null，則控制項會假設值為 HDC，並且使用該裝置內容繪製。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[繪製和繪製總覽](painting-and-drawing.md)
</dt> <dt>

[繪製和繪製訊息](painting-and-drawing-messages.md)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ NCPAINT**](wm-ncpaint.md)
</dt> <dt>

[**WM \_ 列印**](wm-print.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
