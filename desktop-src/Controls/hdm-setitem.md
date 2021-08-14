---
title: 'HDM_SETITEM 訊息 (Commctrl .h) '
description: 在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用標頭 \_ SetItem 宏。
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd0e2709a1b40bd4a564498cd0ae0b5d4e11861066aa9b0951815f92ee1c295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171063"
---
# <a name="hdm_setitem-message"></a>HDM \_ SETITEM 訊息

在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要變更其屬性之專案的目前索引。

</dd> <dt>

*lParam* 
</dt> <dd>

包含專案資訊之 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的指標。 傳送此訊息時，必須設定結構的 **遮罩** 成員，以指出要設定的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回非零值，否則傳回零。

## <a name="remarks"></a>備註

支援此訊息的 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構支援專案順序和影像清單資訊。 藉由使用這些成員，您可以控制顯示專案的順序，並指定要與專案一起顯示的影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDM \_SETITEMW** (Unicode) 和 **HDM \_ SETITEMA** (ANSI) <br/>                   |



 

 





