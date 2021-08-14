---
title: 'LVM_GETHOTITEM 訊息 (Commctrl .h) '
description: 抓取熱專案的索引。 您可以明確地傳送此訊息，或使用 ListView \_ GetHotItem 宏。
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743bd7a80a58bec41fa5a75f24b0e333ab33ad152909adb6ea69a9c4ca0fd78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958397"
---
# <a name="lvm_gethotitem-message"></a>LVM \_ GETHOTITEM 訊息

抓取熱專案的索引。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回熱專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





