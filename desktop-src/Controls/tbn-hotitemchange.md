---
title: 'TBN_HOTITEMCHANGE (Commctrl 的通知碼) '
description: 當熱 (反白顯示) 專案變更時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685505"
---
# <a name="tbn_hotitemchange-notification-code"></a>TBN \_ HOTITEMCHANGE 通知碼

當熱 (反白顯示) 專案變更時，由工具列控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以允許反白顯示專案，或傳回非零值以防止專案反白顯示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





