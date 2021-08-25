---
title: 'TBN_ENDDRAG (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已停止拖曳工具列中的按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff6cfff7448f452223681ef1ebf720e0330c1fee52ba48862411978d53a0616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876868"
---
# <a name="tbn_enddrag-notification-code"></a>TBN \_ ENDDRAG 通知碼

通知工具列的父視窗，指出使用者已停止拖曳工具列中的按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。 **IItem** 成員包含所拖曳按鈕的命令識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





