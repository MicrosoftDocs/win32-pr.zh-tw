---
title: 'TCM_DESELECTALL 訊息 (Commctrl .h) '
description: 重設索引標籤控制項中的專案，清除任何已設定為 TCIS \_ BUTTONPRESSED 狀態的專案。 您可以使用 TabCtrl DeselectAll 宏明確地傳送此訊息 \_ 。
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105749"
---
# <a name="tcm_deselectall-message"></a>TCM \_ DESELECTALL 訊息

重設索引標籤控制項中的專案，清除任何已設定為 [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) 狀態的專案。 您可以使用 [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定專案 deselection 範圍的旗標。 如果此參數設定為 **FALSE**，則會重設所有索引標籤專案。 如果設定為 **TRUE**，則會重設目前選取專案以外的所有索引標籤專案。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

只有在已設定 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式旗標的情況下，此訊息才有意義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





