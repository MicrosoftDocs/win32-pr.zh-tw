---
title: WM_POINTERHWHEEL 訊息
description: 當水準滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- WM_POINTERHWHEEL 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5817d5ed243363c82038dc3df2d8f1e337079076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385029"
---
# <a name="wm_pointerhwheel-message"></a>WM_POINTERHWHEEL 訊息

當水準滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標識別碼和輪子差異。 使用下列宏來取得此資訊。

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam) (WPARAM) ：輪子 DELTA 作為帶正負號的簡短值。

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

如果應用程式處理此訊息，則應該傳回零。

如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="remarks"></a>備註

若要取出滾輪滾動單位，請使用呼叫 [**GetPointerInfo**](/previous-versions/windows/desktop/api)函數所傳回 [**POINTER_INFO**](/previous-versions/windows/desktop/api)結構的 **inputData** 。 此欄位包含帶正負號的值，並以 **WHEEL_DELTA** 的倍數表示。 正值表示向前旋轉，負數值表示向前旋轉。

請注意，即使滑鼠游標位於應用程式視窗之外，也可以傳遞輪子輸入。 滾輪訊息的傳遞方式與鍵盤輸入非常類似。 Foregournd 訊息佇列的焦點視窗會接收滾輪訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> </dl>

 

