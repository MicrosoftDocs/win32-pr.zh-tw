---
title: 'DTM_SETSYSTEMTIME 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的時間。 您可以明確地傳送此訊息，或使用 DateTime \_ SetSystemtime 宏。
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd0c6a09e3fc7bd9d068e27049329f3289a8ba1968ffae4592c7e07db9f2eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088968"
---
# <a name="dtm_setsystemtime-message"></a>DTM \_ SETSYSTEMTIME 訊息

設定日期和時間選擇器 (DTP) 控制項的時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定應執行的動作。 此值必須設定為下列其中一項：



| 值                                                                                                                                             | 意義                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ 有效**</dt> </dl> | 根據 *lParam* 指向的結構內的資料，設定 DTP 控制項。 <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ 無**</dt> </dl>    | 將 [DTP] 控制項設定為 [無日期]，並清除其核取方塊。 當指定這個旗標時，會忽略 *lParam* 。 此旗標只適用于設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) 樣式的 DTP 控制項。 <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含用來設定 DTP 控制項的系統時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

