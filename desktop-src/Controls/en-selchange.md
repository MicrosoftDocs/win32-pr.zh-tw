---
title: 'EN_SELCHANGE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，指出目前的選取範圍已變更。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686290"
---
# <a name="en_selchange-notification-code"></a>EN \_ SELCHANGE 通知碼

通知 rich edit 控制項的父視窗，指出目前的選取範圍已變更。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)結構，可接收選取專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼不會傳回值。

## <a name="remarks"></a>備註

若要接收 EN \_ SELCHANGE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) 。

當插入號位置變更，但未選取任何文字時，就會傳送此通知碼 (選取範圍是空的) 。 當使用者按一下滑鼠、輸入或按下方向鍵時，插入號位置可能會變更。

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





