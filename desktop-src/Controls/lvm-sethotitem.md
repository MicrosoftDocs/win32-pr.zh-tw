---
title: 'LVM_SETHOTITEM 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的熱專案。 您可以明確地傳送此訊息，或使用 ListView \_ SetHotItem 宏。
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685518"
---
# <a name="lvm_sethotitem-message"></a>LVM \_ SETHOTITEM 訊息

設定清單視圖控制項的熱專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是要設定為熱專案的專案。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前熱的專案索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





