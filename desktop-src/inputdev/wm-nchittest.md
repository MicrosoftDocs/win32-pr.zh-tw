---
title: 'WM_NCHITTEST 訊息 (Winuser .h) '
description: 傳送至視窗，以判斷視窗的哪個部分對應至特定的螢幕座標。
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983310"
---
# <a name="wm_nchittest-message"></a>WM \_ NCHITTEST 訊息

傳送至視窗，以判斷視窗的哪個部分對應至特定的螢幕座標。 例如，當游標移動時、按下或放開滑鼠按鍵時，或為了回應函式（例如 [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint)）的呼叫時，就會發生這種情況。 如果未捕捉到滑鼠，則會將訊息傳送至游標下的視窗。 否則，訊息會傳送至已捕捉滑鼠的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定游標的 x 座標。 座標相對於畫面的左上角。

高序位字組指定游標的 y 座標。 座標相對於畫面的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式的傳回值是下列其中一個值，表示游標作用點的位置。



| 傳回碼/值                                                                                                                                    | Description                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | 在沒有調整大小框線的視窗框線中。<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | 在可調整大小之視窗的水準框線 (使用者可以按一下滑鼠，以垂直方式調整視窗的大小) 。<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | 在可調整大小之視窗框線的左下角 (使用者可以按一下滑鼠，以對角線方式調整視窗的大小) 。<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | 在可調整大小之視窗框線的右下角 (使用者可以按一下滑鼠，以對角線方式調整視窗的大小) 。<br/>                                                                             |
| <dl> <dt>**HTCAPTION**</dt> <dt>2</dt> </dl>      | 在標題列中。<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | 在工作區中。<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | 在 [ **關閉** ] 按鈕中。<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | 在螢幕背景上或 windows (與 **HTNOWHERE** 相同的分隔線上，不同之處在于 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會產生系統嗶聲，指出) 錯誤。<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | 在 [大小] 方塊中 (與 **HTSIZE**) 相同。<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | **在 [說明] 按鈕中**。<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | 水準捲軸。<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | 在可調整大小之視窗的左邊框線中 (使用者可以按一下滑鼠，以水準方式調整視窗的大小) 。<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | 在功能表中。<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | 在 [ **最大化** ] 按鈕中。<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | 在 [ **最小化** ] 按鈕中。<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | 在螢幕背景或視窗之間的分隔線上。<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | 在 [ **最小化** ] 按鈕中。<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | 在可調整大小之視窗的右框線中 (使用者可以按一下滑鼠，以水準方式調整視窗的大小) 。<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | 在 [大小] 方塊中 (與 **HTGROWBOX**) 相同。<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | 在 [視窗] 功能表或子視窗的 [ **關閉** ] 按鈕中。<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | 在視窗的上水準框線中。<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | 在視窗框線的左上角。<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | 在視窗框線的右上角。<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | 在目前由相同執行緒中的另一個視窗所涵蓋的視窗中 (會將訊息傳送至相同執行緒中的基礎視窗，直到其中一個傳回未 **HTTRANSPARENT**) 的程式碼為止。<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | 在垂直捲動條中。<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | 在 [ **最大化** ] 按鈕中。<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

使用下列程式碼來取得水準和垂直位置：


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。 如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。 您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。

> [!IMPORTANT]
> 請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。 具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。

 

**Windows Vista：** 建立包含標準標題按鈕的自訂框架時，應先將此訊息傳遞至 [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) 函式。 這可讓桌面視窗管理員 (DWM) 提供標題按鈕的點擊測試。 如果 **DwmDefWindowProc** 未處理訊息，可能需要進一步處理 **WM \_ NCHITTEST** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windowsx) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**點**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

