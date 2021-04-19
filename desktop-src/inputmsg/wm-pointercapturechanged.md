---
title: WM_POINTERCAPTURECHANGED 訊息
description: 傳送至遺失輸入指標之捕捉的視窗。
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966337"
---
# <a name="wm_pointercapturechanged-message"></a>WM_POINTERCAPTURECHANGED 訊息

傳送至遺失輸入指標之捕捉的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含遺失之輸入指標的相關資訊。 使用 [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) 取得指標識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

包含正在捕捉輸入指標的視窗控制碼。 如果該指標不再由視窗所捕捉，則這個值可以是 Null。

如果此訊息是從內部處理產生的，則此值可以是接收訊息的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="remarks"></a>備註

視窗應該使用此通知來停止處理後續的訊息，並起始指標遺失所需的任何清除。 與指標相關聯的手勢的處理也應終止 (例如，呼叫 [**StopInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) 和剩餘的連絡人重新與視窗相關聯。

一般來說，如果視窗收到 **WM_POINTERCAPTURECHANGED** 通知，就不會收到與輸入指標相關的後續通知。 因此，請不要依賴成對的通知，例如 [**WM_POINTERENTER**](wm-pointerenter.md) 和 [**WM_POINTERLEAVE**](wm-pointerleave.md)。

**WM_POINTERCAPTURECHANGED** 不包含 [**POINTER_INFO**](/previous-versions/windows/desktop/api) 的資料。 除了設定的 [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) 旗標以外， [**GetPointerInfo**](/previous-versions/windows/desktop/api) (或任何變異) 所傳回的資料，與通知之前傳回的資料相同。

如果應用程式未處理此通知， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會產生一或多個 [**WM_GESTURE**](../wintouch/wm-gesture.md) 訊息，或者，如果無法辨識手勢， **DefWindowProc** 可能會產生滑鼠輸入。

如果應用程式選擇性地取用一些指標輸入，並將 rest 傳遞給 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)，則產生的行為是未定義的。

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

 

