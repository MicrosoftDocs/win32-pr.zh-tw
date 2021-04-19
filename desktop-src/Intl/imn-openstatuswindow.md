---
description: 當 IME 即將建立狀態視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: 'IMN_OPENSTATUSWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977348"
---
# <a name="imn_openstatuswindow-notification-code"></a>IMN \_ OPENSTATUSWINDOW 通知碼

當 IME 即將建立狀態視窗時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMN \_ OPENSTATUSWINDOW。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此命令沒有傳回值。

## <a name="remarks"></a>備註

應用程式會處理此命令，以顯示 IME 本身的狀態視窗。

IME 視窗在處理此命令時，會建立狀態視窗，並將在視窗中顯示的字串設定為輸入內容。 應用程式可以使用 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 函數來取得狀態視窗的相關資訊。

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**WM \_ 輸入法 \_ 通知**](wm-ime-notify.md)
</dt> </dl>

 

 




