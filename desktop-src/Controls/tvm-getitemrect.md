---
title: 'TVM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取樹狀檢視專案的周框，並指出專案是否可見。 您可以使用 TreeView GetItemRect 宏明確地傳送此訊息 \_ 。
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094411"
---
# <a name="tvm_getitemrect-message"></a>TVM \_ GETITEMRECT 訊息

抓取樹狀檢視專案的周框，並指出專案是否可見。 您可以使用 [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定要對其取得周框矩形的專案部分。 如果此參數為 **TRUE**，周框矩形只會包含專案的文字。 否則，它會包含專案在樹狀檢視控制項中所占的整個行。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，在傳送訊息時，會包含要取得其矩形之專案的控制碼。 請參閱下列範例，以取得如何將專案控制碼放置在此參數中的詳細資訊。 從訊息傳回之後，這個參數會包含周框。 座標相對於樹狀檢視控制項的左上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果專案是可見的，且已成功取出周框，則傳回值為 **TRUE**。 否則，訊息會傳回 **FALSE** ，且不會取出周框。

## <a name="remarks"></a>備註

傳送此訊息時， *lParam* 參數包含要為其抓取矩形之專案的控制碼。 控制碼會放置在 *lParam* 中，如下列範例所示：


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

