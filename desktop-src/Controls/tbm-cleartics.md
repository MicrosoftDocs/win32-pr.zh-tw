---
title: 'TBM_CLEARTICS 訊息 (Commctrl .h) '
description: 從跟蹤條中移除目前的刻度標記。 此訊息不會移除第一個和最後一個刻度，這些刻度會由 [並排顯示] 自動建立。
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046768"
---
# <a name="tbm_cleartics-message"></a>TBM \_ CLEARTICS 訊息

從跟蹤條中移除目前的刻度標記。 此訊息不會移除第一個和最後一個刻度，這些刻度會由 [並排顯示] 自動建立。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪旗標。 如果此參數為 **TRUE**，則在清除刻度之後，會重新繪製這些標記。 如果此參數為 **FALSE**，則訊息會清除刻度，但不會重新繪製這些標記。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





