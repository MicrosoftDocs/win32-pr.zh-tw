---
title: 'MCN_GETDAYSTATE (Commctrl 的通知碼) '
description: 由月曆控制項傳送，可要求有關如何顯示個別日期的資訊。 此通知碼只會由使用 MCS DAYSTATE 樣式的月曆控制項來傳送 \_ ，而且會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685955"
---
# <a name="mcn_getdaystate-notification-code"></a>MCN \_ GETDAYSTATE 通知碼

由月曆控制項傳送，可要求有關如何顯示個別日期的資訊。 此通知碼只會由使用 [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) 樣式的月曆控制項來傳送，而且會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate)結構的指標。 結構包含控制項需要資訊之時間範圍的相關資訊，並且會接收提供此資料的陣列位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

處理此通知碼可讓您的應用程式藉由指定以粗體顯示特定日期，來自訂其顯示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





