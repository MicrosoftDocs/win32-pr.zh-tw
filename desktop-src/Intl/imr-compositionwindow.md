---
description: 當選取的輸入法需要組合視窗的相關資訊時，通知應用程式。 應用程式會透過 WM \_ IME 要求訊息接收此命令 \_ ，並使用如下所示的參數設定。
ms.assetid: 08fd7119-d225-4a78-b2cd-8b58887c9139
title: 'IMR_COMPOSITIONWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af0481ccebc59968fe85a489c856388a04dbece
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983484"
---
# <a name="imr_compositionwindow-notification-code"></a>IMR \_ COMPOSITIONWINDOW 通知碼

當選取的輸入法需要組合視窗的相關資訊時，通知應用程式。 應用程式會透過 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，並使用如下所示的參數設定。


```C++
LRESULT IMR_COMPOSITIONWINDOW
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ COMPOSITIONWINDOW。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

包含 [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) 結構之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式填滿 [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) 結構，則傳回非零值。 否則，此命令會傳回0。

## <a name="remarks"></a>備註

此命令可由 IME 傳送至已 \_ 在 [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息處理常式中清除 ISC SHOWUICOMPOSITIONWINDOW 旗標的視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Imm (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員命令](input-method-manager-commands.md)
</dt> <dt>

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




