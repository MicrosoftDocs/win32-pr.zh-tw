---
title: 'LVM_DELETEITEM 訊息 (Commctrl .h) '
description: 從清單視圖控制項中移除專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteItem 宏來傳送。
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM message Windows 控制項
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
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093852"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





