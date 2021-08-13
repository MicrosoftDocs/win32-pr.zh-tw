---
title: 'CBN_DROPDOWN (Winuser 的通知碼) '
description: 在下拉式方塊的清單方塊即將顯示時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978ac01818f3e9ed7da9f3f1decc7398ab4af32df8f884041bec327640a8014d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438298"
---
# <a name="cbn_dropdown-notification-code"></a>CBN \_ 下拉式通知碼

在下拉式方塊的清單方塊即將顯示時傳送。 下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。

</dd> <dt>

*lParam* 
</dt> <dd>

下拉式方塊的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

只有當下拉式方塊具有 [**cbs \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式時，才會傳送此通知碼。

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

[CBN \_ 特寫](cbn-closeup.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

