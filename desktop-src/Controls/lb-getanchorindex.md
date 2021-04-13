---
title: 'LB_GETANCHORINDEX 訊息 (Winuser .h) '
description: 取得錨定專案 \ 郵件的索引，也就是從中開始多重選取的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509303"
---
# <a name="lb_getanchorindex-message"></a>LB \_ GETANCHORINDEX 訊息

取得錨定專案的索引，也就是多個選取範圍開始的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。

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

傳回值是錨點專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)
</dt> </dl>

 

 





