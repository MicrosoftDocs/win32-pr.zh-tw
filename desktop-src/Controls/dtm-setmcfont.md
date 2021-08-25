---
title: 'DTM_SETMCFONT 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。 您可以明確地傳送此訊息，或使用 DateTime \_ SetMonthCalFont 宏。
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877808"
---
# <a name="dtm_setmcfont-message"></a>DTM \_ SETMCFONT 訊息

設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將設定之字型的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

指定是否應該在設定字型時立即重新繪製控制項。 將此參數設定為 **TRUE** 會使控制項重新繪製。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





