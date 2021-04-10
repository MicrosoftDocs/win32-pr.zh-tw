---
title: 'CBN_EDITUPDATE (Winuser 的通知碼) '
description: 當下拉式方塊的編輯控制項部分即將顯示變更的文字時傳送。
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106284"
---
# <a name="cbn_editupdate-notification-code"></a>CBN \_ EDITUPDATE 通知碼

當下拉式方塊的編輯控制項部分即將顯示變更的文字時傳送。 此通知碼會在控制項格式化文字之後，但在顯示文字之前傳送。 下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
CBN_EDITUPDATE

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

如果下拉式方塊具有 [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) 樣式，則不會傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[CBN \_ EDITCHANGE](cbn-editchange.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

