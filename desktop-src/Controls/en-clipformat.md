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
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437038"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

