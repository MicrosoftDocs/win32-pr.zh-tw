---
title: 'BCN_DROPDOWN (Winuser 的通知碼) '
description: 當使用者按一下按鈕上的下拉箭號時傳送。 控制項的父視窗會以 WM 通知訊息的形式接收此通知碼 \_ 。
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965292"
---
# <a name="bcn_dropdown-notification-code"></a>BCN \_ 下拉式通知碼

當使用者按一下按鈕上的下拉箭號時傳送。 控制項的父視窗會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式接收此通知碼。


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)結構的指標。 **RcButton** 成員會設定為描述下拉式區域。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 **LPARAM** 來取出 [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) 結構。 **WPARAM** 包含傳送此訊息之控制項的識別碼。 按鈕控制項必須要有下拉式按鈕樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



 

 





