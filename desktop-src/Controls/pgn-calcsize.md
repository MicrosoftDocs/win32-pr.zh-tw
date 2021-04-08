---
title: 'PGN_CALCSIZE (Commctrl 的通知碼) '
description: 由分頁控制項傳送以取得所包含視窗的可滾動維度。
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685837"
---
# <a name="pgn_calcsize-notification-code"></a>PGN \_ CALCSIZE 通知碼

由分頁控制項傳送以取得所包含視窗的可滾動維度。 這些維度是由分頁控制項用來判斷所包含視窗的可滾動大小。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize)結構的指標，其中包含和接收通知程式碼的相關資訊。 此結構的 **>dwflag** 成員指出正在計算的維度。 根據 **>dwflag** 的值，您應該將所需的維度放在此結構的 **iWidth** 或 **iHeight** 成員中。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





