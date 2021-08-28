---
title: 'LB_SETTOPINDEX 訊息 (Winuser .h) '
description: 確定清單方塊中的指定專案可以看見。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- LB_SETTOPINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b640b55ed2c6e3e38eea0b8bd23eb4f99d770dd49b4499f054f5ec38b71873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435458"
---
# <a name="lb_settopindex-message"></a>LB \_ SETTOPINDEX 訊息

確定清單方塊中的指定專案可以看見。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單方塊中專案的以零為基底的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

系統會將清單方塊內容滾動，讓指定的專案出現在清單方塊的頂端，或達到最大捲軸範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETTOPINDEX**](lb-gettopindex.md)
</dt> </dl>

 

 





