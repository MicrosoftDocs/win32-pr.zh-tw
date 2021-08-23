---
title: 'EN_LOWFIRTF (Richedit 的通知碼) '
description: 通知 Microsoft Rich Edit 控制項的父視窗，表示收到不支援的 Rtf 格式 (RTF) 關鍵字。 Rich Edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576318"
---
# <a name="en_lowfirtf-notification-code"></a>EN \_ LOWFIRTF 通知碼

通知 Microsoft Rich Edit 控制項的父視窗，表示收到不支援的 Rtf 格式 (RTF) 關鍵字。 Rich Edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼不會傳回值。

## <a name="remarks"></a>備註

若要接收 EN \_ LOWFIRTF 通知，請 \_ 在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息傳送的遮罩中指定 ENM LOWFIRTF 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> </dl>

 

 





