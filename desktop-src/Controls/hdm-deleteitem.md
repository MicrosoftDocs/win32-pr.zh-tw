---
title: 'HDM_DELETEITEM 訊息 (Commctrl .h) '
description: 從標題控制項刪除專案。 您可以明確地傳送此訊息，或使用標頭 \_ DeleteItem 宏。
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b0a48d769117ffd68f2ba2af9695fe7fce00031f297626ae48c111d4574dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697348"
---
# <a name="hdm_deleteitem-message"></a>HDM \_ DELETEITEM 訊息

從標題控制項刪除專案。 您可以明確地傳送此訊息，或使用 [**標頭 \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之專案的索引。

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



 

 





