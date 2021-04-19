---
description: 傳送至使用者正在移動的視窗。 藉由處理這個訊息，應用程式可以監視拖曳矩形的位置，並且視需要變更其位置。
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: 'WM_MOVING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979727"
---
# <a name="wm_moving-message"></a>WM \_ 移動訊息

傳送至使用者正在移動的視窗。 藉由處理這個訊息，應用程式可以監視拖曳矩形的位置，並且視需要變更其位置。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，該結構具有視窗目前的位置，以螢幕座標為單位。 若要變更拖曳矩形的位置，應用程式必須變更此結構的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回 **TRUE** 。

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

[**WM \_ 移動**](wm-move.md)
</dt> <dt>

[**WM 重設 \_ 大小**](wm-sizing.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
