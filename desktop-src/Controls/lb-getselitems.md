---
title: 'LB_GETSELITEMS 訊息 (Winuser .h) '
description: 填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS message Windows 控制項
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
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934450"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





