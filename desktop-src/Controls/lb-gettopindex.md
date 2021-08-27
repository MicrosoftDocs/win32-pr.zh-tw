---
title: 'LB_GETTOPINDEX 訊息 (Winuser .h) '
description: 取得清單方塊中第一個可見專案的索引。
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- LB_GETTOPINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b23360da45041e5a728f370e54f8250f216507dd439291a2ffce5ed383d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085378"
---
# <a name="lb_gettopindex-message"></a>LB \_ GETTOPINDEX 訊息

取得清單方塊中第一個可見專案的索引。 一開始，索引0的專案會出現在清單方塊的頂端，但如果清單方塊內容已滾動至另一個專案，則會位於最上方。 多重資料行清單方塊中第一個可見的專案是左上方的專案。

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

傳回值是清單方塊中第一個可見專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETTOPINDEX**](lb-settopindex.md)
</dt> </dl>

 

 





