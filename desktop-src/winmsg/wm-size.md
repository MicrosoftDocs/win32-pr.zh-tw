---
Description: 在視窗大小變更之後傳送至視窗。
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: 'WM_SIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548218"
---
# <a name="wm_size-message"></a>WM \_ 大小訊息

在視窗大小變更之後傳送至視窗。

視窗會透過其 [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數接收此訊息。


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要求的調整大小類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                   | 意義                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**大小 \_MAXHIDE**</dt> <dt>4</dt> </dl>       | 當某個其他視窗最大化時，訊息會傳送至所有快顯視窗。<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**大小 \_最大化**</dt> <dt>2</dt> </dl> | 視窗已經最大化。<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**大小 \_MAXSHOW**</dt> <dt>3</dt> </dl>       | 當某個其他視窗還原成先前的大小時，訊息會傳送至所有快顯視窗。<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**大小 \_最小化**</dt> <dt>1</dt> </dl> | 視窗已經過最小化。<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**大小 \_還原**</dt> <dt>0</dt> </dl>    | 視窗已調整大小，但不會套用 **大小 \_ 最小化** 或 **大小 \_ 最大化** 的值。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的低序位字組指定工作區的新寬度。

*LParam* 的高序位字指定了工作區的新高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="example"></a>範例

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

GitHub 上[Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp)的範例。

## <a name="remarks"></a>備註

如果針對子視窗呼叫 [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) 或 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式作為 **WM \_ 大小** 訊息的結果，則 *bRedraw* 或 *bRepaint* 參數應為非零，以使視窗重新繪製。

雖然視窗的寬度和高度是32位的值，但 *lParam* 參數只會包含每個值的低序位16位。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會在處理 [**wm \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)訊息時，傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。
如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
