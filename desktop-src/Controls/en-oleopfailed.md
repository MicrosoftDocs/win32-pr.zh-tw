---
title: 'EN_OLEOPFAILED (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗， (COM) 物件的元件物件模型上的使用者動作失敗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436678"
---
# <a name="en_oleopfailed-notification-code"></a>EN \_ OLEOPFAILED 通知碼

通知 rich edit 控制項的父視窗， (COM) 物件的元件物件模型上的使用者動作失敗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)結構，其中包含失敗的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼會傳回零。

## <a name="remarks"></a>備註

父視窗一律會取得這個事件的 [**WM \_ 通知**](wm-notify.md) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。

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

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





