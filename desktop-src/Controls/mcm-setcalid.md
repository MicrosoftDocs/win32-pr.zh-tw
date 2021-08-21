---
title: 'MCM_SETCALID 訊息 (Commctrl .h) '
description: 設定給定行事曆控制項的行事曆識別碼。 您可以使用 MonthCal SetCALID 宏明確地傳送此訊息 \_ 。
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575578"
---
# <a name="mcm_setcalid-message"></a>MCM \_ SETCALID 訊息

設定給定行事曆控制項的行事曆識別碼。 您可以使用 [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

行事曆識別碼。 其中一個行事 [曆識別碼](/windows/desktop/Intl/calendar-identifiers) 常數。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

