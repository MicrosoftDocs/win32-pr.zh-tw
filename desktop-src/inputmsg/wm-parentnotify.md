---
title: WM_PARENTNOTIFY 訊息
description: 當子系視窗發生重大動作時，傳送至視窗。
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5de0845f906e72a42fa8d9a290c6cd8ac16cc0e96cae21ac25b3e9d7810309e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829568"
---
# <a name="wm_parentnotify-message"></a>WM_PARENTNOTIFY 訊息

當子系視窗發生重大動作時，傳送至視窗。 這則訊息現在已擴充，以包含 [**WM_POINTERDOWN**](wm-pointerdown.md) 事件。 建立子視窗時，系統會在建立視窗的 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式之前傳送 [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 。 當子視窗被終結時，系統會先傳送訊息，然後再進行任何損毀視窗的處理。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*WParam* 的低序位文字指定要通知其父代的事件。 高序位字的值取決於低序位字組的值。 此參數可以是下列其中一個值。



| LOWORD (*wParam*)                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | 正在建立子視窗。<br/> HIWORD (*wParam*) 是子視窗的識別碼。<br/> *lParam* 是子視窗的控制碼。<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | 正在終結子視窗。<br/> HIWORD (*wParam*) 是子視窗的識別碼。<br/> *lParam* 是子視窗的控制碼。<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | 使用者已將游標放在子視窗上方，並已按下滑鼠左鍵。<br/> 未定義 HIWORD (*wParam*) 。<br/> *lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | 使用者已將游標放在子視窗上方，並已按下滑鼠左鍵。<br/> 未定義 HIWORD (*wParam*) 。<br/> *lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | 使用者將游標放在子視窗上方，然後按一下滑鼠右鍵。<br/> 未定義 HIWORD (*wParam*) 。<br/> *lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | 使用者已將游標放在子視窗上方，並已按一下第一個或第二個 X 按鈕。<br/> HIWORD (*wParam*) 指出已按下的按鈕。 此參數可以是下列其中一個值： XBUTTON1 或 XBUTTON2。<br/> *lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | 指標已與子視窗建立聯繫。<br/> HIWORD (*wParam*) 包含產生 [**WM_POINTERDOWN**](wm-pointerdown.md) 事件之指標的識別碼。<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

包含指標的點位置。

> [!Note]  
> 因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。 如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。

 

您可以使用下列宏來取出點的實際螢幕座標。

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則會傳回零。

如果應用程式未處理此訊息，則會呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="remarks"></a>備註

此訊息也會傳送至子視窗的所有上階視窗，包括最上層視窗。

除了具有 **WS_EX_NOPARENTNOTIFY** 延伸視窗樣式以外的所有子視窗，會將此訊息傳送至其父視窗。 依預設，對話方塊中的子視窗會有 **WS_EX_NOPARENTNOTIFY** 樣式，除非呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立沒有此樣式的子視窗。

此通知可讓子視窗的上階視窗有機會檢查指標資訊，並且在必要時使用指標捕捉函式來捕捉指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

