---
title: 'WM_CAPTURECHANGED 訊息 (Winuser .h) '
description: 傳送至遺失滑鼠捕捉的視窗。
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094355"
---
# <a name="wm_capturechanged-message"></a>WM \_ CAPTURECHANGED 訊息

傳送至遺失滑鼠捕捉的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

取得滑鼠捕捉的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

即使視窗呼叫 [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) 本身，也會收到此訊息。 應用程式不應該嘗試設定滑鼠捕捉以回應此訊息。

當它收到這則訊息時，視窗應該視需要重繪自己，以反映新的滑鼠捕捉狀態。

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

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> </dl>

 

