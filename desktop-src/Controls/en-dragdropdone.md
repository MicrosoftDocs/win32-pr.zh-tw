---
title: 'EN_DRAGDROPDONE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，拖放作業已完成。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb498361de04184823ab0d0652cc32adc9cbb1978bd6f303b7b215417f99f552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436868"
---
# <a name="en_dragdropdone-notification-code"></a>EN \_ DRAGDROPDONE 通知碼

通知 rich edit 控制項的父視窗，拖放作業已完成。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼不會傳回值。

## <a name="remarks"></a>備註

若要接收 EN \_ DRAGDROPDONE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md)旗標。

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> </dl>

 

 





