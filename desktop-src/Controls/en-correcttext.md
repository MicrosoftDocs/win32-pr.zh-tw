---
title: 'EN_CORRECTTEXT (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗 SYV \_ 正確的手勢發生，讓父視窗有機會取消更正文字。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019416"
---
# <a name="en_correcttext-notification-code"></a>EN \_ CORRECTTEXT 通知碼

通知 rich edit 控制項父視窗 SYV \_ 正確的手勢發生，讓父視窗有機會取消更正文字。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

指定要更正之選取範圍的 [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以忽略動作。

傳回非零值以處理動作。

## <a name="remarks"></a>備註

只有在有可用的畫筆功能時，才會傳送此通知碼。

若要接收 EN \_ CORRECTTEXT 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) 。

> [!Note]  
> \_只有在 rich edit 1.0 版中才支援 EN CORRECTTEXT 通知碼。 較新版本的 rich edit 不支援此功能。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





