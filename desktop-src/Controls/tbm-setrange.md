---
title: 'TBM_SETRANGE 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最小和最大邏輯位置的範圍。
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061138"
---
# <a name="tbm_setrange-message"></a>TBM \_ SETRANGE 訊息

設定捲軸中滑杆的最小和最大邏輯位置的範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

重繪旗標。 如果此參數為 **TRUE**，則會在設定範圍之後重新繪製這些程式。 如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定滑杆的最小位置，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果目前滑杆的位置超出新的範圍， **TBM \_ SETRANGE** 訊息會將滑杆位置設定為新的最大值或最小值。

因為此訊息採用 2 16 位不帶正負號的整數值，此訊息可以指定的最大範圍是從0到65535。 若要指定較大的範圍值，請使用 [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) 和 [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) 訊息。

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

