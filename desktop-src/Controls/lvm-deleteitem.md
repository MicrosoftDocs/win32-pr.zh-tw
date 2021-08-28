---
title: 'LVM_DELETEITEM 訊息 (Commctrl .h) '
description: 從清單視圖控制項中移除專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteItem 宏來傳送。
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88520e7d4f9d0d3ff22f90d7cea033b7674cfcbadbf55358f7ced8cc36c2399a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958417"
---
# <a name="lvm_deleteitem-message"></a>LVM \_ DELETEITEM 訊息

從清單視圖控制項中移除專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





