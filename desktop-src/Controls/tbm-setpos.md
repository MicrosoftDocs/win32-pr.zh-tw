---
title: 'TBM_SETPOS 訊息 (Commctrl .h) '
description: TBM_SETPOS 訊息：設定捲軸中滑杆的目前邏輯位置。
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ccd1cb35f8cde672c51baafe5623291e5449f90aa118eb36cb12152fe155385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078042"
---
# <a name="tbm_setpos-message"></a>TBM \_ SETPOS 訊息

設定捲軸中滑杆的目前邏輯位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪旗標。 如果此參數為 **TRUE**，則訊息會使用 *lParam* 所指定位置的滑杆來重新繪製控制項。 如果此參數為 **FALSE**，則訊息不會在新位置重繪滑杆。 請注意，無論 *wParam* 參數為何，訊息都會將滑杆位置 (的值設定為 [**TBM \_ GETPOS**](tbm-getpos.md)訊息所傳回) 。

</dd> <dt>

*lParam* 
</dt> <dd>

滑杆的新邏輯位置。 有效的邏輯位置是在最小至最大滑杆位置的最小值範圍中的整數值。 如果這個值超出控制項的最大和最小範圍，則會將位置設定為最大值或最小值。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





