---
description: 當 IME 即將關閉狀態視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: 'IMN_CLOSESTATUSWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971825"
---
# <a name="imn_closestatuswindow-notification-code"></a>IMN \_ CLOSESTATUSWINDOW 通知碼

當 IME 即將關閉狀態視窗時，通知應用程式。 應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMN \_ CLOSESTATUSWINDOW。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此命令沒有傳回值。

## <a name="remarks"></a>備註

如果應用程式顯示 IME 的狀態視窗，則應該處理此命令。

在處理此命令時，IME 視窗會關閉狀態視窗。

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

[**WM \_ 輸入法 \_ 通知**](wm-ime-notify.md)
</dt> </dl>

 

 




