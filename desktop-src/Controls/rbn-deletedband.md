---
title: 'RBN_DELETEDBAND (Commctrl 的通知碼) '
description: 在刪除帶狀之後，由 Rebar 控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843916"
---
# <a name="rbn_deletedband-notification-code"></a>RBN \_ DELETEDBAND 通知碼

在刪除帶狀之後，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





