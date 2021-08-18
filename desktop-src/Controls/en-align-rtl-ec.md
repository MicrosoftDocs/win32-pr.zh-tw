---
title: 'EN_ALIGN_RTL_EC (Winuser 的通知碼) '
description: 當使用者將編輯控制項方向變更為由右至左時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437088"
---
# <a name="en_align_rtl_ec-notification-code"></a>EN \_ 靠 \_ 左對齊 \_ EC 通知碼

當使用者將編輯控制項方向變更為由右至左時傳送。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

傳送通知碼之編輯控制項的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

如果您的系統上已安裝雙向語言（例如阿拉伯文或希伯來文），您可以使用 CTRL + LSHIFT (（由左到右）) 和 CTRL + RSHIFT (（由右至左) ）來變更編輯控制項方向。

**Rich Edit：** 不支援此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

