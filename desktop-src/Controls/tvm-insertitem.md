---
title: 'TVM_INSERTITEM 訊息 (Commctrl .h) '
description: 在樹狀檢視控制項中插入新專案。 您可以使用 TreeView InsertItem 宏明確地傳送此訊息 \_ 。
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f8a324613820b94e0bd2c49d8fa78136038471f820dd2b9ed8e38ace15f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060188"
---
# <a name="tvm_insertitem-message"></a>TVM \_ INSERTITEM 訊息

在樹狀檢視控制項中插入新專案。 您可以使用 [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa)結構的指標，指定樹狀檢視專案的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新專案的 **HTREEITEM** 控制碼，否則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TVM \_INSERTITEMW** (Unicode) 和 **TVM \_ INSERTITEMA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





