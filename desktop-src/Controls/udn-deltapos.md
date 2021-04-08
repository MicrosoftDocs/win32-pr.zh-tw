---
title: 'UDN_DELTAPOS (Commctrl 的通知碼) '
description: 當控制項的位置即將變更時，作業系統會將其傳送至上下按鈕控制項的父視窗。
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685953"
---
# <a name="udn_deltapos-notification-code"></a>UDN \_ DELTAPOS 通知碼

當控制項的位置即將變更時，作業系統會將其傳送至上下按鈕控制項的父視窗。 當使用者按下控制項的向上或向下箭號時，就會發生這種情況。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown)結構的指標，其中包含位置變更的相關資訊。 此結構的 **iPos** 成員包含控制項的目前位置。 結構的 **iDelta** 成員是帶正負號的整數，其中包含位置的建議變更。 如果使用者按一下 [向上] 按鈕，這就是正值。 如果使用者按一下 [向下] 按鈕，則此值為負值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零以防止控制項的位置變更，或傳回零以允許變更。

## <a name="remarks"></a>備註

UDN \_ DELTAPOS 通知碼會在 [**wm \_ VSCROLL**](wm-vscroll.md) 或 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息之前傳送，這會實際變更控制項的位置。 這可讓您檢查、允許、修改或禁止變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

