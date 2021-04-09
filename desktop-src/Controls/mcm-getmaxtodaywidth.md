---
title: 'MCM_GETMAXTODAYWIDTH 訊息 (Commctrl .h) '
description: 抓取 \ 0034 的最大寬度; today \ 0034;月曆控制項中的字串。 這包括標籤文字和日期文字。 您可以使用 MonthCal GetMaxTodayWidth 宏明確地傳送此訊息 \_ 。
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685987"
---
# <a name="mcm_getmaxtodaywidth-message"></a>MCM \_ GETMAXTODAYWIDTH 訊息

抓取月曆控制項中 "today" 字串的最大寬度。 這包括標籤文字和日期文字。 您可以使用 [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 "today" 字串的寬度（以圖元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





