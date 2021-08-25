---
title: 'MCM_SIZERECTTOMIN 訊息 (Commctrl .h) '
description: 計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用 MonthCal SizeRectToMin 宏明確地傳送此訊息 \_ 。
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN 訊息 Windows 控制項
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
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799228"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

