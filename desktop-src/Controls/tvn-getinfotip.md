---
title: 'TVN_GETINFOTIP (Commctrl 的通知碼) '
description: 由具有電視提示樣式的樹狀檢視控制項所傳送 \_ 。 當控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。 通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5129e1fa97397cfa9c037c7c65099ee3bd961f184b1bf9b43d2dc87e35880f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261158"
---
# <a name="tvn_getinfotip-notification-code"></a>IZDEBSKI \_ GETINFOTIP 通知碼

由具有 [**電視 \_**](tree-view-control-window-styles.md) 提示樣式的樹狀檢視控制項所傳送。 當控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。 通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項會忽略此通知碼的傳回值。

## <a name="remarks"></a>備註

此通知碼僅由具有 [**電視 \_**](tree-view-control-window-styles.md) 提示樣式的樹狀檢視控制項所傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_GETINFOTIPW** (Unicode) 和 **izdebski \_ GETINFOTIPA** (ANSI) <br/>             |



 

 





