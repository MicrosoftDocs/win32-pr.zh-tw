---
title: 'MCM_GETFIRSTDAYOFWEEK 訊息 (Commctrl .h) '
description: 抓取月曆控制項的每週第一天。 您可以使用 MonthCal GetFirstDayOfWeek 宏明確地傳送此訊息 \_ 。
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966325"
---
# <a name="mcm_getfirstdayofweek-message"></a>MCM \_ GETFIRSTDAYOFWEEK 訊息

抓取月曆控制項的每週第一天。 您可以使用 [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含兩個值的 **DWORD** 值。 如果一周的第一天設定為地區設定 IFIRSTDAYOFWEEK 以外 **的值** ，則最大的單字為非零值， \_ 否則為零。 低字組是代表一周第一天的 INT 值，其中0是星期一、1是星期二等等。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





