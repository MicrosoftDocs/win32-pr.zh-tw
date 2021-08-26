---
title: 'LVM_APPROXIMATEVIEWRECT 訊息 (Commctrl .h) '
description: 計算顯示指定專案數目所需的大約寬度和高度。 您可以明確地傳送此訊息，或使用 ListView \_ ApproximateViewRect 宏。
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047058"
---
# <a name="lvm_approximateviewrect-message"></a>LVM \_ APPROXIMATEVIEWRECT 訊息

計算顯示指定專案數目所需的大約寬度和高度。 您可以明確地傳送此訊息，或使用 [**ListView \_ ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要在控制項中顯示的專案數目。 如果此參數設定為-1，則訊息會使用控制項中的總專案數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是控制項的建議 x 維度（以圖元為單位）。 這個參數可以設定為-1，以允許訊息使用目前的寬度值。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是控制項的建議 y 維度（以圖元為單位）。 這個參數可以設定為-1，以允許訊息使用目前的高度值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，此值會將大約寬度 (保存在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) 所需的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) 和高度 (（以圖元為單位）。

## <a name="remarks"></a>備註

根據此訊息所提供的維度來設定清單視圖控制項的大小，可以優化重繪並減少閃爍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

