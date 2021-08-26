---
title: 'TVM_GETCOUNT 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項中的專案計數。 您可以使用 TreeView GetCount 宏明確地傳送此訊息 \_ 。
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060348"
---
# <a name="tvm_getcount-message"></a>TVM \_ GETCOUNT 訊息

抓取樹狀檢視控制項中的專案計數。 您可以使用 [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案的計數。

## <a name="remarks"></a>備註

[**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)所傳回的節點計數限制為整數值。 如果您新增超過32767的節點，宏會傳回負數值。 新增65536節點之後，計數會傳回零。 發生這種情況時，樹狀檢視控制項會顯示為空白且沒有捲軸。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





