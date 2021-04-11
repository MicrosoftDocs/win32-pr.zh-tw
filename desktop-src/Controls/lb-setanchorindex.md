---
title: 'LB_SETANCHORINDEX 訊息 (Winuser .h) '
description: 設定錨定專案 \ 郵件，也就是從中開始多重選取的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105539"
---
# <a name="lb_setanchorindex-message"></a>LB \_ SETANCHORINDEX 訊息

設定錨定專案，也就是多個選取範圍開始的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定新錨定專案的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為零。

如果訊息失敗，則傳回值為 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)
</dt> </dl>

 

 





