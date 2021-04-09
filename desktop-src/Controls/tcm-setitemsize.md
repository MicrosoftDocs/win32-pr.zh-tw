---
title: 'TCM_SETITEMSIZE 訊息 (Commctrl .h) '
description: 在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。 您可以使用 TabCtrl SetItemSize 宏明確地傳送此訊息 \_ 。
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843048"
---
# <a name="tcm_setitemsize-message"></a>TCM \_ SETITEMSIZE 訊息

在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。 您可以使用 [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定新寬度的 **INT** 值（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是指定新高度的 **INT** 值（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回舊的寬度和高度。 寬度是在傳回值的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而高度則在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。

## <a name="remarks"></a>備註

如果寬度設定為小於 [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)所設定的影像寬度，則索引標籤的寬度會設定為大於影像寬度的最小值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

