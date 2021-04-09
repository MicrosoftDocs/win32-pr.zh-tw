---
title: 'WM_MEASUREITEM 訊息 (Winuser .h) '
description: 當控制項或功能表建立時，傳送至下拉式方塊、清單方塊、清單視圖或功能表項目的擁有者視窗。
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843876"
---
# <a name="wm_measureitem-message"></a>WM \_ MEASUREITEM 訊息

當控制項或功能表建立時，傳送至下拉式方塊、清單方塊、清單視圖或功能表項目的擁有者視窗。

視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含 *lParam* 參數所指向之 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的 **CtlID** 成員的值。 此值會識別傳送了 **WM \_ MEASUREITEM** 訊息的控制項。 如果值為零，則會由功能表傳送訊息。 如果此值為非零值，則會由下拉式方塊或清單方塊傳送訊息。 如果此值為非零值，而且 *lParam* 所指向之 **MEASUREITEMSTRUCT** 的 **ITEMID** 成員值是 (UINT) 1，則訊息是由組合編輯欄位所傳送。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的指標，其中包含主控描繪控制項或功能表項目的維度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。

## <a name="remarks"></a>備註

當擁有者視窗收到 **WM \_ MEASUREITEM** 訊息時，擁有者會填入訊息的 *lParam* 參數所指向的 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構並傳回; 這會通知系統有控制項的維度。 如果清單方塊或下拉式方塊是以 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 或 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式來建立，則會將此訊息傳送給控制項中每個專案的擁有者; 否則，此訊息會傳送一次。

系統會將 **wm \_ MEASUREITEM** 訊息傳送至下拉式方塊的擁有者視窗，以及使用 OWNERDRAWFIXED 樣式建立的清單方塊，然後再傳送 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。 如此一來，當擁有者收到此訊息時，系統尚未判斷控制項中所使用之字型的高度和寬度;需要這些值的函式呼叫和計算應該會出現在應用程式或程式庫的主要功能中。

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

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

