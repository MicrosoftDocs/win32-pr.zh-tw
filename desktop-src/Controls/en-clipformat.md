---
title: 'EN_CLIPFORMAT (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，貼上有特定剪貼簿格式的貼上。 無視窗的 rich edit 控制項會使用 ITextHost TxNotify 方法傳送這項通知。
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934202"
---
# <a name="en_clipformat-notification-code"></a>EN \_ CLIPFORMAT 通知碼

通知 rich edit 控制項的父視窗，貼上有特定剪貼簿格式的貼上。 無視窗的 rich edit 控制項會使用 [**ITextHost：： TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法傳送這個通知。


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

藉由呼叫 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函式與 GWL 識別碼值來抓取的視窗識別碼 \_ 。

</dd> <dt>

*lParam* 
</dt> <dd>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)結構的指標，其中包含剪貼簿格式的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

若要接收 EN \_ CLIPFORMAT 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

