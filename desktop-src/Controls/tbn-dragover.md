---
title: 'TBN_DRAGOVER (Commctrl 的通知碼) '
description: Ascertains 是否 \_ 應針對要拖曳的按鈕傳送一則 TB MARKBUTTON 訊息。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829342"
---
# <a name="tbn_dragover-notification-code"></a>TBN \_ system.windows.dragdrop.dragover> 通知碼

Ascertains 是否應針對要拖曳的按鈕傳送一則 [**TB \_ MARKBUTTON**](tb-markbutton.md) 訊息。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)結構的指標，指定要將哪些專案拖曳至其中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果工具列應該傳送 TB 的 MARKBUTTON 訊息，則為 **FALSE** ， \_ 否則為 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





