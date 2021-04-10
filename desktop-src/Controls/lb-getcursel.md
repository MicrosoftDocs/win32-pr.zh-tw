---
title: 'LB_GETCURSEL 訊息 (Winuser .h) '
description: 取得單一選取清單方塊中目前選取之專案的索引（如果有的話）。
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025441"
---
# <a name="lb_getcursel-message"></a>LB \_ GETCURSEL 訊息

取得單一選取清單方塊中目前選取之專案的索引（如果有的話）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

在單一選取清單方塊中，傳回值是目前選取專案之以零為起始的索引。 如果沒有選取專案，則傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

若要在多重選取清單方塊中取出選取專案的索引，請使用 [**LB \_ GETSELITEMS**](lb-getselitems.md) 訊息。 若要判斷是否已選取在多重選取清單方塊中具有焦點矩形的專案，請使用 [**LB \_ GETSEL**](lb-getsel.md) 訊息。

如果傳送至多重選取清單方塊， **LB \_ GETCURSEL** 會傳回具有焦點矩形之專案的索引。 如果未選取任何專案，則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ GETSELITEMS**](lb-getselitems.md)
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> </dl>

 

 





