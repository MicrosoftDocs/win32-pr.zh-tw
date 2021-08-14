---
title: 'CBEN_INSERTITEM (Commctrl 的通知碼) '
description: 在控制項中插入新專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a58c1f8b14f4983e2f7e7444a8110f0407220b0c5bc682cfc73f72bee078ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413664"
---
# <a name="cben_insertitem-notification-code"></a>CBEN \_ INSERTITEM 通知碼

在控制項中插入新專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構的指標，其中包含通知碼和已插入之專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此通知程式碼的應用程式必須傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





