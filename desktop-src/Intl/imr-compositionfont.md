---
description: 當選取的輸入法需要組合視窗所使用之字型的相關資訊時，就會通知應用程式。 應用程式會透過包含參數的 WM \_ IME 要求訊息接收此命令， \_ 如下所示。
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: 'IMR_COMPOSITIONFONT 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980840"
---
# <a name="imr_compositionfont-notification-code"></a>IMR \_ COMPOSITIONFONT 通知碼

當選取的輸入法需要組合視窗所使用之字型的相關資訊時，就會通知應用程式。 應用程式會透過包含參數的 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，如下所示。


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ COMPOSITIONFONT。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

包含 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構之緩衝區的指標。 應用程式會填入目前撰寫視窗的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式填滿 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構，則傳回非零值。 否則，此命令會傳回0。

## <a name="remarks"></a>備註

此命令可由 IME 傳送至在 \_ [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) 訊息處理常式中清除 ISC SHOWUICOMPOSITIONWINDOW 旗標的視窗。

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

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 
