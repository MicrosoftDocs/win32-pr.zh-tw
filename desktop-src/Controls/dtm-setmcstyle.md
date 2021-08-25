---
title: 'DTM_SETMCSTYLE 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的樣式。 請明確地傳送此訊息，或使用 DateTime \_ SetMonthCalStyle 宏。
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877798"
---
# <a name="dtm_setmcstyle-message"></a>DTM \_ SETMCSTYLE 訊息

設定日期和時間選擇器 (DTP) 控制項的樣式。 請明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>樣式值。 如需詳細資訊，請參閱 <a href="month-calendar-control-styles.md">月曆控制項樣式</a>。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回上一個樣式的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





