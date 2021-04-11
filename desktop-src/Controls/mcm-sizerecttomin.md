---
title: 'MCM_SIZERECTTOMIN 訊息 (Commctrl .h) '
description: 計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用 MonthCal SizeRectToMin 宏明確地傳送此訊息 \_ 。
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105983"
---
# <a name="mcm_sizerecttomin-message"></a>MCM \_ SIZERECTTOMIN 訊息

計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用 [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

On 專案時，會包含一個 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構的指標，此結構描述的區域大於或等於符合所需的行事歷數目所需的大小。 當此函式傳回時，會包含適合此日曆數目的最小 **矩形** 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

