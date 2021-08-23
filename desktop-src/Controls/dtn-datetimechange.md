---
title: 'DTN_DATETIMECHANGE (Commctrl 的通知碼) '
description: 每次發生變更時，日期和時間選擇器都會傳送 (的 DTP) 控制。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be916859a8c963c81d1f68410e9e821c430832610aa85378a6ae6162e0488bf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877698"
---
# <a name="dtn_datetimechange-notification-code"></a>DTN \_ DATETIMECHANGE 通知碼

每次發生變更時，日期和時間選擇器都會傳送 (的 DTP) 控制。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)結構的指標，其中包含在控制項中發生之變更的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項的擁有者必須傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





