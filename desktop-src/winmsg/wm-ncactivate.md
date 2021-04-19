---
description: 當工作區的非工作區需要變更以表示使用中或非作用中狀態時，傳送至視窗。
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: 'WM_NCACTI加值稅E 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974457"
---
# <a name="wm_ncactivate-message"></a>WM \_ NCACTI加值稅E 訊息

當工作區的非工作區需要變更以表示使用中或非作用中狀態時，傳送至視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出何時需要變更標題列或圖示，以指出作用中或非作用中狀態。 如果要繪製現用標題列或圖示， *wParam* 參數就是 **TRUE**。 如果要繪製非使用中的標題列或圖示， *wParam* 是 **FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

當 [視覺效果樣式](../controls/themes-overview.md) 在此視窗中為作用中時，不會使用此參數。

當此視窗的視覺化樣式不在作用中時，此參數是視窗非工作區之選擇性更新區域的控制碼。 如果此參數設定為-1， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 就不會重新繪製非工作區，以反映狀態變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

當 *wParam* 參數為 **FALSE** 時，應用程式應該傳回 **TRUE** ，表示系統應繼續進行預設處理，否則應該傳回 **FALSE** 以防止變更。 當 *wParam* 為 **TRUE** 時，會忽略傳回值。

## <a name="remarks"></a>備註

不建議處理與標準視窗的非工作區相關的訊息，因為應用程式必須能夠為視窗的非工作區繪製所有必要的部分。 如果應用程式處理此訊息，則必須傳回 **TRUE** ，以指示系統完成使用中視窗的變更。 如果接收到此訊息時視窗最小化，則應用程式應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。

當 *wParam* 參數為 **TRUE** 時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會使用其使用中色彩來繪製標題列或圖示標題，當 *wParam* 為 **FALSE** 時，則會以其非作用中色彩來繪製。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
