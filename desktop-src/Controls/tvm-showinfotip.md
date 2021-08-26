---
title: 'TVM_SHOWINFOTIP 訊息 (Commctrl .h) '
description: 顯示樹狀檢視控制項中所指定專案的提示。 您可以明確地傳送此訊息，或使用 TreeView \_ ShowInfoTip 宏來傳送。
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913918"
---
# <a name="tvm_showinfotip-message"></a>TVM \_ SHOWINFOTIP 訊息

顯示樹狀檢視控制項中所指定專案的提示。 您可以明確地傳送此訊息，或使用 [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* \[在\]
</dt> <dd>

專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零。

## <a name="remarks"></a>備註

大部分的應用程式都不會使用此訊息。 提示會自動顯示。 如需詳細資訊，請參閱 [關於 Tree-View 控制項](tree-view-controls.md) 總覽中的使用樹狀檢視提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





