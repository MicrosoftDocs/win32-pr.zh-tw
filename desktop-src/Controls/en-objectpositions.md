---
title: 'EN_OBJECTPOSITIONS (Richedit 的通知碼) '
description: 當控制項讀取物件時，通知 rich edit 控制項的父視窗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843679"
---
# <a name="en_objectpositions-notification-code"></a>EN \_ OBJECTPOSITIONS 通知碼

當控制項讀取物件時，通知 rich edit 控制項的父視窗。 Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以繼續 **讀取** 操作。

傳回非零值以停止 **讀取** 作業。

## <a name="remarks"></a>備註

若要接收 EN \_ OBJECTPOSITIONS 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md)旗標。

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**WM \_ 通知**](wm-notify.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

