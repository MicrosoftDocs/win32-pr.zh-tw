---
title: 'HDN_ENDFILTEREDIT (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，篩選編輯已結束。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- HDN_ENDFILTEREDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225ac41a875f6eadb17054c89e34451306cd78db66cc40cc3c26d15035f7c388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435538"
---
# <a name="hdn_endfilteredit-notification-code"></a>HDN \_ ENDFILTEREDIT 通知碼

通知標題控制項的父視窗，篩選編輯已結束。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含正在編輯之篩選的其他資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





