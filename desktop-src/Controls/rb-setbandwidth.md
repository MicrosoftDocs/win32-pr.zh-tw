---
title: 'RB_SETBANDWIDTH 訊息 (Commctrl .h) '
description: 設定停駐區的寬度。
ms.assetid: dca9dfe9-3e5a-40bb-8de7-a296e6be7d06
keywords:
- RB_SETBANDWIDTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBANDWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc30b8cd4cdb3a9d6f5e6123ec46df6565a0ccb19d3920fe67c50a57cd15fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409178"
---
# <a name="rb_setbandwidth-message"></a>RB \_ SETBANDWIDTH 訊息

設定停駐區的寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

寬線的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

新的寬度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已設定值，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





