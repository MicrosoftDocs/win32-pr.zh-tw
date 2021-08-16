---
title: 'LVN_ITEMCHANGED (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，指出專案已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea129a1b62b442b0fb545f29a57e9eab0d6d1bae057996df5bc269d9a4296d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830382"
---
# <a name="lvn_itemchanged-notification-code"></a>LVN \_ ITEMCHANGED 通知碼

通知清單視圖控制項的父視窗，指出專案已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，該結構會識別專案並指定其屬性已變更。 如果 *lParam* 所指向之結構的 **iItem** 成員為-1，則變更已套用至清單視圖中的所有專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果清單視圖控制項有 [**lvs) \_ OWNERDATA**](list-view-window-styles.md) 樣式，且使用者按住 SHIFT 鍵並按一下滑鼠來選取某個範圍的專案，則 \_ 不會針對每個選取或取消選取的專案傳送 LVN ITEMCHANGED 通知碼。 相反地，您會收到單一 [LVN \_ ODSTATECHANGED](lvn-odstatechanged.md) 通知碼，指出某個範圍的專案已變更狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





