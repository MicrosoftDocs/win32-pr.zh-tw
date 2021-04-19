---
title: 'CBN_DBLCLK (Winuser 的通知碼) '
description: 當使用者在下拉式方塊的清單方塊中按兩下字串時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001316"
---
# <a name="cbn_dblclk-notification-code"></a>CBN \_ DBLCLK 通知碼

當使用者在下拉式方塊的清單方塊中按兩下字串時傳送。 下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
CBN_DBLCLK

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

此通知程式碼只會針對具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊進行。 在具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊中，只要按一下即可關閉清單方塊，就無法按兩下。

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

