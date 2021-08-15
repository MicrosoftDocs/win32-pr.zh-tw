---
title: 'LB_SELITEMRANGE 訊息 (Winuser .h) '
description: 選取或取消選取多重選取清單方塊中的一或多個連續專案。
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958597"
---
# <a name="lb_selitemrange-message"></a>LB \_ SELITEMRANGE 訊息

選取或取消選取多重選取清單方塊中的一或多個連續專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**TRUE** 表示選取專案的範圍，或選取 [ **FALSE** ] 以取消選取專案。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要選取的第一個專案之以零為起始的索引。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定要選取之最後一個專案的以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

此訊息只能搭配多重選取清單方塊使用。

此訊息只能選取前65536個專案內的範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

