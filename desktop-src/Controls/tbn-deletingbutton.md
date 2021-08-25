---
title: 'TBN_DELETINGBUTTON 訊息 (Commctrl .h) '
description: 工具列控制項在即將刪除按鈕時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a426d32af308d6d254a4221bbf35b103b401f07ab1ba6fa74801b6debd46ab70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876968"
---
# <a name="tbn_deletingbutton-message"></a>TBN \_ DELETINGBUTTON 訊息

工具列控制項在即將刪除按鈕時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標，其中包含要刪除之按鈕的相關資訊。 針對此通知碼，只有此結構的 **hdr** 和 **iItem** 成員有效。 此結構的 **iItem** 成員包含所要刪除按鈕的命令識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





