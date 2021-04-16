---
title: 'MCN_VIEWCHANGE (Commctrl 的通知碼) '
description: 由月曆控制項在目前的視圖變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464529"
---
# <a name="mcn_viewchange-notification-code"></a>MCN \_ VIEWCHANGE 通知碼

由月曆控制項在目前的視圖變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange)結構的指標，其中包含目前視圖的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





