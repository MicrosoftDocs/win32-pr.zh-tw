---
title: 'TBN_BEGINADJUST (Commctrl 的通知碼) '
description: 通知工具列的父視窗，指出使用者已開始自訂工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- TBN_BEGINADJUST 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b83d14d82b84e493d47e193542b1d2fdc83ba92ccc53bd4cb383f17436ad1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877008"
---
# <a name="tbn_beginadjust-notification-code"></a>TBN \_ BEGINADJUST 通知碼

通知工具列的父視窗，指出使用者已開始自訂工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





