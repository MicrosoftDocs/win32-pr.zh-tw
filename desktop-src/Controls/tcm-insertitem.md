---
title: 'TCM_INSERTITEM 訊息 (Commctrl .h) '
description: 在索引標籤控制項中插入新的索引標籤。 您可以使用 TabCtrl InsertItem 宏明確地傳送此訊息 \_ 。
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829099"
---
# <a name="tcm_insertitem-message"></a>TCM \_ INSERTITEM 訊息

在索引標籤控制項中插入新的索引標籤。 您可以使用 [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新索引標籤的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，指定索引標籤的屬性。此訊息會忽略此結構的 **dwState** 和 **dwStateMask** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新索引標籤的索引，否則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TCM \_INSERTITEMW** (Unicode) 和 **TCM \_ INSERTITEMA** (ANSI) <br/>             |



 

 





