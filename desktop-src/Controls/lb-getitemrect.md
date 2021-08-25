---
title: 'LB_GETITEMRECT 訊息 (Winuser .h) '
description: 取得以清單方塊專案為範圍的矩形維度，這是清單方塊專案目前顯示在清單方塊中的範圍。
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e6fa6ed15f4d3a186800fd66e7c917e8620effa775c76f85b144e49207f12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799478"
---
# <a name="lb_getitemrect-message"></a>LB \_ GETITEMRECT 訊息

取得以清單方塊專案為範圍的矩形維度，這是清單方塊專案目前顯示在清單方塊中的範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

項目之以零起始的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收清單方塊中專案的用戶端座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

