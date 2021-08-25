---
title: 'NM_THEMECHANGED (Commctrl 的通知碼) '
description: 通知控制項的父視窗，主題已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069f4eb2b3727edc19c531f4404b723df2ea775677a25283268c1c20a978dedc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877258"
---
# <a name="nm_themechanged-notification-code"></a>NM \_ THEMECHANGED 通知碼

通知控制項的父視窗，主題已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項會忽略傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





