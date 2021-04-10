---
title: 'LVM_UPDATE 訊息 (Commctrl .h) '
description: 更新清單視圖專案。 如果清單視圖控制項有 LVS) \_ AUTOARRANGE 樣式，此宏就會排列清單視圖控制項。 您可以使用 ListView Update 宏明確地傳送此訊息 \_ 。
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843144"
---
# <a name="lvm_update-message"></a>LVM \_ 更新訊息

更新清單視圖專案。 如果清單視圖控制項有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式，此宏就會排列清單視圖控制項。 您可以使用 [**ListView \_ Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要更新之專案的索引。

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



 

 





