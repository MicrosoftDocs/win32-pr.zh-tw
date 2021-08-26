---
title: 'TBM_SETRANGEMIN 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最小邏輯位置。
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046068"
---
# <a name="tbm_setrangemin-message"></a>TBM \_ SETRANGEMIN 訊息

設定捲軸中滑杆的最小邏輯位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪旗標。 如果此參數為 **TRUE**，則訊息會在設定範圍之後重新繪製資訊區。 如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。

</dd> <dt>

*lParam* 
</dt> <dd>

滑杆的最小位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果目前滑杆的位置小於新的最小值， **TBM \_ SETRANGEMIN** 訊息會將滑杆位置設定為新的最小值。

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





