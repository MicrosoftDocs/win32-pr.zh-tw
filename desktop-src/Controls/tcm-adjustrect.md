---
title: 'TCM_ADJUSTRECT 訊息 (Commctrl .h) '
description: 在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。 您可以使用 TabCtrl AdjustRect 宏明確地傳送此訊息 \_ 。
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba09a88f12a25b87f507d70961a816412f2679da0fb9e1cb6ed6c760ecca320e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105008"
---
# <a name="tcm_adjustrect-message"></a>TCM \_ ADJUSTRECT 訊息

在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。 您可以使用 [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要執行的作業。 如果此參數為 **TRUE**， *lParam* 會指定一個顯示矩形，並接收對應的視窗矩形。 如果此參數為 **FALSE**，則 *lParam* 會指定視窗矩形，並接收對應的顯示區域。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，該結構會指定指定的矩形，並接收匯出的矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此訊息只適用于位於頂端的索引標籤控制項。 它並不適用于側邊或底部的索引標籤控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

