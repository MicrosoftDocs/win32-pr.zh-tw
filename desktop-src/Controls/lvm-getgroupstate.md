---
title: 'LVM_GETGROUPSTATE 訊息 (Commctrl .h) '
description: 取得指定群組的狀態。 明確地傳送此訊息，或使用 ListView \_ GetGroupState 宏。
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464413"
---
# <a name="lvm_getgroupstate-message"></a>LVM \_ GETGROUPSTATE 訊息

取得指定群組的狀態。 明確地傳送此訊息，或使用 [**ListView \_ GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定 group by **iGroupId** (參閱 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構) 。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

指定要取出的狀態值。 這是 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)的 **state** 成員所列出的旗標組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回已設定之狀態值的組合。 例如，如果 *lParam* 是 LVGS 折迭 \_ 的，且傳回的值為零，則 \_ 不會設定 LVGS 折迭狀態。 如果找不到群組，就會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





