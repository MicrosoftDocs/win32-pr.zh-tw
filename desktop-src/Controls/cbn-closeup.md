---
title: 'CBN_CLOSEUP (Winuser 的通知碼) '
description: 在下拉式方塊的清單方塊已關閉時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106445"
---
# <a name="cbn_closeup-notification-code"></a>CBN \_ 特寫通知碼

在下拉式方塊的清單方塊已關閉時傳送。 下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。


```C++
CBN_CLOSEUP

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

如果使用者變更目前的選取範圍，下拉式方塊也會在下拉式清單關閉時傳送 [CBN \_ SELCHANGE](cbn-selchange.md) 通知碼。 一般來說，您無法預測通知碼的傳送順序。 尤其是在 \_ CBN \_ 特寫通知碼之前或之後，可能會發生 CBN SELCHANGE 通知碼。

若要在每次使用者選取清單專案時執行特定進程，您可以處理 [CBN \_ SELCHANGE](cbn-selchange.md) 或 CBN \_ 特寫通知碼。 一般來說，您會先等候 CBN \_ 特寫通知碼，再處理目前選取範圍內的變更。 如果需要大量的處理，這可能特別重要。

此通知碼不會傳送至具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊。

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

[CBN \_ 下拉式清單](cbn-dropdown.md)
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

 

