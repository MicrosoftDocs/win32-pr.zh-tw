---
title: 'EN_REQUESTRESIZE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，控制項的內容小於控制項的視窗大小。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047578"
---
# <a name="en_requestresize-notification-code"></a>EN \_ REQUESTRESIZE 通知碼

通知 rich edit 控制項的父視窗，控制項的內容小於控制項的視窗大小。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

接收所要求大小的 [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼不會傳回值。

## <a name="remarks"></a>備註

若要支援 rich edit 控制項的無底邊行為，父視窗必須在收到此通知碼時調整控制項的大小。

若要接收 EN \_ REQUESTRESIZE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) 。

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





