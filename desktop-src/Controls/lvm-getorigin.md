---
title: 'LVM_GETORIGIN 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的目前視圖原點。 您可以明確地傳送此訊息，或使用 ListView \_ GetOrigin 宏來傳送。
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411355"
---
# <a name="lvm_getorigin-message"></a>LVM \_ GETORIGIN 訊息

抓取清單視圖控制項的目前視圖原點。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收視圖來源的 [**點**](/previous-versions//dd162805(v=vs.85)) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果目前 view 為清單或報表檢視，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

