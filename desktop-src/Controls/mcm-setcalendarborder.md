---
title: 'MCM_SETCALENDARBORDER 訊息 (Commctrl .h) '
description: 設定框線的大小（以圖元為單位）。 您可以使用 MonthCal SetCalendarBorder 宏明確地傳送此訊息 \_ 。
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465248"
---
# <a name="mcm_setcalendarborder-message"></a>MCM \_ SETCALENDARBORDER 訊息

設定框線的大小（以圖元為單位）。 您可以使用 [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

若 **為 TRUE**，則會將框線大小設定為 *lParam* 指定的圖元數。 如果 **為 FALSE**，則會將框線大小重設為主題所指定的預設值，如果未使用主題則為零。

</dd> <dt>

*lParam* 
</dt> <dd>

框線大小的圖元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





