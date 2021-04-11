---
title: 'DTM_SETMCSTYLE 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的樣式。 請明確地傳送此訊息，或使用 DateTime \_ SetMonthCalStyle 宏。
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE message Windows 控制項
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
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104838"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





