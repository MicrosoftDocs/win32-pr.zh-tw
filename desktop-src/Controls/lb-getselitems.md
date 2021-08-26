---
title: 'LB_GETSELITEMS 訊息 (Winuser .h) '
description: 填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a541c7efb0acb8d462cce42f0323393baff58e51d63e6a78a72a9d334c0eae81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085498"
---
# <a name="lb_getselitems-message"></a>LB \_ GETSELITEMS 訊息

填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要將其專案編號放在緩衝區中的已選取專案數目上限。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

緩衝區的指標，足以容納 *wParam* 參數所指定的整數數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是放置在緩衝區中的專案數目。 如果清單方塊是單一選取清單方塊，則傳回值為 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





