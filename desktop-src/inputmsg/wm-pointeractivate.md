---
title: WM_POINTERACTI加值稅E 訊息
description: 當主要指標在視窗上產生 WM_POINTERDOWN 時，傳送至非使用中的視窗。
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTI加值稅E 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001300"
---
# <a name="wm_pointeractivate-message"></a>WM_POINTERACTI加值稅E 訊息

當主要指標在視窗上產生 [**WM_POINTERDOWN**](wm-pointerdown.md) 時，傳送至非使用中的視窗。 只要訊息保持未處理狀態，它就會向上移動父視窗鏈，直到到達最上層視窗為止。 應用程式可以回應此訊息，以指定是否要啟用它們。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標識別碼和其他資訊。 使用下列宏來取得此資訊。

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。

</dd> <dt>

*lParam* 
</dt> <dd>

包含要啟動之視窗最上層視窗的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回 [備註] 區段中所述的其中一個值。

如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="remarks"></a>備註

應用程式可以處理這則訊息，並傳回下列其中一個值，以判斷系統如何處理啟用和啟用輸入：

-   PA_ACTI加值稅E
-   PA_NOACTI加值稅E

請務必注意，當使用者與具有多個同時指標的系統互動時， **WM_POINTERACTI加值稅E** 訊息代表的啟動機會僅適用于這些指標的第一個。 因此，應用程式應留意到它們在非使用中時，仍會收到指標的輸入。

如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 會將訊息傳遞至父視窗。

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

 

