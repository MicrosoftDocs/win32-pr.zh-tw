---
title: 'TBM_SETRANGEMAX 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最大邏輯位置。
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26b4a588e67164b96db8256116466206d0274a5bc64caedbcb1ccf25135ce62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829591"
---
# <a name="tbm_setrangemax-message"></a>TBM \_ SETRANGEMAX 訊息

設定捲軸中滑杆的最大邏輯位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪旗標。 如果此參數為 **TRUE**，則會在設定範圍之後重新繪製這些程式。 如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。

</dd> <dt>

*lParam* 
</dt> <dd>

滑杆的最大位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果目前滑杆的位置大於新的最大值， **TBM \_ SETRANGEMAX** 訊息會將滑杆位置設定為新的最大值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





