---
title: 'EN_MSGFILTER (Richedit 的通知碼) '
description: 在控制項中通知 rich edit 控制項的鍵盤或滑鼠事件的父視窗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d2cbe47af3d74deb4795946d58871b4729118db0e839027e78e05976ebf855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436708"
---
# <a name="en_msgfilter-notification-code"></a>EN \_ MSGFILTER 通知碼

在控制項中通知 rich edit 控制項的鍵盤或滑鼠事件的父視窗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)結構，其中包含鍵盤或滑鼠訊息的相關資訊。 如果父視窗修改此結構並傳回非零值，則會處理修改過的訊息，而不是原始的訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果控制項應該處理鍵盤或滑鼠事件，則傳回零。

如果控制項應該忽略鍵盤或滑鼠事件，則傳回非零。

## <a name="remarks"></a>備註

若要接收 \_ 事件的 EN MSGFILTER 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息傳送的遮罩中指定下列一或多個旗標。



| 旗標                                                                             | 意義                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | 接收鍵盤事件的通知碼。     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | 接收滑鼠事件的通知碼。        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | 接收滑鼠滾輪事件的通知碼。 |



 

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

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





