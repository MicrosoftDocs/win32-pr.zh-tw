---
title: 'EN_ALIGN_LTR_EC (Winuser 的通知碼) '
description: 當使用者將編輯控制項方向從左至右變更時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685780"
---
# <a name="en_align_ltr_ec-notification-code"></a>EN \_ 對齊 \_ LTR \_ EC 通知碼

當使用者將編輯控制項方向從左至右變更時傳送。 編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
EN_ALIGN_LTR_EC

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

