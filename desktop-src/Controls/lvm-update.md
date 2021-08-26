---
title: 'LVM_UPDATE 訊息 (Commctrl .h) '
description: 更新清單視圖專案。 如果清單視圖控制項有 LVS) \_ AUTOARRANGE 樣式，此宏就會排列清單視圖控制項。 您可以使用 ListView Update 宏明確地傳送此訊息 \_ 。
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE 訊息 Windows 控制項
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
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915228"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





