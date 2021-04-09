---
title: 'LB_SETCARETINDEX 訊息 (Winuser .h) '
description: 將焦點矩形設定為多重選取清單方塊中指定索引處的專案。 如果看不到專案，則會將它滾動到視野中。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844112"
---
# <a name="lb_setcaretindex-message"></a>LB \_ SETCARETINDEX 訊息

將焦點矩形設定為多重選取清單方塊中指定索引處的專案。 如果看不到專案，則會將它滾動到視野中。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要接收焦點矩形之清單方塊專案的以零為基底的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

如果這個值為 **FALSE**，則會滾動專案直到完全可見為止;若為 **TRUE**，則會滾動專案，直到至少有部分可見為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值會是 LB \_ ERR (-1) 。 否則， \_ 會傳回 LB ok (0) 。

## <a name="remarks"></a>備註

如果將此訊息傳送至不包含選取專案的單一選取清單方塊，則會將插入號索引設定為 *wParam* 參數所指定的專案。 如果單一選取清單方塊包含選取的專案，清單方塊會傳回 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> </dl>

 

 





