---
title: 'HDM_GETFOCUSEDITEM 訊息 (Commctrl .h) '
description: 取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用標頭 \_ GetFocusedItem 宏。
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f71b1b374c4d12f6dfb493cb8f8e0ea46d9d48094f0aed3c95a037ab7f3ea4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006114"
---
# <a name="hdm_getfocuseditem-message"></a>HDM \_ GETFOCUSEDITEM 訊息

取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用 [**標頭 \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>未使用。 必須為零。</dd> <dt>

*lParam* 
</dt> <dd>未使用。 必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回焦點專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> </dl>

 

 





