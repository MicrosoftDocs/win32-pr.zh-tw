---
title: 'MCM_GETMAXSELCOUNT 訊息 (Commctrl .h) '
description: 抓取月曆控制項中可選取的最大日期範圍。 您可以使用 MonthCal GetMaxSelCount 宏明確地傳送此訊息 \_ 。
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025250"
---
# <a name="mcm_getmaxselcount-message"></a>MCM \_ GETMAXSELCOUNT 訊息

抓取月曆控制項中可選取的最大日期範圍。 您可以使用 [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 INT 值，代表可以為控制項選取的總天數。

## <a name="remarks"></a>備註

您可以使用 [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) 訊息來變更可選取的最大日期範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





