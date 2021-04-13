---
title: 'EN_PROTECTED (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，讓使用者採取動作來變更受保護的文字範圍。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465481"
---
# <a name="en_protected-notification-code"></a>EN \_ 受保護的通知碼

通知 rich edit 控制項的父視窗，讓使用者採取動作來變更受保護的文字範圍。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)結構，其中包含觸發通知碼之訊息的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以允許操作。

傳回非零值以防止作業。

## <a name="remarks"></a>備註

如果傳回零，且 [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)結構的 **msg**、 **wParam** 和 **lParam** 成員有所變更，控制項會處理修改過的訊息，而不是原始訊息。

若要接收 EN-US \_ 受保護的通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ PROTECTED**](rich-edit-control-event-mask-flags.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





