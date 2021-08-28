---
title: 'LB_GETCARETINDEX 訊息 (Winuser .h) '
description: 抓取在多重選取清單方塊中具有焦點之專案的索引。 您可以或可能不會選取此專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085538"
---
# <a name="lb_getcaretindex-message"></a>LB \_ GETCARETINDEX 訊息

抓取在多重選取清單方塊中具有焦點之專案的索引。 您可以或可能不會選取此專案。

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

傳回值是聚焦清單方塊專案以零為起始的索引，如果沒有任何專案具有焦點，則為0。

## <a name="remarks"></a>備註

此訊息也可以用來取得目前在單一選取清單方塊中選取之專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETCARETINDEX**](lb-setcaretindex.md)
</dt> </dl>

 

 





