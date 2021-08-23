---
title: 'HDM_ORDERTOINDEX 訊息 (Commctrl .h) '
description: 根據標題控制項中的順序，抓取專案的索引值。 您可以明確地傳送此訊息，或使用標頭 \_ OrderToIndex 宏。
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7afd006c90684137ffc484dac62ab40c04d90c0cdbc87f51102d8e9119e8b14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576257"
---
# <a name="hdm_ordertoindex-message"></a>HDM \_ ORDERTOINDEX 訊息

根據標題控制項中的順序，抓取專案的索引值。 您可以明確地傳送此訊息，或使用 [**標頭 \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

專案在標題控制項內出現的順序，由左至右。 例如，在最左邊的資料行中，專案的索引值會是0。 右邊的下一個專案的值為1，依此類推。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回表示專案索引的 INT。 如果 *wParam* 無效 (負或太大) ，則傳回等於 *wParam*。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





