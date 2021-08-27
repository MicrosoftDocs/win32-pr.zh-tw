---
title: 'LBN_SELCANCEL (Winuser 的通知碼) '
description: 通知應用程式使用者已在清單方塊中取消選取。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- LBN_SELCANCEL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cd4826310a8c2528764089ce128db1c1b3db75f7f26748f3d8578ef9ee6ccb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085188"
---
# <a name="lbn_selcancel-notification-code"></a>LBN \_ SELCANCEL 通知碼

通知應用程式使用者已在清單方塊中取消選取。 清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

清單方塊的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

此通知碼只會由具有 L [**BS \_ 通知**](button-styles.md) 樣式的清單方塊來傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCHANGE](lbn-selchange.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

